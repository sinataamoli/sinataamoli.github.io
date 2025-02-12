---
layout: page
title: Teaching
permalink: /teaching/
description: Courses that I have been instructing as a Teaching Assistant.
nav: true
nav_order: 5
display_categories: [teaching]
horizontal: true
---

---
layout: page
permalink: /teaching/
title: Teaching
description: Courses that I have been instructing as Teaching Assistant
nav: true
nav_order: 5
---

Introduction to Data Science
Introduction to Applied Machine Learning
Applications of Data Visualization and Computer Graphics


<!-- pages/teaching.md -->
<div class="teaching">
{% if page.display_categories %}
  {% for category in page.display_categories %}
  <a id="{{ category | slugify }}" href=".#{{ category | slugify }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  <div class="grid">
    <div class="teaching-card">
      <a href="{{ site.baseurl }}/teaching/{{ category | slugify }}/">
        <h3>{{ category }}</h3>
      </a>
    </div>
  </div>
  {% endfor %}
{% endif %}
</div>
3. Explanation of the New Structure
Each course has its own dedicated page.
The main Teaching page (teaching.md) lists the courses dynamically.
The structure is similar to the Projects page, but instead of using _data/projects.yml, we use a manually defined display_categories list.
4. Optional: Styling (if needed)
If the layout doesn’t look right, you can add CSS styles in your theme's custom CSS file (assets/css/custom.scss):

scss
Copy
Edit
.teaching-card {
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  text-align: center;
  transition: all 0.3s;
}

.teaching-card:hover {
  background-color: #f8f9fa;
}

.teaching-card a {
  text-decoration: none;
  font-weight: bold;
  color: #007bff;
}