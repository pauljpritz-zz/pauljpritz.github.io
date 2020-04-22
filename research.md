---
layout: page
permalink: /research/
title: Research
---

## Publications

{% assign thumbnail="left" %}

{% for pub in site.data.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.pdf %}<br />PDF: {% for article in pub.pdf %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
