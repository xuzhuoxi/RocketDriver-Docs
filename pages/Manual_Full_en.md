---
layout: print
page_id: 'home.manual'
group_id: home
lang: 'en-US'
title: 'User Manual'
---
{% include_relative ManualInclude_Head_en.md %}

{%- include i18ntext.html -%}
{% assign pages = i18ntext.manual.nav | where: "show", "yes" %}
{% for p in pages %}
{% include_relative {{p.include}} %}
{% endfor %}