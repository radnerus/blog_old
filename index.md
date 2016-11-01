---
layout: default
---

<div class="post">
  {% for post in site.posts %}
    <p>
          <a href="{{ post.url }}">{{ post.title }}</a>
          <br/>

          {{ post.date | date: "%-d %B %Y" }}
          {% include image.html%}
          {{ post.excerpt }}
    </p>
  {% endfor %}
</div>
