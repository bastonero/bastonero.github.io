---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

{% if site.cv_pdf %}
<a href="{{ base_path }}/files/{{ site.cv_pdf }}" class="btn btn--primary">Download CV as PDF</a>
{% endif %}

Employment
======
* **Postdoctoral researcher**, Harvard University, Cambridge (MA, USA) — *since July 2026*
  * Advisor: Prof. Dr. Boris Kozinsky (Gordon McKay Professor of Materials Science and Mechanical Engineering)
* **Postdoctoral researcher**, University of Bremen, Bremen (Germany) — *February 2026 – June 2026*
  * Advisor: Prof. Dr. Nicola Marzari (Cavendish Professor of Physics, University of Cambridge; Theory and Simulation of Materials, EPFL; Excellence Chair, University of Bremen)

Education
======
* **Ph.D. in Physics**, University of Bremen, Bremen (Germany), 2021 – 2026 — *summa cum laude*
  * Thesis: *Automated first-principles highways for Mars exploration*
  * Supervisor: Prof. Dr. Nicola Marzari
* **M.Sc. in Physics**, University of Turin, Turin (Italy), 2018 – 2020 — *110/110 cum laude and Honorable Mention*
  * Thesis: *Prediction of the Optoelectronic Properties of 2D Heterostructures Via First Principles Simulations*
  * Supervisors: Prof. Dr. Giancarlo Cicero (Polytechnic of Turin), Prof. Dr. Ettore Vittone (University of Turin), Dr. Michele Re Fiorentin (Polytechnic of Turin)
* **B.Sc. in Physics**, University of Turin, Turin (Italy), 2015 – 2018 — *110/110*
  * Thesis: *Double slit problem for surface waves: Lagrangian transport of particles*
  * Supervisor: Prof. Dr. Miguel Onorato

Research visits
======
* **EPFL**, Lausanne (Switzerland) — Nov. 2025, July–Aug. 2024, Apr.–July 2023, Apr.–June 2022, Sept.–Oct. 2021
  * Long research stays in Prof. Nicola Marzari's group (THEOS).
* **EMPA (ETH Zürich)**, Zürich (Switzerland) — June 2024
  * Visit to Dr. Carlo Pignedoli's group.
* **PSI**, Villigen (Switzerland) — January 2024
  * Visit to Dr. Giovanni Pizzi's group.
* **ETH Zürich**, Zürich (Switzerland) — July 2023
  * Visit to Prof. Mathieu Luisier's group.

Awards
======
* **R. Stephen Berry Early-Career Fellowship 2026**, Telluride Science Scholarship

Computational grants
======
* **Alps** — CSCS CHRONOS grant, Tier-0 Project 2024. Accepted resources: 250k node hours over 2 years
* **LUMI-G** — CSCS CHRONOS grant, Tier-0 Project 2023. Accepted resources: 5M node hours over 2 years
* **NHR@FAU** — HPC grant 2024 (e103ef10). Accepted resources: 49k GPU hours over 1 year
* **HLRN** — HPC grant 2022 (hbi00059). Accepted resources: 9M core hours over 1 year

Technical skills
======
* **Programming languages**: Python, LaTeX, C/C++
* **Scientific software**: AiiDA, Quantum ESPRESSO, phonopy, python-sscha, ASE, Pymatgen, NequIP/Allegro, LAMMPS, AiiDAlab, Yambo, VESTA
* **Development**: git, GitHub, VSCode, Docker, cmake, spack

Languages
======
* Italian (native)
* English (fluent)
* German (basic)

Code development
======
  <ul>{% for post in site.software %}
    <li>{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}{% if post.period %} ({{ post.period }}){% endif %}{% if post.summary %} — {{ post.summary }}{% endif %}</li>
  {% endfor %}</ul>

See the [software](/software/) page for details.

Publications
======
{% for category in site.publication_category %}
{% assign title_shown = false %}
{% for post in site.publications reversed %}
{% if post.category != category[0] %}{% continue %}{% endif %}
{% unless title_shown %}
<h3>{{ category[1].title }}</h3>
<ul>
{% assign title_shown = true %}
{% endunless %}
{% include archive-single-cv.html %}
{% endfor %}
{% if title_shown %}</ul>{% endif %}
{% endfor %}

Talks and posters
======
  <ul>{% for post in site.talks reversed %}
    <li><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a><br />{{ post.type }}, {{ post.venue }}, {{ post.location }}, {{ post.date | date: "%B %Y" }}</li>
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    <li><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a><br />{{ post.type }}, {{ post.venue }}, {{ post.date | date: "%Y" }}</li>
  {% endfor %}</ul>

Outreach
======
  <ul>{% for post in site.outreach reversed %}
    <li><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a><br />{{ post.type }}, {{ post.venue }}, {{ post.location }}, {{ post.date | date: "%B %Y" }}</li>
  {% endfor %}</ul>
