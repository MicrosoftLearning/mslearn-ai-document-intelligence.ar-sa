<div class="Box-sc-g0xbh4-0 eoaCFS js-snippet-clipboard-copy-unpositioned undefined" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><markdown-accessiblity-table data-catalyst=""><table>
  <thead>
  <tr>
  <th>lab</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl"><table>
  <thead>
  <tr>
  <th>title</th>
  <th>module</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div dir="rtl">استخراج البيانات من النماذج</div></td>
  <td><div dir="rtl">Module 6 - Document Intelligence</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">استخراج البيانات من النماذج</h1><a id="user-content-استخراج-البيانات-من-النماذج" class="anchor" aria-label="Permalink: استخراج البيانات من النماذج" href="#استخراج-البيانات-من-النماذج"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">نفترض أن الشركة تتطلب حاليًا من الموظفين شراء أوراق الطلبات يدويًا وإدخال البيانات في قاعدة البيانات. يريدون منك استخدام خدمات الذكاء الاصطناعي لتحسين عملية إدخال البيانات. قررت إنشاء نموذج تعلُّم آلي يقرأ النموذج وينتج بيانات منظمة يمكن استخدامها لتحديث قاعدة البيانات تلقائيًا.</p>
<p dir="rtl">تُعدَّ <strong>Azure AI Document Intelligence</strong> خدمة الذكاء الاصطناعي في Azure التي تُمكِّن المستخدمين من إنشاء برامج معالجة البيانات الآلية. يمكن لهذا البرنامج استخراج النصوص وأزواج المفاتيح/القيم والجداول من مستندات النماذج باستخدام التعرُّف البصري على الحروف (OCR). يحتوي Azure AI Document Intelligence على نماذج جاهزة مسبقًا للتعرُّف على الفواتير والإيصالات وبطاقات العمل. وتوفر الخدمة أيضًا القدرة على تدريب النماذج المخصَّصة. في هذا التمرين، سنركز على تصميم نماذج مخصَّصة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية</h2><a id="user-content-الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية" class="anchor" aria-label="Permalink: الاستعداد لتطوير تطبيق في تعليمة Visual Studio البرمجية" href="#الاستعداد-لتطوير-تطبيق-في-تعليمة-visual-studio-البرمجية"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن دعونا نستخدم SDK للخدمة لتطوير تطبيق باستخدام تعليمة Visual Studio البرمجية. تم توفير ملفات التعليمات البرمجية للتطبيق الخاص بك في مستودع GitHub.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: إذا كنت قد قمت بالفعل باستنساخ مستودع <strong>mslearn-ai-document-intelligence</strong>، فافتحه في تعليمة Visual Studio البرمجية. بخلاف ذلك، اتبع الخطوات التالية لاستنساخه إلى بيئة التطوير الخاصة بك.</p>
</blockquote>
<ol dir="rtl">
<li>
<p dir="rtl">ابدأ تشغيل Visual Studio Code.</p>
</li>
<li>
<p dir="rtl">افتح لوحة (SHIFT+CTRL+P) وشغّل **Git: استنسخ الأمر ** لاستنساخ مستودع <code>https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence</code> إلى مجلد محلي (لا يُهم أي مجلد).</p>
</li>
<li>
<p dir="rtl">عند استنساخ المستودع، افتح المجلد في Visual Studio Code.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا عرضت لك Visual Studio Code رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق <strong>نعم، أثق في خيار الكُتاب</strong> في النافذة المنبثقة.</p>
</blockquote>
</li>
<li>
<p dir="rtl">انتظر حتى تثبيت ملفات إضافية لدعم مشاريع التعليمات البرمجية C# في المستودع.</p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا جرت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <strong>ليس الآن</strong>. إذا تمت مطالبتك برسالة <em>اكتشاف مشروع وظيفة Azure في المجلد</em>، يمكنك إغلاق هذه الرسالة بأمان.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مورد Azure AI Document Intelligence</h2><a id="user-content-إنشاء-مورد-azure-ai-document-intelligence" class="anchor" aria-label="Permalink: إنشاء مورد Azure AI Document Intelligence" href="#إنشاء-مورد-azure-ai-document-intelligence"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لاستخدام خدمة Azure AI Document Intelligence، تحتاج إلى مورد Azure AI Document Intelligence أو Azure AI Services في اشتراك Azure الخاص بك. ستستخدم مدخل Microsoft Azure لإنشاء مورد.</p>
<ol dir="rtl">
<li>في علامة تبويب المستعرض، افتح مدخل Microsoft Azure على <code>https://portal.azure.com</code>، وقم بتسجيل الدخول باستخدام حساب Microsoft المرتبط باشتراكك في Azure.</li>
<li>في الصفحة الرئيسية لمدخل Microsoft Azure، انتقل إلى مربع البحث العلوي واكتب <strong>Document Intelligence</strong>، ثم اضغط على <strong>إدخال</strong>.</li>
<li>في صفحة <strong>Document Intelligence</strong>، حدد <strong>إنشاء</strong>.</li>
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
<li>عند اكتمال النشر، حدد <strong>الانتقال إلى المورد</strong> لعرض صفحة <strong>نظرة عامة</strong> الخاصة بالمورد.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">جمع المستندات للتدريب</h2><a id="user-content-جمع-المستندات-للتدريب" class="anchor" aria-label="Permalink: جمع المستندات للتدريب" href="#جمع-المستندات-للتدريب"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستستخدم نماذج العينة مثل هذا النموذج لتدريب نموذج اختبار:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/Form_1.jpg"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/Form_1.jpg" alt="صورة الفاتورة المستخدمة في هذا المشروع." style="max-width: 100%;"></a></p>
<ol dir="rtl">
<li>
<p dir="rtl">ارجع إلى <strong>تعليمة Visual Studio البرمجية</strong>. في جزء <em>المستكشف</em>، افتح المجلد <strong>Labfiles/02-custom-document-intelligence</strong> وقم بتوسيع المجلد <strong>sample-forms</strong>. لاحظ أن هناك ملفات تنتهي بـ <strong>.json</strong> و <strong>.jpg</strong> في المجلد.</p>
<p dir="rtl">ستستخدم ملفات <strong>.jpg</strong> لتدريب نموذجك.</p>
<p dir="rtl">لقد تم إنشاء ملفات <strong>.json</strong> لك وهي تحتوي على معلومات التسمية. سيتم تحميل الملفات إلى حاوية تخزين الكائنات الثنائية كبيرة الحجم الخاصة بك إلى جانب النماذج.</p>
<p dir="rtl">يمكنك عرض الصور التي نستخدمها في مجلد <em>sample-forms</em> عن طريق تحديدها في تعليمة Visual Studio البرمجية.</p>
</li>
<li>
<p dir="rtl">ارجع إلى <strong>مدخل Microsoft Azure</strong> وانتقِل إلى صفحة <strong>نظرة عامة</strong> في موردك إذا لم تكن هناك بالفعل. ضمن قسم <em>الأساسيات</em>، اعرض <strong>مجموعة الموارد</strong> التي قمت بإنشاء مورد Document Intelligence فيها.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>النظرة العامة</strong> لمجموعة الموارد الخاصة بك، لاحظ <strong>معرف الاشتراك</strong> و<strong>الموقع</strong>. ستحتاج إلى هذه القيم، إلى جانب اسم <strong>مجموعة الموارد</strong> في الخطوات اللاحقة.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/resource_group_variables.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/resource_group_variables.png" alt="مثال على صفحة مجموعة الموارد." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية  في جزء <em>المستكشف</em>، انتقِل إلى المجلد <strong>Labfiles/02-custom-document-intelligence</strong> وقم بتوسيع المجلد <strong>CSharp</strong> أو <strong>Python</strong> حسب تفضيل اللغة لديك. يحتوي كل مجلد على الملفات الخاصة باللغة للتطبيق الذي تريد دمج وظيفة Azure OpenAI فيه.</p>
</li>
<li>
<p dir="rtl">انقر بزر الماوس الأيمن فوق المجلد <strong>CSharp</strong> أو <strong>Python</strong> الذي يحتوي على ملفات التعليمات البرمجية الخاصة بك وحدد <strong>فتح محطة طرفية متكاملة</strong>.</p>
</li>
<li>
<p dir="rtl">في الوحدة الطرفية، شغَّل الأمر التالي لتسجيل الدخول إلى Azure. سيؤدي الأمر <strong>az login</strong> إلى فتح متصفح Microsoft Edge، وتسجيل الدخول بنفس الحساب الذي استخدمته لإنشاء مورد Azure AI Document Intelligence. بمجرد تسجيل الدخول، أغلق نافذة المتصفح.</p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>az login</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az login" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">عد إلى Visual Studio Code. في جزء الوحدة الطرفية، شغَّل الأمر التالي لسرد مواقع Azure.</p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>az account list<span class="pl-k">-</span>locations <span class="pl-k">-</span>o table</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az account list-locations -o table" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">في المخرجات، ابحث عن قيمة <strong>الاسم</strong> التي تتوافق مع موقع مجموعة الموارد الخاصة بك (على سبيل المثال، بالنسبة <em>لشرق الولايات المتحدة</em>، الاسم المقابل هو <em>eastus</em>).</p>
<blockquote>
<p dir="rtl"><strong>مهم</strong>: قم بتسجيل قيمة <strong>الاسم</strong> واستخدمها في الخطوة 11.</p>
</blockquote>
</li>
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية  في المجلد <strong>Labfiles/02-custom-document-intelligence</strong>، حدد <strong>setup.cmd</strong>. ستستخدم هذا البرنامج النصي لتشغيل أوامر واجهة سطر أوامر Azure (CLI) المطلوبة لإنشاء موارد Azure الأخرى التي تحتاجها.</p>
</li>
<li>
<p dir="rtl">في البرنامج النصي <strong>setup.cmd</strong>، راجع الأوامر. سيقوم البرنامج بما يلي:</p>
<ul dir="rtl">
<li>إنشاء حساب تخزين في مجموعة موارد Azure الخاصة بك</li>
<li>تحميل الملفات من مجلد <em>sampleforms</em> المحلي الخاص بك إلى حاوية تسمى <em>sampleforms</em> في حساب التخزين</li>
<li>طباعة معرف URI لـ Shared Access Signature</li>
</ul>
</li>
<li>
<p dir="rtl">قم بتعديل إعلانات المتغيرات <strong>subscription_id</strong>، و<strong>resource_group</strong>، و<strong>location</strong> بالقيم المناسبة للاشتراك ومجموعة الموارد واسم الموقع الذي قمت بنشر مورد Document Intelligence فيه.
ثم <strong>احفظ</strong> التغييرات.</p>
<p dir="rtl">اترك متغير <strong>expiry_date</strong> كما هو بالنسبة للتمرين. يتم استخدام هذا المتغير عند إنشاء معرف URI لـ Shared Access Signature (SAS). في الممارسة العملية، قد ترغب في تحديد تاريخ انتهاء صلاحية مناسب لـ SAS الخاص بك. يمكنك معرفة المزيد عن SAS <a href="https://docs.microsoft.com/azure/storage/common/storage-sas-overview#how-a-shared-access-signature-works" rel="nofollow">هنا</a>.</p>
</li>
<li>
<p dir="rtl">في الوحدة الطرفية لمجلد <strong>Labfiles/02-custom-document-intelligence</strong>، أدخل الأمر التالي لتشغيل البرنامج النصي:</p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-smi">$currentdir</span><span class="pl-k">=</span>(<span class="pl-c1">Get-Item</span> .).FullName
cd ..
.<span class="pl-k">/</span><span class="pl-c1">setup.cmd</span>
cd <span class="pl-smi">$currentdir</span>
</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$currentdir=(Get-Item .).FullName
cd ..
./setup.cmd
cd $currentdir
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">عند اكتمال البرنامج النصي، قم بمراجعة المخرجات المعروضة.</p>
</li>
<li>
<p dir="rtl">في مدخل Microsoft Azure، قم بتحديث مجموعة الموارد الخاصة بك وتأكد من أنها تحتوي على حساب Azure Storage الذي تم إنشاؤه للتو. افتح حساب التخزين، وفي الجزء الموجود على اليسار، حدد <strong>متصفح التخزين</strong>. بعد ذلك في متصفح التخزين، قم بتوسيع <strong>حاويات الكائنات الثنائية كبيرة الحجم</strong> وحدد حاوية <strong>sampleforms</strong> للتحقق من تحميل الملفات من المجلد المحلي <strong>02-custom-document-intelligence/sample-forms</strong>.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تدريب النموذج باستخدام Document Intelligence Studio</h2><a id="user-content-تدريب-النموذج-باستخدام-document-intelligence-studio" class="anchor" aria-label="Permalink: تدريب النموذج باستخدام Document Intelligence Studio" href="#تدريب-النموذج-باستخدام-document-intelligence-studio"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">سنقوم الآن بتدريب النموذج باستخدام الملفات التي قمت بتحميلها إلى حساب التخزين.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في المتصفح، انتقل إلى Document Intelligence Studio في <code>https://documentintelligence.ai.azure.com/studio</code>.</p>
</li>
<li>
<p dir="rtl">مرِّر لأسفل إلى قسم <strong>النماذج المخصَّصة</strong> وحدد تجانب <strong>نموذج الاستخراج المخصَّص</strong>.</p>
</li>
<li>
<p dir="rtl">إذا طلب منك تسجيل الدخول إلى حسابك، فاستخدم بيانات اعتماد Azure.</p>
</li>
<li>
<p dir="rtl">إذا تم سؤالك عن مورد Azure AI Document Intelligence الذي يجب استخدامه، فحدد الاشتراك واسم المورد اللذين استخدمتهما عند إنشاء مورد Azure AI Document Intelligence.</p>
</li>
<li>
<p dir="rtl">ضمن <strong>مشاريعي</strong>، حدد <strong>إنشاء مشروع</strong>. استخدم التكوينات التالية:</p>
<ul dir="rtl">
<li><strong>اسم المشروع</strong>: أدخل اسمًا فريدًا.
<ul dir="rtl">
<li>حدد <em>متابعة</em>.</li>
</ul>
</li>
<li><strong>تكوين مورد الخدمة</strong>: حدد الاشتراك ومجموعة الموارد ومورد document intelligence الذي قمت بإنشائه مسبقًا في هذا الواجب. ضع علامة على المربع <em>تعيين كإعداد افتراضي</em>. الاحتفاظ بإصدار API الافتراضي.
<ul dir="rtl">
<li>حدد <em>متابعة</em>.</li>
</ul>
</li>
<li><strong>ربط مصدر بيانات التدريب</strong>: حدد الاشتراك ومجموعة الموارد وحساب التخزين الذي تم إنشاؤه بواسطة البرنامج النصي للإعداد. ضع علامة على المربع <em>تعيين كإعداد افتراضي</em>. حدد حاوية الكائن الثنائي كبير الحجم <code>sampleforms</code>، واترك مسار المجلد فارغًا.
<ul dir="rtl">
<li>حدد <em>متابعة</em>.</li>
</ul>
</li>
<li>اختر * إنشاء مشروع *</li>
</ul>
</li>
<li>
<p dir="rtl">بمجرد إنشاء مشروعك، في الجزء العلوي الأيسر من الشاشة، حدد <strong>تدريب</strong> لتدريب النموذج الخاص بك. استخدم التكوينات التالية:</p>
<ul dir="rtl">
<li><strong>معرف النموذج</strong>: <em>وفِّر اسمًا فريدًا عالميًا (ستحتاج إلى اسم معرف النموذج في الخطوة التالية)</em>.</li>
<li><strong>وضع الإصدار</strong>: القالب.</li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>الانتقال إلى النماذج</strong>.</p>
</li>
<li>
<p dir="rtl">قد يستغرق التدريب بعض الوقت. سترى إشعارًا عند اكتماله.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">اختبار نموذج Document Intelligence المخصَّص الخاص بك</h2><a id="user-content-اختبار-نموذج-document-intelligence-المخصَّص-الخاص-بك" class="anchor" aria-label="Permalink: اختبار نموذج Document Intelligence المخصَّص الخاص بك" href="#اختبار-نموذج-document-intelligence-المخصَّص-الخاص-بك"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol dir="rtl">
<li>
<p dir="rtl">عد إلى Visual Studio Code. في الوحدة الطرفية، قم بتثبيت حزمة Document Intelligence عن طريق تشغيل الأمر المناسب لتفضيل اللغة الخاص بك:</p>
</li>
<p dir="rtl"><strong>:#C</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>dotnet add package Azure.AI.FormRecognizer <span class="pl-k">--</span>version <span class="pl-c1">4.1</span>.<span class="pl-c1">0</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet add package Azure.AI.FormRecognizer --version 4.1.0" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl">:<strong>Python</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>pip install azure<span class="pl-k">-</span>ai<span class="pl-k">-</span>formrecognizer<span class="pl-k">==</span><span class="pl-c1">3.3</span>.<span class="pl-c1">3</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install azure-ai-formrecognizer==3.3.3" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية في المجلد <strong>Labfiles/02-custom-document-intelligence</strong>، حدد اللغة التي تستخدمها. قم بتعديل ملف التكوين (<strong>appsettings.json</strong> أو <strong>.env</strong>، حسب تفضيل اللغة لديك) بالقيم التالية:</p>
<ul dir="rtl">
<li>نقطة نهاية Document Intelligence الخاصة بك.</li>
<li>مفتاح Document Intelligence الخاص بك.</li>
<li>معرف النموذج الذي تم إنشاؤه قمت بتوفيره عند تدريب النموذج الخاص بك. يمكنك العثور على هذا في صفحة <strong>النماذج</strong> في Document Intelligence Studio. <strong>احفظ</strong> تغييراتك.</li>
</ul>
</li>
<li>
<p dir="rtl">في تعليمة Visual Studio البرمجية، افتح ملف التعليمة البرمجية لتطبيق العميل الخاص بك (<em>Program.cs</em> لـ C#، و<em>test-model.py</em> لـ Python) واستعرض التعليمة البرمجية التي تحتوي عليه، وخاصة أن الصورة الموجودة في عنوان URL تشير إلى الملف الموجود في مستودع GitHub هذا على الويب.</p>
</li>
<li>
<p dir="rtl">قم بإعادة الوحدة الطرفية، وأدخل الأمر التالي لتشغيل البرنامج:</p>
</li>
<p dir="rtl"><strong>#C</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>dotnet build
dotnet run</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="dotnet build
dotnet run" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl"><strong>Python</strong></p>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" dir="auto"><pre>python <span class="pl-c1">test-model</span>.py</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python test-model.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="rtl">قم بعرض المخرجات ولاحظ كيف يوفر مخرج النموذج أسماء الحقول مثل <code>Merchant</code> و<code>CompanyPhoneNumber</code>.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا انتهيت من استخدام مورد Azure، فتذكر حذف المورد في <a href="https://portal.azure.com/?azure-portal=true" rel="nofollow">مدخل Microsoft Azure</a> لتجنب المزيد من الرسوم.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">مزيد من المعلومات</h2><a id="user-content-مزيد-من-المعلومات" class="anchor" aria-label="Permalink: مزيد من المعلومات" href="#مزيد-من-المعلومات"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لمزيد من المعلومات حول خدمة Document Intelligence، راجع <a href="https://learn.microsoft.com/azure/ai-services/document-intelligence/?azure-portal=true" rel="nofollow">مستندات Document Intelligence</a>.</p>
</article></div>
