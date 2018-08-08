{% import 'common.rst' as common %}

.. js:module:: {{ name }}{{ params }}

   {{ common.deprecated(deprecated)|indent(3) }}

   {% for heads, tail in fields -%}
     :{{ heads|join(' ') }}: {{ tail }}
   {% endfor %}

   {{ content|indent(3) }}

   {% if members -%}
     {{ members|indent(3) }}
   {%- endif %}

   {{ common.see_also(see_also)|indent(3) }}