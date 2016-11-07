---
layout: default
---
<div class="pure-u-3-4">
  <div style="color:red;">{{page.title}}</div>
  {{ page.date | date: "%-d %B %Y" }}
  {% include image.html%}
  {{ content}}
</div>
<div class="pure-u-1-4 side-pane">
  <div class="side-pane-contents">
    <span>Similar Posts:</span>
    {% for category_name in page.categories %}
      {% if site.categories[category_name].size > 1 %}
      <span>Other articles in {{ category_name }}</span>
      <ul>
      {% for post in site.categories[category_name] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
      </ul>
      {% endif %}
    {% endfor %}
  </div>
</div>
