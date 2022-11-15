---
layout: default
page_id: 'home.manual'
group_id: home
lang: zh-CN
title: '用户手册'
---
{% include_relative ManualInclude_Head_cn.md %}

{% if i18ntext %}
666
{% else %}
777
{% endif %}

{% assign pages = i18ntext.manual.nav | where: "show", "yes" %}
{% for p in pages %}
  <h4><a href="{{ site.home.url }}/{{ p.pattern }}">{{ p.text }}</a><h4>
{% endfor %}

