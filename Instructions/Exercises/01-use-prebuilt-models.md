<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div dir="rtl"><markdown-accessiblity-table data-catalyst=""><table>
  <thead>
  <tr>
  <th>lab</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="auto"><table>
  <thead>
  <tr>
  <th>title</th>
  <th>module</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="auto">استخدام نماذج Document Intelligence التي تم إنشاؤها مسبقًا</div></td>
  <td><div dir="auto">Module 6 - Document Intelligence</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto">استخدام نماذج Document Intelligence التي تم إنشاؤها مسبقًا</h1><a id="user-content-استخدام-نماذج-document-intelligence-التي-تم-إنشاؤها-مسبقًا" class="anchor" aria-label="Permalink: استخدام نماذج Document Intelligence التي تم إنشاؤها مسبقًا" href="#استخدام-نماذج-document-intelligence-التي-تم-إنشاؤها-مسبقًا"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">في هذا التمرين، ستقوم بإعداد مورد Azure AI Document Intelligence في اشتراك Azure الخاص بك. ستستخدم Azure AI Document Intelligence Studio وC# أو Python لإرسال النماذج إلى هذا المورد للتحليل.</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">إنشاء مورد Azure AI Document Intelligence</h2><a id="user-content-إنشاء-مورد-azure-ai-document-intelligence" class="anchor" aria-label="Permalink: إنشاء مورد Azure AI Document Intelligence" href="#إنشاء-مورد-azure-ai-document-intelligence"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">قبل أن تتمكن من الاتصال بخدمة Azure AI Document Intelligence، يجب عليك إنشاء مورد لاستضافة هذه الخدمة في Azure:</p>
<ol dir="rtl">
<li>في علامة تبويب المتصفح، افتح مدخل Microsoft Azure على <a href="https://portal.azure.com?azure-portal=true" rel="nofollow">https://portal.azure.com</a>، وقم بتسجيل الدخول باستخدام حساب Microsoft المرتبط باشتراكك في Azure.</li>
<li>في الصفحة الرئيسية لمدخل Microsoft Azure، انتقل إلى مربع البحث العلوي واكتب <strong>Document Intelligence</strong>، ثم اضغط على <strong>إدخال</strong>.</li>
<li>في صفحة <strong>ذكاء المستند</strong>، حدد <strong>إنشاء ذكاء مستند</strong>.</li>
<li>في صفحة <strong>إنشاء استخبارات المستندات</strong>، استخدم ما يلي لتكوين الموارد الخاصة بك:
<ul dir="rtl">
<li><strong>Subscription</strong>: حدد اشتراك Azure الخاص بك.</li>
<li><strong>مجموعة الموارد</strong>: حدد أو أنشئ مجموعة موارد باسم فريد مثل <em>DocIntelligenceResources</em>.</li>
<li><strong>المنطقة</strong>: حدد منطقة قريبة منك.</li>
<li><strong>الاسم</strong>: أدخل اسمًا فريدًا عالميًا.</li>
<li><strong>مستوى الأسعار</strong>: حدد <strong>Free F0</strong> (إذا لم يكن لديك مستوى مجاني متوفر، فحدد <strong>Standard S0</strong>).</li>
</ul>
</li>
<li>ثم حدد ⁧⁧<strong>⁩⁩⁩⁩مراجعة + إنشاء⁦⁦</strong>⁩⁩ و<strong>إنشاء</strong>. انتظر بينما يقوم Azure بإنشاء مورد Azure AI Document Intelligence.</li>
<li>عندما تكتمل عملية النشر، حدد <strong>الانتقال إلى المورد</strong>. اترك هذه الصفحة مفتوحة لبقية هذا التمرين.</li>
</ol>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">استخدام نموذج القراءة</h2><a id="user-content-استخدام-نموذج-القراءة" class="anchor" aria-label="Permalink: استخدام نموذج القراءة" href="#استخدام-نموذج-القراءة"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">لنبدأ باستخدام <strong>Azure AI Document Intelligence Studio</strong> ونموذج القراءة لتحليل مستند بلغات متعددة. ستقوم بربط Azure AI Document Intelligence Studio بالمورد الذي قمت بإنشائه للتو لإجراء التحليل:</p>
<ol dir="rtl">
<li>
<p dir="auto">افتح علامة تبويب جديدة للمتصفح وانتقل إلى <strong>Azure AI Document Intelligence Studio</strong> على <a href="https://documentintelligence.ai.azure.com/studio" rel="nofollow">https://documentintelligence.ai.azure.com/studio</a>.</p>
</li>
<li>
<p dir="auto">ضمن <strong>تحليل المستند</strong>، حدد لوحة <strong>القراءة</strong>.</p>
</li>
<li>
<p dir="auto">إذا طلب منك تسجيل الدخول إلى حسابك، فاستخدم بيانات اعتماد Azure.</p>
</li>
<li>
<p dir="auto">إذا تم سؤالك عن مورد Azure AI Document Intelligence الذي يجب استخدامه، فحدد الاشتراك واسم المورد اللذين استخدمتهما عند إنشاء مورد Azure AI Document Intelligence.</p>
</li>
<li>
<p dir="auto">في قائمة المستندات على اليسار، حدد <strong>read-german.pdf</strong>.</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/read-german-sample.png#lightbox"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/read-german-sample.png#lightbox" alt="لقطة شاشة تعرض صفحة القراءة في Azure AI Document Intelligence Studio." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="auto">في الجزء العلوي الأيسر، حدد <strong>خيارات التحليل</strong>، ثم قم بتمكين مربع الاختيار <strong>اللغة</strong> (ضمن <strong>الاكتشاف الاختياري</strong>) في جزء <strong>خيارات التحليل</strong> وانقر فوق <strong>حفظ</strong>.</p>
</li>
<li>
<p dir="auto">في الجزء العلوي الأيسر، حدد <strong>تشغيل التحليل</strong>.</p>
</li>
<li>
<p dir="auto">عند اكتمال التحليل، يظهر النص المستخرج من الصورة على اليمين في علامة التبويب <strong>المحتوى</strong>. راجع هذا النص وقارنه بالنص الموجود في الصورة الأصلية للتأكد من دقته.</p>
</li>
<li>
<p dir="auto">حدد علامة التبويب <strong>Result</strong>. تعرض علامة التبويب هذه التعليمات البرمجية JSON المستخرجة.</p>
</li>
<li>
<p dir="auto">قم بالتمرير إلى أسفل التعليمة البرمجية JSON في علامة تبويب <strong>Result</strong>. لاحظ أن نموذج القراءة قد اكتشف لغة كل فترة تم الإشارة إليها بواسطة <code>locale</code>. معظم الفواصل باللغة الألمانية (رمز اللغة <code>de</code>) ولكن يمكنك العثور على رموز لغوية أخرى في الفواصل (على سبيل المثال، اللغة الإنجليزية - رمز اللغة <code>en</code> - في أحد الفترات الأخيرة).</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/language-detection.png#lightbox"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/language-detection.png#lightbox" alt="لقطة شاشة توضح اكتشاف اللغة لفترتين في النتائج من نموذج القراءة في Azure AI Document Intelligence Studio." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">الآن دعونا نستكشف التطبيق الذي يستخدم SDK لخدمة Azure Document Intelligence. ستقوم بتطوير تطبيقك باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية لتطبيقك في مستودع GitHub.</p>
<blockquote>
<p dir="auto"><strong>تلميح</strong>: إذا كنت قد قمت بالفعل باستنساخ مستودع <strong>mslearn-ai-document-intelligence</strong>، فافتحه في تعليمة Visual Studio البرمجية. بخلاف ذلك، اتبع الخطوات التالية لاستنساخه إلى بيئة التطوير الخاصة بك.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="auto">ابدأ تشغيل Visual Studio Code.</p>
</li>
<li>
<p dir="auto">افتح لوحة (SHIFT+CTRL+P) وشغّل **Git: استنسخ الأمر ** لاستنساخ مستودع <code>https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence</code> إلى مجلد محلي (لا يُهم أي مجلد).</p>
</li>
<li>
<p dir="auto">عند استنساخ المستودع، افتح المجلد في Visual Studio Code.</p>
<blockquote>
<p dir="auto"><strong>ملاحظة</strong>: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق <strong>نعم، أثق في خيار الكُتاب</strong> في النافذة المنبثقة.</p>
</blockquote>
</li>
<li>
<p dir="auto">انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.</p>
<blockquote>
<p dir="auto"><strong>ملاحظة</strong>: إذا جرت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <strong>ليس الآن</strong>. إذا تمت مطالبتك برسالة <em>اكتشاف مشروع وظيفة Azure في المجلد</em>، يمكنك إغلاق هذه الرسالة بأمان.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">تكوين تطبيقك</h2><a id="user-content-تكوين-تطبيقك" class="anchor" aria-label="Permalink: تكوين تطبيقك" href="#تكوين-تطبيقك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">تم توفير تطبيقات لكل من C# وPython، بالإضافة إلى ملف pdf نموذجي ستستخدمه لاختبار Document Intelligence. يتميز كلا التطبيقين بنفس الوظيفة. أولاً، ستقوم بإكمال بعض الأجزاء الرئيسية للتطبيق لتمكين استخدام مورد Azure Document Intelligence الخاص بك.</p>
<ol dir="rtl">
<li>
<p dir="auto">قم بالتحقُّق من الفاتورة التالية وانتبه إلى بعض حقولها وقيمها. هذه هي الفاتورة التي ستحللها التعليمة البرمجية.</p>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/read-german-sample.png#lightbox"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/Instructions/media/sample-invoice.png#lightbox" alt="لقطة شاشة تظهر نموذجًا لمستند الفاتورة." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="auto">في تعليمة Visual Studio البرمجية  في جزء <strong>المستكشف</strong>، انتقِل إلى المجلد <strong>Labfiles/01-prebuild-models</strong> وقم بتوسيع المجلد <strong>CSharp</strong> أو <strong>Python</strong> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure Document Intelligence فيه.</p>
</li>
<li>
<p dir="auto">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وحدد <strong>فتح محطة طرفية متكاملة</strong>. بعد ذلك، قم بتثبيت حزمة SDK لبرنامج Azure Form Recognizer (الاسم السابق لـ Document Intelligence) من خلال تشغيل الأمر المناسب لتفضيل اللغة الخاص بك:</p>
</li>
<p dir="rtl"><strong>:#C</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><code>dotnet add package Azure.AI.FormRecognizer --version 4.1.0</code></pre></div>
<p dir="rtl">:<strong>Python</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><code>pip install azure-ai-formrecognizer==3.3.3</code></pre></div>

</ol>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">إضافة التعليمة البرمجية لاستخدام خدمة Azure Document Intelligence</h2><a id="user-content-إضافة-التعليمة-البرمجية-لاستخدام-خدمة-azure-document-intelligence" class="anchor" aria-label="Permalink: إضافة التعليمة البرمجية لاستخدام خدمة Azure Document Intelligence" href="#إضافة-التعليمة-البرمجية-لاستخدام-خدمة-azure-document-intelligence"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">أنت الآن جاهز لاستخدام SDK لتقييم ملف pdf.</p>
<ol dir="rtl">
<li>
<p dir="auto">انتقل إلى علامة تبويب المتصفح التي تعرض نظرة عامة حول Azure AI Document Intelligence في مدخل Microsoft Azure. في الجزء الأيسر، ضمن <em>إدارة الموارد</em>، حدد <strong>المفاتيح ونقطة النهاية</strong>. إلى يمين قيمة <strong>نقطة النهاية</strong>، انقر فوق الزر <strong>نسخ إلى الحافظة</strong>.</p>
</li>
<li>
<p dir="auto">في جزء <strong>المستكشف</strong>، في مجلد <strong>CSharp</strong> أو <strong>Python</strong>، افتح ملف التعليمة البرمجية الخاص باللغة المفضلة لديك، واستبدل <code>&lt;Endpoint URL&gt;</code> بالسلسلة التي نسختها للتو:</p>
</li>
<p dir="rtl"><strong>C#</strong>: <em><strong>Program.cs</strong></em></p>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><code>string apiKey = &quot;&lt;API Key&gt;&quot;;</code></pre></div>
<p dir="rtl"><strong>Python</strong>: <em><strong>document-analysis.py</strong></em></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><code>endpoint = &quot;&lt;Endpoint URL&gt;&quot;;</code></pre></div>

<li>
<p dir="auto">انتقِل إلى علامة تبويب المتصفح التي تعرض <strong>مفاتيح Azure AI Document Intelligence ونقطة النهاية</strong> في مدخل Microsoft Azure. إلى يمين قيمة <strong>KEY 1</strong>، انقر فوق الزر <em>نسخ إلى الحافظة</em>*.</p>
</li>
<li>
<p dir="auto">في ملف التعليمات البرمجية في تعليمة Visual Studio البرمجية، حدد موقع هذا السطر واستبدل <code>&lt;API Key&gt;</code> بالسلسلة التي نسختها للتو:</p>
</li>
<p dir="rtl"><strong>C#</strong></p>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><code>string apiKey = &quot;&lt;API Key&gt;&quot;;</code></pre></div>
<p dir="rtl"><strong>Python</strong></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><code>key = &quot;&lt;API Key&gt;&quot;;</code></pre></div>

<li>
<p dir="auto">حدد موقع التعليق <code>Create the client</code>. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:</p>
</li>
<p dir="rtl"><strong>#C</strong></p>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><code>var cred = new AzureKeyCredential(apiKey);
var client = new DocumentAnalysisClient(new Uri(endpoint), cred);</code></pre></div>
<p dir="rtl"><strong>Python</strong></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><code>document_analysis_client = DocumentAnalysisClient(
    endpoint=endpoint, credential=AzureKeyCredential(key)
)</code></pre></div>

<li>
<p dir="auto">حدد موقع التعليق <code>Analyze the invoice</code>. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:</p>
</li>
<p dir="rtl"><strong>#C</strong></p>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><code>AnalyzeDocumentOperation operation = await client.AnalyzeDocumentFromUriAsync(WaitUntil.Completed, "prebuilt-invoice", fileUri);</code></pre></div>
<p dir="rtl"><strong>Python</strong></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><code>poller = document_analysis_client.begin_analyze_document_from_url(
    fileModelId, fileUri, locale=fileLocale
)</code></pre></div>

<li>
<p dir="auto">حدد موقع التعليق <code>Display invoice information to the user</code>. بعد ذلك، في الأسطر الجديدة، أدخل التعليمات البرمجية التالية:</p>
</li>
<p dir="rtl"><strong>#C</strong></p>
<div class="highlight highlight-source-cs notranslate position-relative overflow-auto" dir="auto"><pre><code>AnalyzeResult result = operation.Value;
<br>
foreach (AnalyzedDocument invoice in result.Documents)
{
    if (invoice.Fields.TryGetValue("VendorName", out DocumentField? vendorNameField))
    {
        if (vendorNameField.FieldType == DocumentFieldType.String)
        {
            string vendorName = vendorNameField.Value.AsString();
            Console.WriteLine($"Vendor Name: '{vendorName}', with confidence {vendorNameField.Confidence}.");
        }
}</code></pre></div>
<p dir="rtl"><strong>Python</strong></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><code>receipts = poller.result()
<br>
for idx, receipt in enumerate(receipts.documents):
<br>
    vendor_name = receipt.fields.get("VendorName")
    if vendor_name:
        print(f"\nVendor Name: {vendor_name.value}, with confidence {vendor_name.confidence}.")</code></pre></div>
<blockquote>
<p dir="auto">[!NOTE]
لقد أضفت تعليمة برمجية لعرض اسم المورد. يتضمَّن مشروع البداية أيضًا تعليمة برمجية لعرض <em>اسم العميل</em> و<em>إجمالي الفاتورة</em>.</p>
</blockquote>

<li>
<p dir="auto">احفظ التغييرات في ملف التعليمة البرمجية.</p>
</li>
<li>
<p dir="auto">في جزء الوحدة الطرفية التفاعلية، تأكد من أن سياق المجلد هو المجلد الخاص باللغة المفضلة لديك. ثم أدخل الأمر التالي لتشغيل التطبيق.</p>
</li>
<li>
<p dir="auto"><em><strong>بالنسبة لـ C# فقط</strong></em>، لبناء مشروعك، أدخل هذا الأمر:</p>
<p dir="rtl"><strong>:#C</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><code>dotnet build</code></pre></div>
</li>
<li>
<p dir="auto">لتشغيل التعليمات البرمجية الخاصة بك، أدخل هذا الأمر:</p>
<p dir="rtl"><strong>:#C</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><code>dotnet run</code></pre></div>
<p dir="rtl">:<strong>Python</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><code>python document-analysis.py</code></pre></div>
</li>
</ol>
<p dir="auto">يعرض البرنامج اسم المورد واسم العميل وإجمالي الفاتورة مع مستويات الثقة. قارن القيم التي يبلغ عنها مع عينة الفاتورة التي فتحتها في بداية هذا القسم.</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">إذا انتهيت من استخدام مورد Azure، فتذكر حذف المورد في <a href="https://portal.azure.com/?azure-portal=true" rel="nofollow">مدخل Microsoft Azure</a> لتجنب المزيد من الرسوم.</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">مزيد من المعلومات</h2><a id="user-content-مزيد-من-المعلومات" class="anchor" aria-label="Permalink: مزيد من المعلومات" href="#مزيد-من-المعلومات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto">لمزيد من المعلومات حول خدمة Document Intelligence، راجع <a href="https://learn.microsoft.com/azure/ai-services/document-intelligence/?azure-portal=true" rel="nofollow">مستندات Document Intelligence</a>.</p>
</article></div></div>
