<h2 id="projects" style="margin: 2px 0px -15px;">Projects</h2>

<div class="projects">
<ol class="project-list" style="padding-left: 0; list-style: none;">

{% for project in site.data.projects.main %}

<li>
<div class="project-row" style="display: flex; flex-wrap: wrap;">
  <!-- 左侧：项目图片与标签 -->
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if project.image %} 
    <img src="{{ project.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;">
    {% if project.tag %} 
    <abbr class="badge">{{ project.tag }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  
  <!-- 右侧：项目信息与链接 -->
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ project.link }}">{{ project.title }}</a></div>
      <div class="description">{{ project.description }}</div>
      <div class="tech-stack"><em>{{ project.tech_stack }}</em></div>
      
    <div class="links">
      {% if project.doc %} 
      <a href="{{ project.doc }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Docs</a>
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
