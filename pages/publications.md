---
layout: page
title: "Publications"
categories:
 - papers
---

<h2 class="section-title fade-in">Publications</h2>
<p class="section-subtitle fade-in">Selected peer-reviewed publications from our lab</p>

<div class="fade-in">
{% assign years = (2010..2100) | reverse %}
{% for year in years %}
    {% assign is_print_year = true %}
        {% for paper in site.categories.papers %}
            {% if paper.year == year %}
                {% if is_print_year %}
<div class="pub-year">{{ year }}</div>
                    {% assign is_print_year = false %}
                {% endif %}
<div class="pub-item">
    <a href="{{ paper.doi }}">{{ paper.title }}.</a><br>
    <em>{{ paper.authors }}.</em><br>
    <em><strong>{{ paper.journal }}</strong>, {{ paper.year }}.</em>
</div>
            {% endif %}
        {% endfor %}
{% endfor %}
</div>
