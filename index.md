---
layout: default
---

<div class="pure-u-3-4">
  {% for post in site.posts | limit : 2 %}
      <p>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <br/>
            {{ post.date | date: "%-d %B %Y" }}
            {% include image.html%}
            {{ post.excerpt  | strip_html | truncatewords:20}}
      </p>
  {% endfor %}
</div>
<div class="pure-u-1-4 side-pane">
  <div class="side-pane-contents">
    <span>Trending:</span>
    <ul>
    {% for post in site.posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </div>
</div>
