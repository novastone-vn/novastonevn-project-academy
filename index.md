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

<!-- ========================================== -->
<!-- 以下为新增的互动留言/工程询盘板块 -->
<!-- ========================================== -->
<div style="margin-top: 5rem; border-top: 2px solid #333; padding-top: 3rem; margin-bottom: 3rem;">
  <h2 style="font-size: 1.8em; font-weight: bold; color: #111; margin-bottom: 0.5rem;">
    Have a Question or an Upcoming Project?
  </h2>
  <p style="color: #666; font-size: 1.05em; margin-bottom: 2rem;">
    Whether you need value engineering advice, full slab imagery, or direct container pricing for tailored projects, drop your message below. Our team will get back to you within 24 hours.
  </p>

  <form action="https://formspree.io/f/mrevwggp" method="POST" style="max-width: 600px;">
    
    <div style="display: flex; gap: 15px; margin-bottom: 15px; flex-wrap: wrap;">
      <div style="flex: 1; min-width: 250px;">
        <label style="display: block; font-weight: 500; margin-bottom: 5px; font-size: 0.9em; color: #333;">Your Name *</label>
        <input type="text" name="name" required style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 1em;">
      </div>
      <div style="flex: 1; min-width: 250px;">
        <label style="display: block; font-weight: 500; margin-bottom: 5px; font-size: 0.9em; color: #333;">Company Name / Profession</label>
        <input type="text" name="company" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 1em;" placeholder="e.g., Fabricator, GC, Architect">
      </div>
    </div>

    <div style="margin-bottom: 15px;">
      <label style="display: block; font-weight: 500; margin-bottom: 5px; font-size: 0.9em; color: #333;">Work Email *</label>
      <input type="email" name="_replyto" required style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 1em;">
    </div>

    <!-- 专业技术问题引导区 -->
    <div style="background-color: #f9f9f9; border-left: 3px solid #111; padding: 15px; margin-bottom: 20px; font-size: 0.9em; border-radius: 0 4px 4px 0;">
      <strong style="display: block; margin-bottom: 8px; color: #111;">Feel free to ask our engineering team about:</strong>
      <ul style="margin: 0; padding-left: 20px; color: #555; line-height: 1.6;">
        <li><strong>Technical Compliance:</strong> Request ASTM test reports, NSF/Greenguard certifications, or resin-to-quartz ratio details.</li>
        <li><strong>Value Engineering:</strong> How to optimize slab yields and minimize seam waste for your specific multi-family/hospitality layouts.</li>
        <li><strong>Fabrication & Design:</strong> Inquiries regarding vein-matching for large islands, mitered edge profiles, or cut-to-size tolerances.</li>
        <li><strong>US Logistics:</strong> Lead times for direct container shipping from Vietnam, packaging security, and tariff/anti-dumping compliance.</li>
      </ul>
    </div>

    <div style="margin-bottom: 20px;">
      <label style="display: block; font-weight: 500; margin-bottom: 5px; font-size: 0.9em; color: #333;">Your Message or Technical Questions *</label>
      <textarea name="message" required rows="5" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 1em; resize: vertical;"></textarea>
    </div>

    <button type="submit" style="background-color: #111; color: #fff; padding: 12px 30px; border: none; border-radius: 4px; font-size: 1em; font-weight: bold; cursor: pointer;">
      Submit Inquiry
    </button>
  </form>
</div>
