---
layout: default
title: Projects
---

<div class="projects-hero">
  <h1>Featured Projects</h1>
  <p>Innovative solutions powered by AI and machine learning</p>
</div>

<section class="project-gallery">
  <div class="project-grid">
    {% for project in site.data.projects %}
    <div class="project-card">
      <div class="project-header">
        <h3>{{ project.title }}</h3>
        <span class="project-tech">{{ project.technologies | join: ', ' }}</span>
      </div>
      <div class="project-description">
        <p>{{ project.description }}</p>
      </div>
      <div class="project-links">
        {% if project.github %}
        <a href="{{ project.github }}" class="button secondary" target="_blank">GitHub</a>
        {% endif %}
        {% if project.demo %}
        <a href="{{ project.demo }}" class="button secondary" target="_blank">Demo</a>
        {% endif %}
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<section class="project-categories">
  <h2>Project Categories</h2>
  <div class="category-grid">
    <div class="category-card">
      <h3>AI/ML</h3>
      <p>Machine learning models and AI-powered solutions</p>
      <span class="project-count">4 Projects</span>
    </div>
    
    <div class="category-card">
      <h3>Web Development</h3>
      <p>Modern web applications and platforms</p>
      <span class="project-count">2 Projects</span>
    </div>
    
    <div class="category-card">
      <h3>Community Tools</h3>
      <p>Tools for community engagement and collaboration</p>
      <span class="project-count">1 Project</span>
    </div>
  </div>
</section>

<section class="project-filters">
  <h2>Filter Projects</h2>
  <div class="filter-tags">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="ai">AI/ML</button>
    <button class="filter-btn" data-filter="web">Web</button>
    <button class="filter-btn" data-filter="community">Community</button>
  </div>
</section>
