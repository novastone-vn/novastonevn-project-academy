---
layout: default
title: Home
---

<div style="margin-top: 2rem; margin-bottom: 3rem;">
  <h1 style="font-size: 2.5em; font-weight: bold; letter-spacing: -1px;">Novastone Vietnam Project Academy</h1>
  <p style="font-size: 1.2em; color: #555; line-height: 1.6;">
    Expert Insights for Premium Quartz Surfaces & Engineering. <br>
    <span style="font-size: 0.9em; color: #777;">
      Actionable guides, comparative analyses, and industry updates dedicated to General Contractors, Fabricators, and Designers across US residential, commercial, and hospitality sectors.
    </span>
  </p>
</div>

{% for category in site.categories %}
  <h2 style="margin-top: 2rem; border-bottom: 1px solid #eee; padding-bottom: 10px; color: #333;">
    {{ category[0] | replace: "-", " " }}
  </h2>
  <ul style="list-style-type: none; padding-left: 0;">
    {% for post in category[1] %}
      <li style="margin-bottom: 15px;">
        <span style="color: #999; font-size: 0.85em; font-family: monospace; margin-right: 15px;">
          {{ post.date | date: "%b %d, %Y" }}
        </span> 
        <a href="{{ post.url | relative_url }}" style="text-decoration: none; font-size: 1.1em; color: #0056b3; font-weight: 500;">
          {{ post.title }}
        </a>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
