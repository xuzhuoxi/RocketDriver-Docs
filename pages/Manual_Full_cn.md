---
layout: print
page_id: 'home.manual'
group_id: home
lang: zh-CN
title: '用户手册'
---
{% include_relative ManualInclude_Head_cn.md %}

{%- include i18ntext.html -%}
{% assign pages = i18ntext.manual.nav | where: "show", "yes" %}
{% for p in pages %}
{% include_relative {{p.include}} %}
{% endfor %}