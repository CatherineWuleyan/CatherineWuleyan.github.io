<h2 id="notes" style="margin: 2px 0px -15px;">Notes</h2>

<div class="notes">
<ol class="note-list" style="padding-left: 0; list-style: none;">

{% for note in site.data.notes.main %}

<li>
<div class="note-row" style="display: flex; flex-wrap: wrap;">
  <!-- 左侧：笔记配图或分类标签 -->
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if note.image %} 
    <img src="{{ note.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;">
    {% endif %}
    {% if note.category %} 
    <abbr class="badge">{{ note.category }}</abbr>
    {% endif %}
  </div>
  
  <!-- 右侧：笔记信息与链接 -->
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ note.url }}">{{ note.title }}</a></div>
      <div class="description">{{ note.description }}</div>
      <div class="date"><em>{{ note.date }}</em></div>
      
    <div class="links">
      {% if note.pdf %} 
      <a href="{{ note.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if note.url %} 
      <a href="{{ note.url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Read More</a>
      {% endif %}
      {% if note.slides %} 
      <a href="{{ note.slides }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Slides</a>
      {% endif %}
      {% if note.highlight %} 
      <strong> <i style="color:#e74d3c">{{ note.highlight }}</i></strong>
      {% endif %}
      {% if note.others %} 
      {{ note.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
