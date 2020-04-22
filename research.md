---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Fast-Fourier-Forecasting Resource Utilisation in Distributed Systems"
      author:  "Paul J. Pritz, Daniel Perez, Kin K. Leung"
      journal: "arXiv preprint"
      year:    "2020"
      url:     "https://arxiv.org/abs/2001.04281"
      pdf:
        - name: "arXiv"
          url:  "https://arxiv.org/pdf/2001.04281.pdf"
    
    - title:   "Step on the Gas? A Better Approach for Recommending the Ethereum Gas Price"
      author:  "Sam M. Werner, Paul J. Pritz, Daniel Perez"
      journal: "arXiv preprint"
      note:    "Accepted to Marble 2020."
      year:    "2020"
      url:     "https://arxiv.org/abs/2003.03479"
      pdf:
        - name: "arXiv"
          url:  "https://arxiv.org/pdf/2003.03479.pdf"

    - title:   "Uncle Traps: Harvesting Rewards in a Queue-based Ethereum Mining Pool"
      author:  "Sam M. Werner, Paul J. Pritz, Alexei Zamyatin, William J. Knottenbelt"
      journal: "Proceedings of the 12th EAI International Conference on Performance Evaluation Methodologies and Tools"
      note:    "Received Best Presentation Award."
      year:    "2019"
      url:     "https://dl.acm.org/doi/pdf/10.1145/3306309.3306328"
      pdf:
        - name: "dl.acm.org"
          url:  "https://dl.acm.org/doi/pdf/10.1145/3306309.3306328"
---

## Publications

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
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
