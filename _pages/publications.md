<h2>Publications</h2>

<div class="publist">
{% for publi in site.data.publist %}
{% if publi.highlight == 1 %}
<article class="pub">
<div class="pub-media">
{% if publi.image contains '.mp4' %}
<video src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" autoplay muted loop playsinline preload="metadata" aria-label="{{ publi.title | escape }}"></video>
{% else %}
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" alt="{{ publi.title | escape }}" loading="lazy">
{% endif %}
</div>
<div class="pub-body">
<h3 class="pub-title">{{ publi.title }}</h3>
<p class="pub-authors">{{ publi.authors | replace: "Simon Giebenhain", "<strong>Simon Giebenhain</strong>" }}</p>
<p class="pub-desc">{{ publi.description }}</p>
{% if publi.news1 %}<p class="pub-news1">{{ publi.news1 }}</p>{% endif %}
{% if publi.news2 %}<p class="pub-news2">{{ publi.news2 }}</p>{% endif %}
<p class="pub-links"><a class="pill" href="{{ publi.link.url }}">{{ publi.link.display }}</a></p>
</div>
</article>
{% endif %}
{% endfor %}
</div>
