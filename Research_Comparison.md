# Assignment 2: Library vs. Framework

**Student:** Eng. Dhafer Alyaari  
**Topic:** A comparison using CSS, JavaScript, Java, PHP, and Python  
**Research references checked:** 6 November 2026

## 1. Definitions | التعريفات

**Library — المكتبة:** مجموعة من الأدوات أو الوظائف أو الوحدات البرمجية القابلة لإعادة الاستخدام، يستدعيها البرنامج لأداء مهمة محددة. غالبًا يكون تطبيقك هو الذي يحدد متى وأين يستخدمها.

**Framework — إطار العمل:** مجموعة من القواعد والمكونات والبنية العامة التي تساعد على بناء نوع معين من التطبيقات. غالبًا ما ينظم إطار العمل تدفق التنفيذ ويوفر نقاطًا تضيف فيها منطق برنامجك.

**Inversion of Control — عكس التحكم:** في الاستخدام المعتاد للمكتبات، برنامجك يستدعي دوال المكتبة. في كثير من أطر العمل، إطار العمل هو الذي يستدعي كودك عند وقوع حدث معين. هذا فرق أساسي أوضحه Martin Fowler في مقاله عن Inversion of Control.  
Source: [Martin Fowler — Inversion of Control](https://martinfowler.com/bliki/InversionOfControl.html)

## 2. Key differences | الفروق الأساسية

| Aspect | Library — مكتبة | Framework — إطار عمل |
|---|---|---|
| Purpose / الهدف | Solves a specific problem / تحل مهمة محددة | Provides an application structure / يوفر هيكلًا لتطبيق |
| Control / التحكم | Your program usually calls it / برنامجك يستدعيها | Often invokes your code / غالبًا يستدعي كودك |
| Structure / البنية | Does not normally require a full project layout / لا تفرض غالبًا هيكل مشروع كامل | Often recommends or enforces conventions / يحدد عادة تنظيمًا وقواعد للمشروع |
| Usage / الاستخدام | Add a needed feature / تضيف وظيفة محددة | Build an application following a shared pattern / تبني تطبيقًا وفق نمط عام |
| Relationship / العلاقة | Can be used inside a framework / قد تُستخدم داخل إطار عمل | Can include and depend on libraries / قد يحتوي على مكتبات |

**Important clarification:** These are typical differences, not absolute rules. Some frameworks are flexible and some libraries provide broad capabilities. **Size alone is not a reliable definition.**  
**توضيح:** الفروق عامة وليست قواعد مطلقة، ولا يصح التفريق بينهما بالاعتماد على الحجم فقط.

## 3. Examples in five technologies | أمثلة من خمس تقنيات

### CSS

- **Library: [Animate.css](https://animate.style/)** — Ready-made CSS animations / مكتبة لتأثيرات الحركة الجاهزة.
- **Framework: [Bootstrap 5](https://getbootstrap.com/docs/5.3/getting-started/introduction/)** — A responsive UI framework with layout and component conventions / إطار لتصميم الواجهات المتجاوبة.

**Note:** CSS does not have application execution flow in the same sense as Java or Python. Calling Bootstrap a CSS framework describes its UI structure and component system, not a runtime Inversion of Control.

### JavaScript

- **Library: [Lodash](https://lodash.com/)** — Helper functions for working with arrays, objects, and values / أدوات للتعامل مع المصفوفات والكائنات والقيم.
- **Framework: [Angular](https://angular.dev/overview)** — Framework for web applications with components and application architecture / إطار لبناء تطبيقات الويب.

### Java

- **Library: [Apache Commons Lang](https://commons.apache.org/proper/commons-lang/)** — Utility methods extending Java's core capabilities / أدوات إضافية للتعامل مع النصوص والقيم وغيرها.
- **Framework: [Spring Framework](https://spring.io/projects/spring-framework/)** — Infrastructure and programming model for Java applications / إطار يوفر بنية ومكونات لبناء تطبيقات Java.

### PHP

- **Library: [Guzzle](https://docs.guzzlephp.org/)** — HTTP client used to send requests / مكتبة لإرسال طلبات HTTP.
- **Framework: [Laravel](https://laravel.com/docs)** — Web application framework with routing, database tools, and conventions / إطار لتطبيقات الويب يتضمن المسارات وقواعد البيانات.

### Python

- **Library: [Requests](https://docs.python-requests.org/en/latest/)** — A simple HTTP request library / مكتبة لإرسال طلبات HTTP.
- **Framework: [Django](https://www.djangoproject.com/)** — A web framework with routing, views, and application structure / إطار لبناء تطبيقات الويب.

## 4. A practical example | مثال عملي

Imagine that you need to retrieve a web page using Python:

```python
import requests
response = requests.get("https://example.com")
```

Here, **your code chooses when to call `requests.get()`**. That is typical library usage.

In a Django application, you write a view and connect it to a URL route. When the correct request arrives, **Django calls that view for you**. That demonstrates the common framework pattern.

Original reference: [Django — Django at a glance](https://docs.djangoproject.com/en/5.2/intro/overview/).

## 5. Conclusion | الخلاصة

Choose a **library** when you need a targeted feature that fits into an application you already control. Choose a **framework** when you want a consistent structure for a larger application and are willing to follow its conventions. The two can work together: a framework-based application can use many separate libraries.

اختر **مكتبة** عندما تحتاج إلى وظيفة معينة داخل مشروعك، واختر **إطار عمل** عندما تحتاج إلى بنية منظمة لبناء التطبيق كاملًا. يمكن استخدام المكتبات داخل أطر العمل، ولا يوجد تعارض بينهما.

## 6. References | المراجع الأصلية

These links lead to first-party documentation or a named technical author's explanation. They can be opened individually to verify the statements and examples.

1. Martin Fowler. [Inversion of Control](https://martinfowler.com/bliki/InversionOfControl.html).
2. Animate.css. [Official documentation](https://animate.style/).
3. Bootstrap. [Version 5 documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/).
4. Lodash. [Official website](https://lodash.com/).
5. Angular. [What is Angular?](https://angular.dev/overview).
6. Apache Commons. [Commons Lang](https://commons.apache.org/proper/commons-lang/).
7. Spring. [Spring Framework](https://spring.io/projects/spring-framework/).
8. Guzzle. [Documentation](https://docs.guzzlephp.org/).
9. Laravel. [Documentation](https://laravel.com/docs).
10. Requests. [Official documentation](https://docs.python-requests.org/en/latest/).
11. Django. [Official website](https://www.djangoproject.com/), [documentation](https://docs.djangoproject.com/en/5.2/intro/overview/).

---

**Academic note:** The assignment asks for traditional research. Review the original links yourself, take notes from them, and confirm the comparison before submitting. The infographic is a visual summary of these references.
