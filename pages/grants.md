---
layout: page
title: "Grants"
---

<h2 class="section-title fade-in">Research Grants</h2>
<p class="section-subtitle fade-in">Current research projects and funding</p>

<div class="grants-list stagger">
{% for grant in site.data.grants %}
  <div class="grant-card">
    <div class="grant-header">
      {% if grant.role == "연구책임자" %}
        <span class="grant-badge pi">PI</span>
      {% else %}
        <span class="grant-badge co-pi">Co-PI</span>
      {% endif %}
      <span class="grant-agency">{{ grant.agency }}</span>
    </div>
    <h3 class="grant-title">{{ grant.title }}</h3>
    <div class="grant-meta">
      <div class="grant-meta-item">
        <span class="grant-label">사업명</span>
        <span>{{ grant.program }}</span>
      </div>
      <div class="grant-meta-item">
        <span class="grant-label">연구개발기간</span>
        <span>{{ grant.period }}</span>
      </div>
    </div>
  </div>
{% endfor %}
</div>
