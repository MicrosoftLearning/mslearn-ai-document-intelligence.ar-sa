---
title: تمارين التحليل الذكي لمستند الذكاء الاصطناعي في Azure
permalink: index.html
layout: home
---

تم تصميم التمارين التالية لتزويدك بتجربة تعليمية عملية تستكشف فيها المهام الشائعة التي يقوم بها المطورون عند بناء حلول ذكاء المستندات على Microsoft Azure.

> **ملاحظة**: لاستكمال التمارين، ستحتاج إلى اشتراك Azure الذي تتمتع فيه بالأذونات والحصة الكافية لتوفير موارد Azure الضرورية. إذا لم يكن لديك حسابًا مسبقًا، فيمكنك التسجيل للحصول على [حساب Azure](https://azure.microsoft.com/free). هناك خيار تجريبي مجاني للمستخدمين الجدد يتضمن رصيدًا لأول 30 يومًا.

## التدريبات

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %} {% for activity in labs  %} {% if activity.url contains 'ai-foundry' %} {% continue %} {% endif %}
<hr>
### [{{activity.lab.title}}]({{ site.github.url }}{{ activity.url }})

{{activity.lab.description}}

{% endfor %}

> **ملاحظة**: على الرغم من أنه يمكنك إكمال هذه التدريبات بمفردها، إلا أنها مصممة لاستكمال الوحدات الموجودة على [Microsoft Learn](https://learn.microsoft.com/training/paths/extract-data-from-forms-document-intelligence/)؛ حيث ستجد تعمقًا في بعض المفاهيم الأساسية التي تستند إليها هذه التدريبات.
