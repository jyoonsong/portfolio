---
layout: home
title: Publications
order: 1
---

{% assign publications = site.data.publications | sort: "year" | reverse %}
{% assign papers = publications | where_exp: "item", "item.attrs contains 'paper'" %}
{% assign posters = publications | where_exp: "item", "item.attrs contains 'poster'" %}
{% assign wips = publications | where_exp: "item", "item.attrs contains 'wip'" %}


<section>
    <h2 class="title">Conference & Journal Papers</h2>

    {% for pub in papers %}
    {% include publication.html pub = pub %} 
    {% endfor %}
</section>

<section>
    <h2 class="title">Posters</h2>

    {% for pub in posters %}
    {% include publication.html pub = pub %} 
    {% endfor %}
</section>

<section>
    <h2 class="title">Work in Progress</h2>

    {% for pub in wips %}
    {% include publication.html pub = pub %} 
    {% endfor %}
</section>