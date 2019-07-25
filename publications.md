---
layout: post
title: Publications
order: 1
---
{% assign publications = site.data.publications | sort: "year" | reverse %}
{% assign international_publications = publications | where_exp: "item", "item.attrs contains 'international'" %}
{% assign domestic_publications = publications | where_exp: "item", "item.attrs contains 'domestic'" %}


{% for pub in international_publications %}
{% include publication.html pub = pub %} 
{% endfor %}