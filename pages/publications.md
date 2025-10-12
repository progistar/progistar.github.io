---
layout: page
title: "Publications"
categories: 
 - papers
---


{% assign years = (2010..2100) | reverse %}
{% for year in years %}
    {% assign is_print_year = true %}
        {% for paper in site.categories.papers %}
            {% if paper.year == year %}
                {% if is_print_year %}
<b> {{ year }}
                    {% assign is_print_year = false %}
                {% endif %}
---
<div style="line-height: 1.2em; margin-bottom: 10px;">
    <a style="font-size: 1em;" href="{{ paper.doi }}">{{ paper.title }}.</a>
    <em>{{ paper.authors }}.</em>
    <em><strong>{{ paper.journal }}</strong>, {{ paper.year }}.</em>
</div>
            {% endif %}
        {% endfor %}
{% endfor %}

<div class="spacer"></div>