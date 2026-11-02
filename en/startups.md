---
layout: single
title: "Startups"
permalink: /en/startups/
ref: startup
author_profile: false
description: "The startups we are building: see their status, apply or ask for information."
lang: en
locale: en
tr: da_aggiornare
tr_hash: ki82yx
---

<p class="hub-lead">The ideas we are building, validating and taking to market. Each has a clear status and two paths: join the team or learn more as an investor.</p>

{% assign st = site.data.startup %}
{% if st.size > 0 %}
<div class="st-list">
{% for s in st %}
<div class="st-row">
<span class="hub-tag">{{ s.stato }}</span>
<p><strong>{% if true and s.nome_en %}{{ s.nome_en }}{% else %}{{ s.nome }}{% endif %}</strong></p>
<p>{% if true and s.descrizione_en %}{{ s.descrizione_en }}{% else %}{{ s.descrizione }}{% endif %}</p>
{% if s.link_en %}<p><a class="hub-btn hub-btn hub-btn--a" href="{{ s.link_en }}">Read the full project</a></p>{% endif %}
<div class="hub-act"><a class="hub-btn hub-btn--a" href="{{ '/en/invest/?startup=' | append: s.id | relative_url }}">Invest</a> <a class="hub-btn hub-btn--o" href="{{ '/en/work-with-us/?startup=' | append: s.id | relative_url }}">Apply</a></div>
</div>
{% endfor %}
</div>
{% else %}
<div class="hub-vuoto">No startups published yet. The first ones are coming soon.</div>
{% endif %}

## How we pick ideas
Every idea goes through a validation method before it gets time and resources. [Read how we validate]({{ '/en/how-we-validate/' | relative_url }}).

## Got an idea?
[Pitch it here]({{ '/en/work-with-us/?ruolo=idea' | relative_url }}): if it passes validation, we build it together.
