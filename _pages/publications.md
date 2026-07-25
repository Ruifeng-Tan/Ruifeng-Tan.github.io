---
layout: default
title: "Publications"
permalink: /publications/
author_profile: false
---

<main class="academic-shell">
  <header class="academic-card page-hero">
    <h1>Publications</h1>
    <p>Research on battery intelligence, degradation forecasting, materials informatics, and graph learning. An asterisk (*) denotes equal contribution.</p>
  </header>

  <section class="academic-card academic-card--compact">
    <h2 class="section-heading">All Publications</h2>
    <div class="publication-list">
      {% for publication in site.data.publications %}
        {% include publication-card.html publication=publication %}
      {% endfor %}
    </div>
  </section>
</main>
