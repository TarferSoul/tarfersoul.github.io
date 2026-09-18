<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  {% if link.image %}
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %}
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  {% endif %}
  {% assign paper_url = link.paper | default: link.pdf %}
  <div class="{% if link.image %}col-sm-9{% else %}col-sm-12{% endif %}" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ paper_url }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if paper_url %}
      <a href="{{ paper_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.dataset %}
      <a href="{{ link.dataset }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Dataset</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.arxiv %}
      <a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener" style="font-size:12px;">arXiv</a>
      {% endif %}
      {% if link.notes %}
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
