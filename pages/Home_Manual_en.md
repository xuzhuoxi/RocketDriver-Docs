---
layout: default
page_id: 'home.manual'
group_id: home
lang: 'en-US'
title: 'User Manual'
---
{% include_relative ManualInclude_Head_en.md %}

{%- include i18ntext.html -%}
{% assign pages = i18ntext.manual.nav | where: "show", "yes" %}
{% for p in pages %}
  <h4><a href="{{ site.home.url }}/{{ p.pattern }}">{{ p.text }}</a><h4>
{% endfor %}