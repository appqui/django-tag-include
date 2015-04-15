# includetag.py
Django template tag. Combination of inheritance and include principles.

Requirements
-------
Django v1.0+. Created at Summer 2009. Have no idea, if it's working with current build.

Installation
-------

Put file "includetag.py" to your app templatetag directory.

In template load includetag by load call: {% load includetag %}
In place of inclusion - put code, similar to my sample:

```HTML+Django
{% include "control.html" %}
  {% part one %} put inside {% endpart %}
  {% part two %} put inside one more {% endpart %}
{% endinclude %}
```

Inside control.html:

```HTML+Django
<div>
   something in control
   {% part one %}{% endpart %}
   more
   {% part two %}{% endpart %}
   end the footer
</div>
```
