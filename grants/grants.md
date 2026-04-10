---
layout: page
title: "Grants"
---
{% for grant in site.data.grants %}
# 전문기관명
{{ grant.agency }}

## 사업명
{{ grant.program }}

## 연구개발과제명
{{ grant.title }}

## 참여유형
{{ grant.role }}

## 연구개발기간
{{ grant.period }}
{% unless forloop.last %}
---
{% endunless %}
{% endfor %}
