---
layout: page
title: MTL Hockey
---

MTL Hockey is part of the [Mountain Top League](https://mountaintopleague.com/), an all-volunteer organization serving the children of West Orange, NJ since 1959. We offer ice hockey and street hockey programs — no travel required, all fun.

## 2026–27 Programs

<div class="picker-grid">
{% for d in site.data.divisions %}
  <a href="{{ site.baseurl }}/register/" class="picker-card">
    {{ d.name }}
    <small>{{ d.ages }}{% if d.fee_tbd %} &middot; fee TBD{% else %} &middot; {{ d.fee }}{% endif %}</small>
  </a>
{% endfor %}
</div>

## New to MTL Hockey?

Read [How MTL Hockey Works]({{ site.baseurl }}/how-it-works/) for an overview of divisions, schedules, and what to expect, or jump straight to [registration]({{ site.baseurl }}/register/).

## Where We Play

Street hockey at O'Connor Park, full ice at Codey Arena, league games at Mennen Arena — maps and details on the [Rinks]({{ site.baseurl }}/rinks/) page.

## Get Involved

MTL is run entirely by volunteers. To coach, manage a team, or help out, email [mountaintop.hockey@gmail.com](mailto:mountaintop.hockey@gmail.com).
