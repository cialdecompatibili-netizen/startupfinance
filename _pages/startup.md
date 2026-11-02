---
layout: single
title: "Startup"
permalink: /startup/
ref: startup
author_profile: false
seo_description: "Le startup che costruiamo: scopri lo stato, candidati o chiedi informazioni."
---

<p class="hub-lead">Le idee che stiamo costruendo, validando e portando sul mercato. Ognuna ha uno stato chiaro e due strade: entrare nel team o saperne di più come investitore.</p>

{% assign st = site.data.startup %}
{% if st.size > 0 %}
<div class="hub-grid">
{% for s in st %}
<div class="hub-card">
<span class="hub-tag">{{ s.stato }}</span>
<p><strong>{% if false and s.nome_en %}{{ s.nome_en }}{% else %}{{ s.nome }}{% endif %}</strong></p>
<p>{% if false and s.descrizione_en %}{{ s.descrizione_en }}{% else %}{{ s.descrizione }}{% endif %}</p>
{% if s.link %}<p><a class="hub-btn hub-btn--l" href="{{ s.link }}">Leggi il progetto completo</a></p>{% endif %}
<div class="hub-act"><a class="hub-btn hub-btn--a" href="{{ '/investi/?startup=' | append: s.id | relative_url }}">Investi</a> <a class="hub-btn hub-btn--o" href="{{ '/lavora-con-noi/?startup=' | append: s.id | relative_url }}">Candidati</a></div>
</div>
{% endfor %}
</div>
{% else %}
<div class="hub-vuoto">Nessuna startup pubblicata per ora. Le prime arrivano presto.</div>
{% endif %}

## Come scegliamo le idee
Ogni idea passa da un metodo di validazione prima di ricevere tempo e risorse. [Leggi come validiamo]({{ '/come-validiamo/' | relative_url }}).

## Hai un'idea?
[Proponila qui]({{ '/lavora-con-noi/?ruolo=idea' | relative_url }}): se supera la validazione, la costruiamo insieme.
