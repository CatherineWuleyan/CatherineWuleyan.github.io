<h2 id="projects" style="margin: 2px 0px 15px;">Projects</h2>

<div class="projects">
<ol class="project-list" style="padding-left: 0; list-style: none;">

{% for project in site.data.projects.main %}

<li>
<div class="presentation-row">
  <div class="presentation-media">
    {% if project.image %}
    <img src="{{ project.image }}" class="presentation-cover" alt="{{ project.title }} cover">
    {% endif %}
  </div>

  <div class="presentation-content">
      <div class="title">{{ project.title }}</div>
    <div class="links">
      {% if project.doc %}
      <a href="{{ project.doc }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Paper</a>
      {% endif %}
      {% if project.slides %}
      <a href="{{ project.slides }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Slides</a>
      {% endif %}
      {% if project.code %} 
      <a href="{{ project.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if project.page %} 
      <a href="{{ project.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if project.demo %} 
      <a href="{{ project.demo }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Live Demo</a>
      {% endif %}
      {% if project.notes %} 
      <strong> <i style="color:#e74d3c">{{ project.notes }}</i></strong>
      {% endif %}
      {% if project.others %} 
      {{ project.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
