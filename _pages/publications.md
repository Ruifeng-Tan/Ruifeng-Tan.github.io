---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
---

{% if site.author.googlescholar %}
  <div class="wordwrap">See full publications in <a href="{{site.author.googlescholar}}">Google Scholar</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
