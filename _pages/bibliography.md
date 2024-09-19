---
permalink: /bibliography/
# title: "Enrique Barba Roque"
author_profile: true
layout: single
---

I will be posting the papers around Green AI and Sustainable Machine Learning that I read and found interesting, with some notes on their contributions and some thoughts from myself.

This bibliography is part of my PhD program on Green AI with [Luís Cruz](https://luiscruz.github.io/) at TU Delft, where I'll be working in the [SELF Lab](https://www.tudelft.nl/ai/self-lab) for medical IoT edge devices.

# Papers

{% for paper in site.bibliography reversed%}
{{paper.name}}
{% assign currentdate = paper.year %}
{% if currentdate != date %}
### 📅 **{{ currentdate }}**
{% assign date = currentdate %} 
{% endif %}

  <p markdown="span">
      {{paper.author}} ({{paper.year}}).
      {%- unless paper.disable-page %}
      [**{{paper.title}}**]({{paper.url | relative_url}}).
      {%- else %}
      **{{paper.title}}**
      {%- endunless %}
      {%- if paper.journal %}
        *{{paper.journal}}*{% if paper.pages %} (pp. {{paper.pages}}){% endif %}.
      {% endif -%}
{%-for tag in paper.tags %}
<span class="badge">{{tag}}</span>
{% endfor %}
</p>
{%- if paper.annotation %}
<blockquote><small markdown="1">
{{paper.annotation | truncate: 300 }} [Read more.]({{paper.url | relative_url}})
</small></blockquote>
{% endif -%}

{% endfor %}