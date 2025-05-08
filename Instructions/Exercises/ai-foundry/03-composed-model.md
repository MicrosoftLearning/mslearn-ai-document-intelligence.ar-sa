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
  <td><div dir="rtl">إنشاء نموذج تحليل ذكي لمستند مكوّن</div></td>
  <td><div dir="rtl">Module 6 - Document Intelligence</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">إنشاء نموذج تحليل ذكي لمستند مكوّن</h1><a id="user-content-إنشاء-نموذج-تحليل-ذكي-لمستند-مكوّن" class="anchor" aria-label="Permalink: إنشاء نموذج تحليل ذكي لمستند مكوّن" href="#إنشاء-نموذج-تحليل-ذكي-لمستند-مكوّن"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، ستقوم بإنشاء وتدريب نموذجين مخصصين لتحليل نماذج ضريبية مختلفة. بعد ذلك، ستقوم بإنشاء نموذج مكون يتضمن كلا النموذجين المخصصين. ستختبر النموذج عن طريق إرسال نموذج وستتحقق من أنه يتعرف على نوع المستند والحقول المسماة بشكل صحيح.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إعداد الموارد</h2><a id="user-content-إعداد-الموارد" class="anchor" aria-label="Permalink: إعداد الموارد" href="#إعداد-الموارد"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">سنستخدم برنامج نصي لإنشاء مورد التحليل الذكي لمستند الذكاء الاصطناعي في Azure، وحساب تخزين مع نماذج نموذجية، ومجموعة موارد:</p>
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
<p dir="rtl"><strong>ملاحظة</strong>: إذا عرضت لك تعليمة Visual Studio البرمجية رسالة منبثقة لمطالبتك بالثقة في التعليمات البرمجية التي تفتحها، فانقر فوق <strong>نعم، أثق في خيار الكُتاب</strong> في النافذة المنبثقة.</p>
</blockquote>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا تمت مطالبتك بإضافة الأصول المطلوبة للبناء وتصحيح الأخطاء، فحدد <strong>ليس الآن</strong>. إذا كانت هناك أي نوافذ منبثقة أخرى من Visual Studio Code، يمكنك تجاهلها بأمان.</p>
</blockquote>
</li>
<li>
<p dir="rtl">قم بتوسيع مجلد <strong>Labfiles</strong> في الجزء الأيسر، وانقر بزر الماوس الأيمن فوق الدليل <strong>03-composed-model</strong>. حدد خيار الفتح في الوحدة الطرفية المتكاملة، ونفّذ البرنامج النصي التالي:</p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto"><pre>az login <span class="pl-k">--</span>output none</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="az login --output none" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا تلقيتَ خطأ بشأن عدم وجود اشتراكات نشطة وتم تمكين المصادقة متعددة العوامل ( MFA) ، فقد تحتاج إلى تسجيل الدخول إلى مدخل Microsoft Azure في <code>https://portal.azure.com</code> أولاً، ثم إعادة تشغيل <code>az login</code>.</p>
</blockquote>
</li>
<li>
<p dir="rtl">عند المطالبة، قم بتسجيل الدخول إلى اشتراكك في Azure. ثم ارجع إلى Visual Studio Code وانتظر حتى تكتمل عملية تسجيل الدخول.</p>
</li>
<li>
<p dir="rtl">في موجه الوحدة الطرفية المتكاملة، شغّل الأمر التالي لإعداد الموارد:</p>
</li>
<div class="highlight highlight-source-powershell notranslate position-relative overflow-auto" ><pre>.<span class="pl-k">/</span>setup.ps1</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="./setup.ps1" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<blockquote>
<p dir="rtl"><strong>هام</strong>: المورد الأخير الذي تم إنشاؤه بواسطة البرنامج النصي هو خدمة التحليل الذكي لمستند الذكاء الاصطناعي في Azure الخاصة بك. إذا فشل هذا الأمر بسبب وجود مورد من الطبقة F0 لديك بالفعل، فاستخدم هذا المورد لهذا المختبر أو أنشئ مورد يدويًا باستخدام الطبقة S0 في بوابة Azure.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء نموذج مخصص لـ 1040 Forms</h2><a id="user-content-إنشاء-نموذج-مخصص-لـ-1040-forms" class="anchor" aria-label="Permalink: إنشاء نموذج مخصص لـ 1040 Forms" href="#إنشاء-نموذج-مخصص-لـ-1040-forms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لإنشاء نموذج مكون، يجب علينا أولاً إنشاء نموذجين مخصصين أو أكثر. لإنشاء النموذج المخصص الأول:</p>
<ol dir="rtl">
<li>في علامة تبويب مستعرض جديدة، ابدأ تشغيل أداة <strong>Azure AI Document Intelligence Studio</strong> على <code>https://documentintelligence.ai.azure.com/studio</code></li>
<li>مرر لأسفل، ومن ثم ضمن <strong>Custom models</strong>، حدد <strong>Custom extraction model</strong>.</li>
<li>إذا طُلب منك تسجيل الدخول إلى حسابك، فاستخدم بيانات اعتماد Azure لديك.</li>
<li>إذا تم سؤالك عن مورد التحليل الذكي لمستند الذكاء الاصطناعي في Azure لاستخدامه، فحدد اسم الاشتراك والمورد الذي استخدمته عند إنشاء مورد التحليل الذكي لمستند الذكاء الاصطناعي في Azure.</li>
<li>ضمن <strong>My Projects</strong>، حدد <strong>+ Create a project</strong>.</li>
<li>في مربع نص <strong>Project name</strong>، اكتب <strong>1040 Forms</strong>، ثم حدد <strong>Continue</strong>.</li>
<li>في صفحة <strong>Configure service resource</strong>، في القائمة المنسدلة <strong>Subscription</strong>، حدد اشتراك Azure الخاص بك.</li>
<li>في القائمة المنسدلة <strong>Resource group</strong>، حدد <strong>DocumentIntelligenceResources&lt;xxxx&gt;</strong> الذي تم إنشاؤه لك.</li>
<li>في القائمة المنسدلة <strong>ذكاء المستند أو مورد الخدمة المعرفية،</strong> حدد <strong>DocumentIntelligence&lt;xxxx&gt;</strong>.</li>
<li>في القائمة المنسدلة <strong>إصدارAPI،</strong> تأكد من تحديد <strong>(إصدار أولي) 31-07-2024،</strong> ثم حدد <strong>متابعة</strong>.</li>
<li>من صفحة <strong>ربط مصدر بيانات التدريب</strong> في القائمة المنسدلة <strong>الاشتراك</strong>، حدد اشتراك Azure الخاص بك.</li>
<li>في القائمة المنسدلة <strong>مجموعة الموارد</strong>، حدد <strong>DocumentIntelligenceResources&lt;xxxx&gt;</strong>.</li>
<li>في القائمة المنسدلة <strong>Storage account</strong>، حدد حساب التخزين المدرج فقط. إذا كان لديك حسابات تخزين متعددة في اشتراكك، فاختَر الحساب الذي يبدأ بـ <em>docintelstorage</em></li>
<li>في القائمة المنسدلة <strong>Blob container</strong>، حدد <strong>1040examples</strong>، ثم حدد <strong>Continue</strong>.</li>
<li>في الصفحة <strong>Review and create</strong>، حدد <strong>Create project</strong>.</li>
<li>حدد <strong>تشغيل الآن</strong> ضمن قائمة <em>تخطيط التشغيل</em> في النافذة المنبثقة <em>بدء وضع العلامات الآن،</em> وانتظر حتى يكتمل التحليل.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء نموذج مخصص لـ 1040 Forms</h2><a id="user-content-إنشاء-نموذج-مخصص-لـ-1040-forms-1" class="anchor" aria-label="Permalink: إنشاء نموذج مخصص لـ 1040 Forms" href="#إنشاء-نموذج-مخصص-لـ-1040-forms-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن، لنسمي الحقول في نماذج المثال:</p>
<ol dir="rtl">
<li>من صفحة <strong>بيانات الملصق</strong>، في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>FirstName</strong> ثم اضغط على <em>Enter</em>.</li>
<li>حدد المستند المسمى <strong>f1040_1.pdf</strong> في القائمة اليمنى، وحدد <strong>John</strong> ومن ثم حدد <strong>FirstName</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>FirstName</strong> ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>Doe</strong> ثم حدد <strong>LastName</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>أدخل <strong>City</strong>، ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>Los Angeles</strong> ثم حدد <strong>City</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>State</strong>، ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>CA</strong> ثم حدد <strong>State</strong>.</li>
<li>كرر عملية وضع العلامات للنماذج المتبقية في القائمة على اليمين، باستخدام التصنيفات التي قمتَ بإنشائها. قم بتسمية الحقول الأربعة نفسها: <em>FirstName</em> و<em>LastName</em> و<em>City</em> و<em>State</em>. لاحظ أن أحد المستندات لا يحتوي على بيانات المدينة أو الولاية.</li>
</ol>
<blockquote>
<p dir="rtl"><strong>هام</strong> لأغراض هذا التمرين، نستخدم خمسة نماذج فقط ونسمي أربعة حقول فقط. في نماذج العالم الحقيقي الخاصة بك، يجب عليك استخدام أكبر عدد ممكن من العينات لزيادة دقة وثقة تنبؤاتك. يجب أيضاً تسمية كافة الحقول المتوفرة في النماذج، بدلاً من أربعة حقول فقط.</p>
</blockquote>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تدريب نموذج مخصص لـ 1040 Forms</h2><a id="user-content-تدريب-نموذج-مخصص-لـ-1040-forms" class="anchor" aria-label="Permalink: تدريب نموذج مخصص لـ 1040 Forms" href="#تدريب-نموذج-مخصص-لـ-1040-forms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن تمت تسمية نماذج العينة، يمكننا تدريب النموذج المخصص الأول:</p>
<ol dir="rtl">
<li>في استوديو ذكاء المستندات بواسطة الذكاء الاصطناعي في Azure، حدد <strong>تدريب</strong>.</li>
<li>في مربع الحوار <strong>Train a new model</strong>، في مربع النص <strong>Model ID</strong>، اكتب <strong>1040FormsModel</strong>.</li>
<li>في القائمة المنسدلة <strong>Build mode</strong>، حدد <strong>Template</strong>، ثم حدد <strong>Train</strong>.</li>
<li>في مربع الحوار <strong>Training in progress</strong>، حدد <strong>Go to Models</strong>.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء نموذج مخصص لـ 1099 Forms</h2><a id="user-content-إنشاء-نموذج-مخصص-لـ-1099-forms" class="anchor" aria-label="Permalink: إنشاء نموذج مخصص لـ 1099 Forms" href="#إنشاء-نموذج-مخصص-لـ-1099-forms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن، يجب عليك إنشاء نموذج ثانٍ، والذي ستقوم بتدريبه على نماذج الضرائب 1099 المثال:</p>
<ol dir="rtl">
<li>في Azure AI Document Intelligence Studio، حدد <strong>نموذج استخراج مخصص</strong>.</li>
<li>ضمن <strong>My Projects</strong>، حدد <strong>+ Create a project</strong>.</li>
<li>في مربع النص <strong>Project name</strong>، اكتب <strong>1099 Forms</strong>، ثم حدد <strong>Continue</strong>.</li>
<li>في صفحة <strong>Configure service resource</strong>، في القائمة المنسدلة <strong>Subscription</strong>، حدد اشتراك Azure الخاص بك.</li>
<li>في القائمة المنسدلة <strong>مجموعة الموارد</strong>، حدد <strong>DocumentIntelligenceResources&lt;xxxx&gt;</strong>.</li>
<li>في القائمة المنسدلة <strong>ذكاء المستند أو مورد الخدمة المعرفية،</strong> حدد <strong>DocumentIntelligence&lt;xxxx&gt;</strong>.</li>
<li>في القائمة المنسدلة <strong>إصدارAPI،</strong> تأكد من تحديد <strong>(إصدار أولي) 31-07-2024،</strong> ثم حدد <strong>متابعة</strong>.</li>
<li>في الصفحة <strong>ربط مصدر بيانات التدريب</strong> في القائمة المنسدلة <strong>اشتراك</strong>، حدد اشتراك Azure الخاص بك.</li>
<li>في القائمة المنسدلة <strong>مجموعة الموارد</strong>، حدد <strong>DocumentIntelligenceResources&lt;xxxx&gt;</strong>.</li>
<li>في القائمة المنسدلة <strong>Storage account</strong>، حدد حساب التخزين المدرج فقط.</li>
<li>في القائمة المنسدلة <strong>Blob container</strong>، حدد <strong>1099examples</strong>، ثم حدد <strong>Continue</strong>.</li>
<li>في الصفحة <strong>Review and create</strong>، حدد <strong>Create project</strong>.</li>
<li>حدد زر القائمة المنسدلة لـ <strong>تخطيط التشغيل</strong> وحدد <strong>المستندات غير المٌحللة</strong>.</li>
<li>انتظر حتى يكتمل التحليل.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تسمية نموذج مخصص لـ 1099 Forms</h2><a id="user-content-تسمية-نموذج-مخصص-لـ-1099-forms" class="anchor" aria-label="Permalink: تسمية نموذج مخصص لـ 1099 Forms" href="#تسمية-نموذج-مخصص-لـ-1099-forms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن، قم بتسمية نماذج المثال مع بعض الحقول:</p>
<ol dir="rtl">
<li>من صفحة <strong>بيانات الملصق</strong>، في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>FirstName</strong> ثم اضغط على <em>Enter</em>.</li>
<li>حدد المستند المسمى <strong>f1099msc_payer.pdf</strong>، وحدد <strong>John</strong> ومن ثم حدد <strong>FirstName</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>FirstName</strong> ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>Doe</strong> ثم حدد <strong>LastName</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>أدخل <strong>City</strong>، ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>New Haven</strong> ثم حدد <strong>City</strong>.</li>
<li>في أعلى يسار الصفحة، حدد <strong>+ إضافة حقل</strong>، ثم حدد <strong>حقل</strong>.</li>
<li>اكتب <strong>State</strong>، ثم اضغط على <em>Enter</em>.</li>
<li>في المستند، حدد <strong>CT</strong> ثم حدد <strong>State</strong>.</li>
<li>كرر عملية وضع العلامات للنماذج المتبقية في القائمة على اليسار. قم بتسمية الحقول الأربعة نفسها: <em>FirstName</em> و<em>LastName</em> و<em>City</em> و<em>State</em>. لاحظ أن مستندين من المستندات لا يحتويان على أي بيانات اسم للتسمية.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تدريب نموذج مخصص لـ 1099 Forms</h2><a id="user-content-تدريب-نموذج-مخصص-لـ-1099-forms" class="anchor" aria-label="Permalink: تدريب نموذج مخصص لـ 1099 Forms" href="#تدريب-نموذج-مخصص-لـ-1099-forms"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">يمكنك الآن تدريب النموذج المخصص الثاني:</p>
<ol dir="rtl">
<li>في استوديو ذكاء المستندات بواسطة الذكاء الاصطناعي في Azure، حدد <strong>تدريب</strong>.</li>
<li>في مربع الحوار <strong>Train a new model</strong>، في مربع النص <strong>Model ID</strong>، اكتب <strong>1099FormsModel</strong>.</li>
<li>في القائمة المنسدلة <strong>Build mode</strong>، حدد <strong>Template</strong>، ثم حدد <strong>Train</strong>.</li>
<li>في مربع الحوار <strong>Training in progress</strong>، حدد <strong>Go to Models</strong>.</li>
<li>قد تستغرق عملية التدريب بضع دقائق. قم بتحديث المستعرض أحياناً حتى يعرض كلا النموذجين الحالة <strong>الناجحة</strong>.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدام النموذج</h2><a id="user-content-استخدام-النموذج" class="anchor" aria-label="Permalink: استخدام النموذج" href="#استخدام-النموذج"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد اكتمال النموذج، دعنا نختبره باستخدام نموذج مثال:</p>
<ol dir="rtl">
<li>في استوديو ذكاء المستندات بواسطة الذكاء الاصطناعي في Azure، حدد صفحة<strong>النماذج</strong>، ثم حدد <strong>1040FormsModel</strong>.</li>
<li>حدد <strong>اختبار</strong>.</li>
<li>حدد <strong>استعراض الملفات</strong> ثم قم بالاستعراض وصولاً إلى الموقع الذي نسخت المستودع فيه.</li>
<li>حدد <strong>03-composed-model/trainingdata/TestDoc/f1040_7.pdf</strong>، ومن ثم حدد <strong>Open</strong>.</li>
<li>حدد <strong>تشغيل التحليل</strong>. يقوم التحليل الذكي لمستند الذكاء الاصطناعي في Azure بتحليل النموذج باستخدام النموذج الذي تم إنشاؤه.</li>
<li>المستند الذي قمت بتحليله هو مثال على نموذج ضريبة 1040. تحقق من خاصية <strong>DocType</strong> لمعرفة ما إذا كان قد تم استخدام النموذج المخصص الصحيح. تحقق أيضاً من القيم <strong>FirstName</strong> و<strong>LastName</strong> و<strong>City</strong> و<strong>State</strong> التي يحددها النموذج.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف الموارد</h2><a id="user-content-تنظيف-الموارد" class="anchor" aria-label="Permalink: تنظيف الموارد" href="#تنظيف-الموارد"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن رأيت كيفية عمل النماذج المكونة، دعنا نزيل الموارد التي أنشأتها في اشتراك Azure الخاص بك.</p>
<ol dir="rtl">
<li>في مدخل <strong>Azure</strong> على <code>https://portal.azure.com/</code>، حدد <strong>Resource groups</strong>.</li>
<li>في قائمة <strong>مجموعات الموارد</strong> حدد <strong>DocumentIntelligenceResources&lt;xxxx&gt;</strong> الذي قمتَ بإنشائه، ثم حدد <strong>Delete resource group</strong>.</li>
<li>في مربع النص <strong>كتابة اسم مجموعة الموارد</strong>، اكتب اسم مجموعة الموارد، ثم حدد <strong>حذف</strong> لحذف مورد "التحليل الذكي للمستند" وحساب التخزين.</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">معرفة المزيد</h2><a id="user-content-معرفة-المزيد" class="anchor" aria-label="Permalink: معرفة المزيد" href="#معرفة-المزيد"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="rtl">
<li><a href="/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/OLPRODLOC/azure/ai-services/document-intelligence/concept-composed-models">إنشاء نماذج مخصصة</a></li>
</ul>
</article></div>
