---
layout: default
---

<div class="pure-u-2-3">
  {% for post in site.posts %}
      <p>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <br/>

            {{ post.date | date: "%-d %B %Y" }}
            {% include image.html%}
            {{ post.excerpt  | strip_html | truncatewords:20}}
      </p>
  {% endfor %}
</div>
<div class="pure-u-1-3">
  <div class="side-pane">
    <span>Trending:</span>
    <ul>
    {% for post in site.posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </div>
</div>
