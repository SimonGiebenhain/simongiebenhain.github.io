# Publications

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

<div class="row">

<div class="well col-sm-18 clearfix">
  <div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="100%" style="float: left; padding-right: 10px" />
  </div>
  <div class="col-sm-8">
  <pubtit>{{ publi.title }}</pubtit>
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

</div>


{% endif %}
{% endfor %}


<p> &nbsp; </p>
