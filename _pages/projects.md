---
layout: page
title: projects
permalink: /projects/
description: Research and engineering projects, in descending order of complexity.
nav: true
nav_order: 3
_styles: |
  .project-list { display: flex; flex-direction: column; gap: 1rem; }
  .project-card { border: 1px solid var(--global-divider-color); border-radius: 6px; padding: 1rem 1.25rem; background: var(--global-card-bg-color); }
  .project-card.lead { border-left: 4px solid var(--global-theme-color); }
  .project-card h2 { font-size: 1.25rem; margin: 0; display: inline; }
  .project-card.small h2 { font-size: 1.05rem; }
  .project-card .project-head { display: flex; flex-wrap: wrap; align-items: center; gap: 0.5rem 0.75rem; margin-bottom: 0.5rem; }
  .project-card p { margin: 0 0 0.6rem; }
  .project-status { font-size: 0.75rem; font-weight: 500; padding: 0.1rem 0.55rem; border-radius: 999px; border: 1px solid var(--global-theme-color); color: var(--global-theme-color); white-space: nowrap; }
  .project-foot { display: flex; flex-wrap: wrap; align-items: center; gap: 0.4rem; font-size: 0.8rem; }
  .project-tag { padding: 0.05rem 0.5rem; border-radius: 4px; background: var(--global-code-bg-color); color: var(--global-text-color); }
  .project-link { margin-left: auto; white-space: nowrap; }
---

{% assign sorted_projects = site.projects | sort: "importance" %}

<div class="project-list">
  {% for project in sorted_projects %}
    <section class="project-card {{ project.size }}">
      <div class="project-head">
        <h2>{{ project.title }}</h2>
        {% if project.status and project.status != "" %}
          <span class="project-status">{{ project.status }}</span>
        {% endif %}
      </div>
      {{ project.content | markdownify }}
      <div class="project-foot">
        {% for tag in project.stack %}
          <span class="project-tag">{{ tag }}</span>
        {% endfor %}
        {% if project.github %}
          <a class="project-link" href="{{ project.github }}"><i class="fa-brands fa-github"></i> Code</a>
        {% elsif project.paper %}
          <a class="project-link" href="{{ '/publications/' | relative_url }}"><i class="fa-solid fa-file-lines"></i> Paper</a>
        {% endif %}
      </div>
    </section>
  {% endfor %}
</div>
