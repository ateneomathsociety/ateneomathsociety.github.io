---
layout:       default
title:        "About"
heading:      "About Us"
subheading:   "Get to know AMS"
permalink:    "/about"
banner:
  image:      "/assets/images/banners/default.png"
  height:     180px
  opacity:    1.00
---

{%- assign about = site.data.about -%}
{%- assign project_count = site.projects.size | default: "0" -%}

<section class="section-base">
  <h1>Identity</h1>
  {% for identity in about.identity %}
    <p>{{ identity }}</p>
  {% endfor %}
</section>

<section class="section-base">
  <h1>Vision</h1>
  <p>{{ about.vision }}</p>
</section>

<section class="section-base">
  <h1>Mission</h1>
  <p>The organization has the mission to:</p>
  <ul>
  {% for mission in about.mission %}
    <li>{{ mission }}</li>
  {% endfor %}
  </ul>
</section>

<section class="section-base">
  <h1>The Organization by the Numbers</h1>
  <div class="stats-container">
    <div class="stat-card">
      <div id="years" class="stat-number">{{ about.years }}</div>
      <div class="stat-description">Years</div>
    </div>
    <div class="stat-card">
      <div id="projects" class="stat-number">{{ project_count }}</div>
      <div class="stat-description">Projects</div>
    </div>
    <div class="stat-card">
      <div id="members" class="stat-number">{{ about.members }}</div>
      <div class="stat-description">Members</div>
    </div>
    <div class="stat-card">
      <div id="fb-likes" class="stat-number">{{ about.fb_page_follows }}</div>
      <div class="stat-description">FB Page Follows</div>
    </div>
  </div>
</section>

<script>
  // Set years
  function setYears() {
    const today = new Date();
    const dateEstablished = new Date("{{ about.date_established }}");
    let age = today.getFullYear() - dateEstablished.getFullYear();
    const monthDifference = today.getMonth() - dateEstablished.getMonth();
    if (monthDifference < 0) {
      age--;
    } 
    if (monthDifference === 0) {
      if (today.getDate() < dateEstablished.getDate()) {
        age--;
      }
    }
    document.getElementById('years').textContent = age;
  }

  setYears();
</script>
