---
lab:
  title: استخدام نماذج Document Intelligence التي تم إنشاؤها مسبقًا
  module: Module 6 - Document Intelligence
---

# استخدام نماذج Document Intelligence التي تم إنشاؤها مسبقًا

في هذا التمرين، ستقوم بإعداد مورد Azure AI Document Intelligence في اشتراك Azure الخاص بك. ستستخدم Azure AI Document Intelligence Studio وC# أو Python لإرسال النماذج إلى هذا المورد للتحليل.

## إنشاء مورد Azure AI Document Intelligence

قبل أن تتمكن من الاتصال بخدمة Azure AI Document Intelligence، يجب عليك إنشاء مورد لاستضافة هذه الخدمة في Azure:

1. في علامة تبويب المتصفح، افتح مدخل Microsoft Azure على [https://portal.azure.com](https://portal.azure.com?azure-portal=true)، وقم بتسجيل الدخول باستخدام حساب Microsoft المرتبط باشتراكك في Azure.
1. في الصفحة الرئيسية لمدخل Microsoft Azure، انتقل إلى مربع البحث العلوي واكتب **Document Intelligence**، ثم اضغط على **إدخال**.
1. في صفحة **ذكاء المستند**، حدد **إنشاء ذكاء مستند**.
1. في صفحة **إنشاء استخبارات المستندات**، استخدم ما يلي لتكوين الموارد الخاصة بك:
    - **Subscription**: حدد اشتراك Azure الخاص بك.
    - **مجموعة الموارد**: حدد أو أنشئ مجموعة موارد باسم فريد مثل *DocIntelligenceResources*.
    - **المنطقة**: حدد منطقة قريبة منك.
    - **الاسم**: أدخل اسمًا فريدًا عالميًا.
    - **مستوى الأسعار**: حدد **Free F0** (إذا لم يكن لديك مستوى مجاني متوفر، فحدد **Standard S0**).
1. ثم حدد ⁧⁧**⁩⁩⁩⁩مراجعة + إنشاء⁦⁦**⁩⁩ و**إنشاء**. انتظر بينما يقوم Azure بإنشاء مورد Azure AI Document Intelligence.
1. عندما تكتمل عملية النشر، حدد **الانتقال إلى المورد**. اترك هذه الصفحة مفتوحة لبقية هذا التمرين.

## استخدام نموذج القراءة

لنبدأ باستخدام **Azure AI Document Intelligence Studio** ونموذج القراءة لتحليل مستند بلغات متعددة. ستقوم بربط Azure AI Document Intelligence Studio بالمورد الذي قمت بإنشائه للتو لإجراء التحليل:

1. افتح علامة تبويب جديدة للمتصفح وانتقل إلى **Azure AI Document Intelligence Studio** على [https://documentintelligence.ai.azure.com/studio](https://documentintelligence.ai.azure.com/studio).
1. ضمن **تحليل المستند**، حدد لوحة **القراءة**.
1. إذا طلب منك تسجيل الدخول إلى حسابك، فاستخدم بيانات اعتماد Azure.
1. إذا تم سؤالك عن مورد Azure AI Document Intelligence الذي يجب استخدامه، فحدد الاشتراك واسم المورد اللذين استخدمتهما عند إنشاء مورد Azure AI Document Intelligence.
1. في قائمة المستندات على اليسار، حدد **read-german.pdf**.

    ![لقطة شاشة تعرض صفحة القراءة في Azure AI Document Intelligence Studio.](../media/read-german-sample.png#lightbox)

1. في الجزء العلوي الأيسر، حدد **خيارات التحليل**، ثم قم بتمكين مربع الاختيار **اللغة** (ضمن **الاكتشاف الاختياري**) في جزء **خيارات التحليل** وانقر فوق **حفظ**. 
1. في الجزء العلوي الأيسر، حدد **تشغيل التحليل**.
1. عند اكتمال التحليل، يظهر النص المستخرج من الصورة على اليمين في علامة التبويب **المحتوى**. راجع هذا النص وقارنه بالنص الموجود في الصورة الأصلية للتأكد من دقته.
1. حدد علامة التبويب **Result**. تعرض علامة التبويب هذه التعليمات البرمجية JSON المستخرجة. 
1. قم بالتمرير إلى أسفل التعليمة البرمجية JSON في علامة تبويب **Result**. لاحظ أن نموذج القراءة قد اكتشف لغة كل فترة تم الإشارة إليها بواسطة `locale`. معظم الفواصل باللغة الألمانية (رمز اللغة `de`) ولكن يمكنك العثور على رموز لغوية أخرى في الفواصل (على سبيل المثال، اللغة الإنجليزية - رمز اللغة `en` - في أحد الفترات الأخيرة).

    ![لقطة شاشة توضح اكتشاف اللغة لفترتين في النتائج من نموذج القراءة في Azure AI Document Intelligence Studio.](../media/language-detection.png#lightbox)

## الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية

الآن دعونا نستكشف التطبيق الذي يستخدم SDK لخدمة Azure Document Intelligence. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.

> **تلميح**: إذا كنت قد قمت بالفعل باستنساخ مستودع **mslearn-ai-document-intelligence**، فافتحه في تعليمة Visual Studio البرمجية. بخلاف ذلك، اتبع الخطوات التالية لاستنساخه إلى بيئة التطوير الخاصة بك.

1. ابدأ تشغيل Visual Studio Code.
1. افتح لوحة (SHIFT+CTRL+P) وشغّل **Git: استنسخ الأمر ** لاستنساخ مستودع `https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence` إلى مجلد محلي (لا يُهم أي مجلد).
1. عند استنساخ المستودع، افتح المجلد في Visual Studio Code.

    > **ملاحظة**: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق **نعم، أثق في خيار الكُتاب** في النافذة المنبثقة.

1. انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.

    > **ملاحظة**: إذا جرت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد **ليس الآن**. إذا تمت مطالبتك برسالة *اكتشاف مشروع وظيفة Azure في المجلد*، يمكنك إغلاق هذه الرسالة بأمان.

## تكوين تطبيقك

تم توفير تطبيقات لكل من C# وPython، بالإضافة إلى ملف pdf نموذجي ستستخدمه لاختبار Document Intelligence. يتميز كلا التطبيقين بنفس الوظيفة. أولاً، ستقوم بإكمال بعض الأجزاء الرئيسية للتطبيق لتمكين استخدام مورد Azure Document Intelligence الخاص بك.

1. قم بالتحقُّق من الفاتورة التالية وانتبه إلى بعض حقولها وقيمها. هذه هي الفاتورة التي ستحللها التعليمة البرمجية.

    ![لقطة شاشة تظهر نموذجًا لمستند الفاتورة.](../media/sample-invoice.png#lightbox)

1. في تعليمة Visual Studio البرمجية  في جزء **المستكشف**، انتقِل إلى المجلد **Labfiles/01-prebuild-models** وقم بتوسيع المجلد **CSharp** أو **Python** حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure Document Intelligence فيه.

1. انقر بزر الماوس الأيمن فوق المجلد **CSharp** أو **Python** الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وحدد **فتح محطة طرفية متكاملة**. بعد ذلك، قم بتثبيت حزمة SDK لبرنامج Azure Form Recognizer (الاسم السابق لـ Document Intelligence) من خلال تشغيل الأمر المناسب لتفضيل اللغة الخاص بك:

    **C#:**

    ```powershell
    dotnet add package Azure.AI.FormRecognizer --version 4.1.0
    ```

    **Python**:

    ```powershell
    pip install azure-ai-formrecognizer==3.3.3
    ```

## إضافة التعليمة البرمجية لاستخدام خدمة Azure Document Intelligence

أنت الآن جاهز لاستخدام SDK لتقييم ملف pdf.

1. انتقل إلى علامة تبويب المتصفح التي تعرض نظرة عامة حول Azure AI Document Intelligence في مدخل Microsoft Azure. في الجزء الأيسر، ضمن *إدارة الموارد*، حدد **المفاتيح ونقطة النهاية**. إلى يمين قيمة **نقطة النهاية**، انقر فوق الزر **نسخ إلى الحافظة**.
1. في جزء **المستكشف**، في مجلد **CSharp** أو **Python**، افتح ملف التعليمة البرمجية الخاص باللغة المفضلة لديك، واستبدل `<Endpoint URL>` بالسلسلة التي نسختها للتو:

    **C#**: ***Program.cs***

    ```csharp
    string endpoint = "<Endpoint URL>";
    ```

    **Python**: ***document-analysis.py***

    ```python
    endpoint = "<Endpoint URL>"
    ```

1. انتقِل إلى علامة تبويب المتصفح التي تعرض **مفاتيح Azure AI Document Intelligence ونقطة النهاية** في مدخل Microsoft Azure. إلى يمين قيمة **KEY 1**، انقر فوق الزر *نسخ إلى الحافظة**.
1. في ملف التعليمات البرمجية في تعليمة Visual Studio البرمجية، حدد موقع هذا السطر واستبدل `<API Key>` بالسلسلة التي نسختها للتو:

    **C#**

    ```csharp
    string apiKey = "<API Key>";
    ```

    **Python**

    ```python
    key = "<API Key>"
    ```

1. حدد موقع التعليق `Create the client`. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:

    **C#**

    ```csharp
    var cred = new AzureKeyCredential(apiKey);
    var client = new DocumentAnalysisClient(new Uri(endpoint), cred);
    ```

    **Python**

    ```python
    document_analysis_client = DocumentAnalysisClient(
        endpoint=endpoint, credential=AzureKeyCredential(key)
    )
    ```

1. حدد موقع التعليق `Analyze the invoice`. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:

    **C#**

    ```csharp
    AnalyzeDocumentOperation operation = await client.AnalyzeDocumentFromUriAsync(WaitUntil.Completed, "prebuilt-invoice", fileUri);
    ```

    **Python**

    ```python
    poller = document_analysis_client.begin_analyze_document_from_url(
        fileModelId, fileUri, locale=fileLocale
    )
    ```

1. حدد موقع التعليق `Display invoice information to the user`. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:

    **C#**

    ```csharp
    AnalyzeResult result = operation.Value;
    
    foreach (AnalyzedDocument invoice in result.Documents)
    {
        if (invoice.Fields.TryGetValue("VendorName", out DocumentField? vendorNameField))
        {
            if (vendorNameField.FieldType == DocumentFieldType.String)
            {
                string vendorName = vendorNameField.Value.AsString();
                Console.WriteLine($"Vendor Name: '{vendorName}', with confidence {vendorNameField.Confidence}.");
            }
        }
    ```

    **Python**

    ```python
    receipts = poller.result()
    
    for idx, receipt in enumerate(receipts.documents):
    
        vendor_name = receipt.fields.get("VendorName")
        if vendor_name:
            print(f"\nVendor Name: {vendor_name.value}, with confidence {vendor_name.confidence}.")
    ```

    > [!NOTE]
    > لقد أضفت تعليمة برمجية لعرض اسم المورد. يتضمَّن مشروع البداية أيضًا تعليمة برمجية لعرض *اسم العميل* و*إجمالي الفاتورة*.

1. احفظ التغييرات في ملف التعليمة البرمجية.

1. في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.

1. ***بالنسبة لـ C# فقط***، لبناء مشروعك، أدخل هذا الأمر:

    **C#:**

    ```powershell
    dotnet build
    ```

1. لتشغيل التعليمات البرمجية الخاصة بك، أدخل هذا الأمر:

    **C#:**

    ```powershell
    dotnet run
    ```

    **Python**:

    ```powershell
    python document-analysis.py
    ```

يعرض البرنامج اسم المورد واسم العميل وإجمالي الفاتورة مع مستويات الثقة. قارن القيم التي يبلغ عنها مع عينة الفاتورة التي فتحتها في بداية هذا القسم.

## تنظيف

إذا انتهيت من استخدام مورد Azure، فتذكر حذف المورد في [مدخل Microsoft Azure](https://portal.azure.com/?azure-portal=true) لتجنب المزيد من الرسوم.

## مزيد من المعلومات

لمزيد من المعلومات حول خدمة Document Intelligence، راجع [مستندات Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/?azure-portal=true).
