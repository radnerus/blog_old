---
layout: default
---
<div style="color:red;">{{page.title}}</div>
{{ page.date | date: "%-d %B %Y" }}
{% include image.html%}
{{ content}}
