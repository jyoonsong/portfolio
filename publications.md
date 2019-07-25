---
layout: home
title: Publications
order: 1
---

{% assign publications = site.data.publications | sort: "year" | reverse %}
{% assign journals = publications | where_exp: "item", "item.attrs contains 'journal'" %}
{% assign posters = publications | where_exp: "item", "item.attrs contains 'poster'" %}
{% assign wips = publications | where_exp: "item", "item.attrs contains 'wip'" %}


<section>
    <h2 class="title">Journals</h2>

    {% for pub in journals %}
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