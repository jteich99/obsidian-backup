---
tags:
  - project/tesis/bibliografia
title: "{{title}}"
authors: "{{authors}}"
year: '{{date | format("YYYY")}}'
citekey: "{{citekey}}"
---
### Self Notes
{% persist "notes" %}


{% endpersist %}

---

## Reading notes
{% persist "annotations" %}

{% set annots = annotations | filterby("date", "dateafter", lastImportDate) -%}

{% if annots.length > 0 %}
{% for annot in annots -%}
{%- if annot.annotatedText %}
- <mark style="background: {{annot.color}}">{{annot.annotatedText | nl2br}} </mark>
{%- endif -%}

{%- if annot.imageRelativePath %}
![[{{annot.imageRelativePath}}]]
{%- endif %}

{%- if annot.comment %}
>[!annot] Comment
>{{annot.comment | nl2br}}
 {%- endif %}

{%- endfor %}
{%- endif %}
{%- endpersist %}