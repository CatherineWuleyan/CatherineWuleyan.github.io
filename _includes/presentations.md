<h2 id="presentations" style="margin: 2px 0px -15px;">Presentations</h2>

<div class="presentations">
<ol class="presentation-list" style="padding-left: 0; list-style: none;">

{% for presentation in site.data.presentations.main %}

<li>
  <div class="presentation-row">
    <div class="presentation-media">
      <img src="{{ presentation.image }}" class="presentation-cover" alt="{{ presentation.title }} cover">
      <abbr class="badge">Presentation</abbr>
    </div>

    <div class="presentation-content">
      <div class="title">{{ presentation.title }}</div>
      <div class="date"><em>{{ presentation.date }}</em></div>

      <div class="links">
        <a href="{{ presentation.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">PDF</a>
      </div>
    </div>
  </div>
</li>
<br>

{% endfor %}

</ol>
</div>
