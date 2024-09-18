---
permalink: /bibliography/
# title: "Enrique Barba Roque"
author_profile: true
layout: single
---

Academic publications that study environmentally sustainable artificial intelligence – **Green AI**.
In particular, this bibliography focus on research that aims at making the development of AI systems more friendly to the environment.

Contributions are welcome! If you have suggestions for other readings consider sending a pull request or creating an issue in the [Github repository][github-repo]!  😉

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


[github-repo]: https://github.com/luiscruz/green-ai