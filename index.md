---
layout: page
---

# Welcome to Novastonevn Project Academy

Dedicated to sharing the most hardcore industry insights and best practices.

<br>

{% for category in site.categories %}
  ## {{ category[0] }}
  <ul>
    {% for post in category[1] %}
      <li>
        <span style="color: #999; font-size: 0.9em;">{{ post.date | date: "%b %d, %Y" }}</span> &raquo; 
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
