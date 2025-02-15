---
layout: page
title: projects
permalink: /projects/
description: 
nav: true
nav_order: 2
display_categories:
  - name: Artificial Intelligence
    subcategories: [Machine Learning,Data Science,Generative Models]
  - name: Work Projects
    subcategories: [Enterprise Solutions]
  - name: Academic Projects
    subcategories: [Capstone, Course Project]
  - name: Software Engineering
    subcategories: [Full Stack]
horizontal: false
---

<!-- Tab Layout for Categories -->
<div class="tab-container">
  <div class="tab-buttons">
    {%- for category in page.display_categories %}
    <button class="tab-button" onclick="showCategoryTab('{{ category.name | slugify }}')">{{ category.name }}</button>
    {%- endfor %}
  </div>

  <div class="tab-content-container">
    {%- for category in page.display_categories %}
    <div class="tab-content" id="{{ category.name | slugify }}">
      <h2>{{ category.name }}</h2>
      
      <!-- Subcategories -->
      <div class="subcategory-container">
        {%- for subcategory in category.subcategories %}
        <button class="subcategory-button" onclick="showSubcategory('{{ category.name | slugify }}', '{{ subcategory | slugify }}')">{{ subcategory }}</button>
        {%- endfor %}
      </div>

      {%- for subcategory in category.subcategories %}
      <div class="subcategory-content {{ category.name | slugify }}-subcategory" id="{{ subcategory | slugify }}">
        <h3>{{ subcategory }}</h3>
        {%- assign categorized_projects = site.projects | where: "category", category.name | where: "subcategory", subcategory -%}
        {%- assign sorted_projects = categorized_projects | sort: "importance" %}
        <div class="project-items">
          {%- for project in sorted_projects -%}
            {% include projects.html %}
          {%- endfor %}
        </div>
      </div>
      {%- endfor %}
    </div>
    {%- endfor %}
  </div>
</div>

<style>
/* Tab Button Styling */
.tab-container {
  max-width: 900px;
  margin: auto;
  padding: 20px;
}

.tab-buttons {
  display: flex;
  justify-content: space-around;
  margin-bottom: 15px;
}

.tab-button {
  background: #222;
  color: white;
  padding: 10px;
  border: none;
  cursor: pointer;
  transition: background 0.3s;
  font-size: 1rem;
  border-radius: 5px;
}

.tab-button:hover {
  background: #333;
}

/* Subcategory Buttons */
.subcategory-container {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 10px;
}

.subcategory-button {
  background: #444;
  color: white;
  padding: 8px;
  border: none;
  cursor: pointer;
  transition: background 0.3s;
  font-size: 0.9rem;
  border-radius: 5px;
}

.subcategory-button:hover {
  background: #555;
}

/* Tab Content Styling */
.tab-content-container {
  background: #333;
  padding: 15px;
  border-radius: 5px;
}

.tab-content {
  display: none;
}

/* Subcategories */
.subcategory-content {
  display: none;
  margin-top: 15px;
  padding: 10px;
  background: #222;
  border-radius: 5px;
}

.subcategory-content h3 {
  font-size: 1.1rem;
  color: white;
  margin-bottom: 5px;
}

/* Active Classes */
.active-tab {
  display: block;
}

.active-subcategory {
  display: block;
}
</style>

<script>
function showCategoryTab(categoryId) {
  var tabs = document.getElementsByClassName("tab-content");
  for (var i = 0; i < tabs.length; i++) {
    tabs[i].style.display = "none";
  }
  document.getElementById(categoryId).style.display = "block";

  // Hide all subcategories when switching categories
  var subcategories = document.getElementsByClassName(categoryId + "-subcategory");
  for (var i = 0; i < subcategories.length; i++) {
    subcategories[i].style.display = "none";
  }
}

function showSubcategory(categoryId, subcategoryId) {
  var subcategories = document.getElementsByClassName(categoryId + "-subcategory");
  for (var i = 0; i < subcategories.length; i++) {
    subcategories[i].style.display = "none";
  }
  document.getElementById(subcategoryId).style.display = "block";
}

// Open the first category and subcategory by default
document.getElementsByClassName("tab-button")[0].click();
</script>
