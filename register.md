---
layout: page
title: Register
# Fees, ages, and sign-up links render from the divisions data file, so the
# "Suggest an edit" button points there rather than at this page's wording.
edit_path: _data/divisions.yml
---

All MTL Hockey sign-ups in one place. Registration is rolling — signing up early helps us gauge interest and secure ice time, so don't wait for a deadline.

{% for d in site.data.divisions %}
## {{ d.name }}

**{{ d.ages }}** {% if d.fee_tbd %}&middot; **Fee TBD — final pricing coming soon**{% else %}&middot; **{{ d.fee }}**{% endif %}

{% for item in d.details %}- {{ item }}
{% endfor %}
{% if d.register_url == "" %}
*Registration link coming soon — email [mountaintop.hockey@gmail.com](mailto:mountaintop.hockey@gmail.com) to get notified the moment it opens.*
{% else %}
[**Register for {{ d.name }} →**]({{ d.register_url }})
{% endif %}
{% endfor %}

## Questions?

Email [mountaintop.hockey@gmail.com](mailto:mountaintop.hockey@gmail.com) or see the [FAQ]({{ site.baseurl }}/faq/).
