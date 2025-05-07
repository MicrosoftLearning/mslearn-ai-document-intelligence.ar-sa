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
  <td><div dir="rtl">تحليل المحتوى باستخدام Azure AI Content Understanding</div></td>
  <td><div dir="rtl">Multimodal analysis with Content Understanding</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table></markdown-accessiblity-table>

<div class="markdown-heading" dir="rtl"><h1 tabindex="-1" class="heading-element" dir="rtl">تحليل المحتوى باستخدام Azure AI Content Understanding</h1><a id="user-content-تحليل-المحتوى-باستخدام-azure-ai-content-understanding" class="anchor" aria-label="Permalink: تحليل المحتوى باستخدام Azure AI Content Understanding" href="#تحليل-المحتوى-باستخدام-azure-ai-content-understanding"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">في هذا التمرين، يمكنك استخدام مدخل Azure AI Foundry لإنشاء مشروع فهم المحتوى الذي يمكنه استخراج المعلومات من نماذج سياسة التأمين على السفر. ثم ستختبر محلل محتواك في مدخل Azure AI Foundry وتستخدمه من خلال واجهة Content Understanding REST.</p>
<p dir="rtl">سيستغرق هذا التدريب حوالي <strong>30</strong> دقيقة.</p>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء مشروع "فهم المحتوى"</h2><a id="user-content-إنشاء-مشروع-فهم-المحتوى" class="anchor" aria-label="Permalink: إنشاء مشروع &quot;فهم المحتوى&quot;" href="#إنشاء-مشروع-فهم-المحتوى"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">لنبدأ باستخدام مدخل Azure AI Foundry لإنشاء مشروع "فهم المحتوى".</p>
<ol dir="rtl">
<li>
<p dir="rtl">في متصفح الويب، افتح <a href="https://ai.azure.com" rel="nofollow">مدخل Azure AI Foundry</a> على <code>https://ai.azure.com</code> وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك.</p>
<p dir="rtl">تبدو الصفحة الرئيسية لمدخل Azure AI Foundry مشابهة للصورة التالية:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/ai-foundry-portal.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/ai-foundry-portal.png" alt="لقطة شاشة لمدخل Azure AI Foundry." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في قسم <strong>العثور عليه بسرعة</strong> من الصفحة الرئيسية، نحو الأسفل، حدد <strong>فهم المحتوى</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>فهم المحتوى</strong>، حدد زر <strong>إنشاء مشروع "فهم محتوى" جديد</strong>.</p>
</li>
<li>
<p dir="rtl">في خطوة <strong>نظرة عامة على المشروع</strong>، اضبط الخصائص التالية لمشروعك؛ ثم حدد <strong>التالي</strong>:</p>
<ul dir="rtl">
<li><strong>اسم المشروع</strong>: <code>travel-insurance</code></li>
<li><strong>الوصف</strong>: <code>Insurance policy data extraction</code></li>
<li><strong>المركز</strong>: إنشاء مركز جديد</li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>إنشاء مركز</strong>، اضبط الخصائص التالية ثم حدد <strong>التالي</strong>:</p>
<ul dir="rtl">
<li><strong>مورد مركز الذكاء الاصطناعي في Azure</strong>: <code>content-understanding-hub</code></li>
<li><strong>اشتراك Azure</strong>: <em>حدد اشتراكك Azure</em></li>
<li><strong>مجموعة الموارد</strong>: <em>إنشاء مجموعة موارد جديدة باسم مناسب</em></li>
<li><strong>الموقع</strong>: <em>حدد أي موقع متاح</em></li>
<li><strong>خدمات الذكاء الاصطناعي في Azure</strong>: <em>إنشاء مورد جديد لخدمات الذكاء الاصطناعي في Azure باسم مناسب</em></li>
</ul>
</li>
<li>
<p dir="rtl">في خطوة <strong>إعدادات التخزين</strong>، حدّد حساب تخزين مركز الذكاء الاصطناعي جديدًا وحدد <strong>التالي</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>المراجعة</strong>، حدّد <strong>إنشاء مشروع</strong>. ثم انتظر حتى يتم إنشاء المشروع والموارد المرتبطة به.</p>
<p dir="rtl">عندما يكون المشروع جاهزًا، سيتم فتحه في صفحة <strong>تعريف المخطط</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/content-understanding-project.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/content-understanding-project.png" alt="لقطة شاشة لمشروع &quot;فهم المحتوى&quot; الجديد." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">مراجعة موارد Azure</h2><a id="user-content-مراجعة-موارد-azure" class="anchor" aria-label="Permalink: مراجعة موارد Azure" href="#مراجعة-موارد-azure"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">عند إنشاء مركز الذكاء الاصطناعي والمشروع، تم إنشاء موارد مختلفة في اشتراك Azure الخاص بك لدعم المشروع.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في علامة تبويب المتصفح الجديدة، افتح <a href="https://portal.azure.com" rel="nofollow">بوابة Azure</a> على <code>https://portal.azure.com</code>؛ وسجّل الدخول باستخدام بيانات اعتماد Azure الخاصة بك.</p>
</li>
<li>
<p dir="rtl">انتقل إلى مجموعة الموارد التي قمت بإنشائها لمركزك، ولاحظ موارد Azure التي تم إنشاؤها.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/azure-resources.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/azure-resources.png" alt="لقطة شاشة لموارد Azure." style="max-width: 100%;"></a></p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تعريف مخطط مخصص</h2><a id="user-content-تعريف-مخطط-مخصص" class="anchor" aria-label="Permalink: تعريف مخطط مخصص" href="#تعريف-مخطط-مخصص"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">ستقوم ببناء محلل يمكنه استخراج المعلومات من نماذج التأمين على السفر. ستبدأ بتعريف مخطط استنادًا إلى نموذج عينة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">قم بتنزيل نموذج العينة <a href="https://github.com/microsoftlearning/mslearn-ai-document-intelligence/raw/main/Labfiles/05-content-understanding/forms/train-form.pdf">train-form.pdf</a> من <code>https://github.com/microsoftlearning/mslearn-ai-document-intelligence/raw/main/Labfiles/05-content-understanding/forms/train-form.pdf</code> واحفظه في مجلد محلي.</p>
</li>
<li>
<p dir="rtl">ارجع إلى علامة تبويب المتصفح التي تحتوي على مشروع "فهم المحتوى" الخاص بك، وفي صفحة <strong>تعريف المخطط</strong>، قم بتحميل الملف <strong>train-form.pdf</strong> الذي قمت بتنزيله للتو.</p>
</li>
<li>
<p dir="rtl">حدد قالب <strong>تحليل المستند</strong>، ثم حدد <strong>إنشاء</strong>.</p>
<p dir="rtl">يوفر محرر المخطط طريقة لتحديد حقول البيانات التي سيتم استخراجها من النموذج، والذي يظهر على اليمين. يبدو النموذج بهذا الشكل:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/train-form.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/train-form.png" alt="لقطة شاشة لنموذج التأمين." style="max-width: 100%;"></a></p>
<p dir="rtl">تتكون حقول البيانات في النموذج من:</p>
<ul dir="rtl">
<li>مجموعة من التفاصيل الشخصية المتعلقة بحامل الوثيقة.</li>
<li>مجموعة من التفاصيل المتعلقة بالرحلة التي يلزم تأمينها.</li>
<li>توقيع وتاريخ</li>
</ul>
<p dir="rtl">سنبدأ بإضافة حقل يمثل التفاصيل الشخصية كجدول، والذي سنحدد فيه بعد ذلك حقولًا فرعية للتفاصيل الفردية.</p>
</li>
<li>
<p dir="rtl">حدد <strong>+ إضافة حقل جديد</strong> وأنشئ حقل جديد بالقيم التالية:</p>
<ul dir="rtl">
<li><strong>اسم الحقل</strong>: <code>PersonalDetails</code></li>
<li><strong>وصف الحقل</strong>: <code>Policyholder information</code></li>
<li><strong>نوع القيمة</strong>: جدول</li>
</ul>
</li>
<li>
<p dir="rtl">حدد <strong>حفظ التغييرات</strong> (✔) ولاحظ أنه سيتم إنشاء حقل فرعي جديد تلقائيًا.</p>
</li>
<li>
<p dir="rtl">تكوين الحقل الفرعي الجديد بالقيم التالية:</p>
<ul dir="rtl">
<li><strong>اسم الحقل</strong>: <code>PolicyholderName</code></li>
<li><strong>وصف الحقل</strong>: <code>Policyholder name</code></li>
<li><strong>نوع القيمة</strong>: سلسلة</li>
<li><strong>الأسلوب</strong>: استخراج</li>
</ul>
</li>
<li>
<p dir="rtl">استخدم الزر <strong>+ إضافة حقل فرعي جديد</strong> لإضافة الحقول الفرعية الإضافية التالية:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الحقل</th>
<th>وصف الحقل</th>
<th>نوع القيمة</th>
<th>الأسلوب</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>StreetAddress</code></td>
<td><code>Policyholder address</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>City</code></td>
<td><code>Policyholder city</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>PostalCode</code></td>
<td><code>Policyholder post code</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>CountryRegion</code></td>
<td><code>Policyholder country or region</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>DateOfBirth</code></td>
<td><code>Policyholder birth date</code></td>
<td>التاريخ</td>
<td>الاستخراج</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">عند الانتهاء من إضافة كافة الحقول الفرعية للتفاصيل الشخصية، استخدم زر <strong>الرجوع</strong> للعودة إلى المستوى الأعلى من المخطط.</p>
</li>
<li>
<p dir="rtl">أضف حقل <em>جدول</em> جديد باسم <strong><code>TripDetails</code></strong> لتمثيل تفاصيل الرحلة المؤمنة. ثم أضف إليه الحقول الفرعية التالية:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الحقل</th>
<th>وصف الحقل</th>
<th>نوع القيمة</th>
<th>الأسلوب</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>DestinationCity</code></td>
<td><code>Trip city</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>DestinationCountry</code></td>
<td><code>Trip country or region</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>DepartureDate</code></td>
<td><code>Date of departure</code></td>
<td>التاريخ</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>ReturnDate</code></td>
<td><code>Date of return</code></td>
<td>التاريخ</td>
<td>الاستخراج</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">ارجع إلى المستوى الأعلى للمخطط وأضف الحقلين الفرديين التاليين:</p>
<markdown-accessiblity-table data-catalyst=""><table>
<thead>
<tr>
<th>اسم الحقل</th>
<th>وصف الحقل</th>
<th>نوع القيمة</th>
<th>الأسلوب</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Signature</code></td>
<td><code>Policyholder signature</code></td>
<td>السلسلة‬</td>
<td>الاستخراج</td>
</tr>
<tr>
<td><code>Date</code></td>
<td><code>Date of signature</code></td>
<td>التاريخ</td>
<td>الاستخراج</td>
</tr>
</tbody>
</table></markdown-accessiblity-table>
</li>
<li>
<p dir="rtl">تحقق من أن المخطط المكتمل يبدو كما يلي، ثم احفظه.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/completed-schema.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/completed-schema.png" alt="لقطة شاشة لمخطط المستند." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في صفحة <strong>محلل الاختبار</strong>، إذا لم يبدأ التحليل تلقائيًا، فحدد <strong>تشغيل التحليل</strong>. ثم انتظر حتى اكتمال التحليل وراجع قيم النص في النموذج التي تم تحديدها على أنها تطابق الحقول في المخطط.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/test-analyzer.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/test-analyzer.png" alt="لقطة شاشة لنتائج اختبار المحلل." style="max-width: 100%;"></a></p>
<p dir="rtl">يجب أن تكون خدمة "فهم المحتوى" قد حددت بشكل صحيح النص الذي يتوافق مع الحقول الموجودة في المخطط. إذا لم يتم ذلك، فيمكنك استخدام صفحة <strong>بيانات الوصف</strong> لتحميل نموذج عينة آخر وتحديد النص الصحيح لكل حقل بشكل صريح.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">إنشاء محلل واختباره</h2><a id="user-content-إنشاء-محلل-واختباره" class="anchor" aria-label="Permalink: إنشاء محلل واختباره" href="#إنشاء-محلل-واختباره"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن قمت بتدريب نموذج لاستخراج الحقول من نماذج التأمين، يمكنك إنشاء محلل لاستخدامه مع نماذج مماثلة.</p>
<ol dir="rtl">
<li>
<p dir="rtl">في جزء التنقل الموجود على اليسار، حدد صفحة <strong>إنشاء محلل</strong>.</p>
</li>
<li>
<p dir="rtl">حدد <strong>+ إنشاء محلل</strong> وأنشئ محللًا جديدًا بالخصائص التالية (مكتوب بالضبط كما هو موضح هنا):</p>
<ul dir="rtl">
<li><strong>الاسم:</strong> <code>travel-insurance-analyzer</code></li>
<li><strong>الوصف</strong>: <code>Insurance form analyzer</code></li>
</ul>
</li>
<li>
<p dir="rtl">انتظر حتى يصبح المحلل الجديد جاهزًا (استخدم زر <strong>تحديث</strong> للتحقق).</p>
</li>
<li>
<p dir="rtl">قم بتنزيل <a href="https://github.com/microsoftlearning/mslearn-ai-document-intelligence/raw/main/Labfiles/05-content-understanding/forms/test-form.pdf">test-form.pdf</a> من <code>https://github.com/microsoftlearning/mslearn-ai-document-intelligence/raw/main/Labfiles/05-content-understanding/forms/test-form.pdf</code> واحفظه في مجلد محلي.</p>
</li>
<li>
<p dir="rtl">ارجع إلى صفحة <strong>إنشاء محلل</strong> وحدد رابط <strong>محلل تأمين السفر</strong>. سيتم عرض الحقول المحددة في مخطط المحلل.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>محلل تأمين السفر</strong>، حدد <strong>اختبار</strong>.</p>
</li>
<li>
<p dir="rtl">استخدم الزر <strong>+ تحميل ملفات الاختبار</strong> لتحميل <strong>test-form.pdf</strong> وتشغيل التحليل لاستخراج بيانات الحقل من نموذج الاختبار.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/test-form-results.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/test-form-results.png" alt="لقطة شاشة لنتائج تحليل نموذج الاختبار." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">اعرض علامة التبويب <strong>النتيجة</strong> لرؤية النتائج بتنسيق JSON التي أعادها المحلل. في المهمة التالية، ستستخدم واجهة برمجة تطبيقات Content Understanding REST لإرسال نموذج إلى المحلل الخاص بك وإرجاع النتائج بهذا التنسيق.</p>
</li>
<li>
<p dir="rtl">أغلق صفحة <strong>محلل-تأمين-السفر</strong>.</p>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">استخدم واجهة برمجة تطبيقات Content Understanding REST</h2><a id="user-content-استخدم-واجهة-برمجة-تطبيقات-content-understanding-rest" class="anchor" aria-label="Permalink: استخدم واجهة برمجة تطبيقات Content Understanding REST" href="#استخدم-واجهة-برمجة-تطبيقات-content-understanding-rest"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">الآن بعد أن قمت بإنشاء محلل، يمكنك استخدامه من خلال تطبيق عميل عبر واجهة برمجة تطبيقات Content Understanding REST.</p>
<ol dir="rtl">
<li>
<p dir="rtl">انتقل إلى علامة تبويب المتصفح التي تحتوي على بوابة Azure (أو افتح <code>https://portal.azure.com</code> في علامة تبويب جديدة إذا قمت بإغلاقها).</p>
</li>
<li>
<p dir="rtl">في مجموعة الموارد الخاصة بمركز فهم المحتوى الخاص بك، افتح مورد <strong>خدمات الذكاء الاصطناعي في Azure</strong>.</p>
</li>
<li>
<p dir="rtl">في صفحة <strong>نظرة عامة</strong>، في قسم <strong>المفاتيح ونقطة النهاية</strong>، اعرض علامة التبويب <strong>فهم المحتوى</strong>.</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/keys-and-endpoint.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/keys-and-endpoint.png" alt="لقطة شاشة للمفاتيح ونقطة النهاية لـ &quot;فهم المحتوى&quot;." style="max-width: 100%;"></a></p>
<p dir="rtl">ستحتاج إلى نقطة نهاية "فهم المحتوى" وأحد المفاتيح للاتصال بالمحلل الخاص بك من خلال تطبيق العميل.</p>
</li>
<li>
<p dir="rtl">استخدم الزر <strong>[&gt;_]</strong> الموجود على يمين شريط البحث أعلى الصفحة لإنشاء Cloud Shell جديد في بوابة Azure، وتحديد بيئة <em><strong>PowerShell</strong></em>. يوفر shell السحابي واجهة سطر أوامر في جزء أسفل مدخل Microsoft Azure، كما هو موضح هنا:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/cloud-shell.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/cloud-shell.png" alt="لقطة شاشة لبوابة Azure مع جزء Cloud Shell." style="max-width: 100%;"></a></p>
<blockquote>
<p dir="rtl"><strong>ملاحظة</strong>: إذا كنت قد أنشأت مسبقًا Cloud Shell يستخدم بيئة <em>معالج Bash</em>، فبدّل إلى <em><strong>PowerShell</strong></em>.</p>
</blockquote>
</li>
<li>
<p dir="rtl">لاحظ أنه يمكنك تغيير حجم Cloud Shell عن طريق سحب شريط الفاصل في أعلى الجزء، أو عن طريق استخدام الرموز <strong>—</strong> و <strong>◻</strong> و<strong>X</strong> في أعلى يمين الجزء للتصغير والتكبير وإغلاق الجزء. لمزيد من المعلومات حول استخدام Azure Cloud Shell، راجع <a href="https://docs.microsoft.com/azure/cloud-shell/overview" rel="nofollow">وثائق Azure Cloud Shell</a>.</p>
</li>
<li>
<p dir="rtl">في شريط أدوات Cloud Shell، في قائمة <strong>الإعدادات</strong>، حدد <strong>الانتقال إلى الإصدار الكلاسيكي</strong> (هذا مطلوب لاستخدام محرر التعليمات البرمجية).</p>
</li>
<li>
<p dir="rtl">في جزء PowerShell، أدخل الأوامر التالية لاستنساخ مستودع GitHub لهذا التمرين:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>rm -r mslearn-ai-doc -f
git clone https://github.com/microsoftlearning/mslearn-ai-document-intelligence mslearn-ai-doc
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="rm -r mslearn-ai-doc -f
git clone https://github.com/microsoftlearning/mslearn-ai-document-intelligence mslearn-ai-doc" tabindex="0" role="button">
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
<p dir="rtl">بعد استنساخ المستودع، انتقل إلى المجلد <strong>mslearn-ai-doc/Labfiles/05-content-understanding/code</strong>:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>cd mslearn-ai-doc/Labfiles/05-content-understanding/code
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd mslearn-ai-doc/Labfiles/05-content-understanding/code" tabindex="0" role="button">
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
<p dir="rtl">أدخل الأمر التالي لتحرير ملف التعليمات البرمجية <strong>analyze_doc.py</strong> لـ Python الذي تم توفيره:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>code analyze_doc.py
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="code analyze_doc.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="rtl">يتم فتح ملف التعليمات البرمجية Python في محرر التعليمات البرمجية:</p>
<p dir="rtl"><a target="_blank" rel="noopener noreferrer" href="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/code-editor.png"><img src="https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence.ar-sa/blob/main/Instructions/media/code-editor.png" alt="لقطة شاشة لمحرر التعليمات البرمجية مع تعليمات Python البرمجية." style="max-width: 100%;"></a></p>
</li>
<li>
<p dir="rtl">في ملف التعليمات البرمجية، استبدل العنصر النائب <strong>&lt;CONTENT_UNDERSTANDING_ENDPOINT&gt;</strong> بنقطة نهاية "فهم المحتوى" لديك، والعنصر النائب <strong>&lt;CONTENT_UNDERSTANDING_KEY&gt;</strong> بأحد المفاتيح لمورد خدمات الذكاء الاصطناعي في Azure لديك.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: ستحتاج إلى تغيير حجم نافذة Cloud Shell أو تصغيرها لنسخ نقطة النهاية والمفتاح من صفحة موارد خدمات الذكاء الاصطناعي في Azure في بوابة Azure - احرص على عدم <em>إغلاق</em> Cloud Shell (أو ستحتاج إلى تكرار الخطوات المذكورة أعلاه)</p>
</blockquote>
</li>
<li>
<p dir="rtl">بعد استبدال العناصر النائبة، استخدم الأمر <strong>CTRL+S</strong> لحفظ التغييرات ثم مراجعة التعليمات البرمجية المكتملة، والتي:</p>
<ul dir="rtl">
<li>jرسل طلب HTTP POST إلى نقطة نهاية "فهم المحتوى" لديك، مما يعطي تعليمات لـ <strong>محلل-تأمين-السفر</strong> بتحليل نموذج استنادًا إلى عنوان URL الخاص به.</li>
<li>يتحقق من الاستجابة لعملية POST لاسترداد مُعرّف لعملية التحليل.</li>
<li>ترسل طلب HTTP GET بشكل متكرر إلى خدمة Content Understanding حتى تتوقف العملية عن التشغيل.</li>
<li>إذا نجحت العملية، يتم عرض استجابة JSON.</li>
</ul>
</li>
<li>
<p dir="rtl">استخدم الأمر <strong>CTRL+Q</strong> لإغلاق محرر التعليمات البرمجية مع إبقاء سطر أوامر Cloud Shell مفتوحًا.</p>
</li>
<li>
<p dir="rtl">في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتثبيت مكتبة <strong>الطلبات</strong> الخاصة بـ Python (التي تستخدم في التعليمات البرمجية):</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>pip install requests
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install requests" tabindex="0" role="button">
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
<p dir="rtl">بعد تثبيت المكتبة، في جزء سطر أوامر Cloud Shell، أدخل الأمر التالي لتشغيل التعليمات البرمجية لـ Python:</p>
</li>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>python analyze_doc.py
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python analyze_doc.py" tabindex="0" role="button">
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
<p dir="rtl">راجع مخرجات البرنامج، والتي تتضمن نتائج JSON لتحليل المستندات.</p>
<blockquote>
<p dir="rtl"><strong>تلميح</strong>: قد لا يكون المخزن المؤقت للشاشة في وحدة تحكم Cloud Shell كبيرًا بما يكفي لإظهار الناتج بأكمله. إذا كنت ترغب في مراجعة الناتج بأكمله، فشغّل البرنامج باستخدام الأمر <code>python analyze_doc.py &gt; output.txt</code>. بعد ذلك، عند انتهاء البرنامج، استخدم الأمر <code>code output.txt</code> لفتح الناتج في محرر التعليمات البرمجية.</p>
</blockquote>
</li>
</ol>
<div class="markdown-heading" dir="rtl"><h2 tabindex="-1" class="heading-element" dir="rtl">تنظيف</h2><a id="user-content-تنظيف" class="anchor" aria-label="Permalink: تنظيف" href="#تنظيف"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="rtl">إذا انتهيت من العمل باستخدام خدمة "فهم المحتوى"، فيجب عليك حذف الموارد التي قمت بإنشائها في هذا التمرين لتجنب تكبد تكاليف Azure غير الضرورية.</p>
<ol dir="rtl">
<li>في مدخل Azure AI Foundry، انتقل إلى مشروع <strong>تأمين-السفر</strong> واحذفه.</li>
<li>في بوابة Azure، انتقل إلى مجموعة الموارد التي أنشأتها لهذه التدريبات.</li>
</ol>
</article></div>
