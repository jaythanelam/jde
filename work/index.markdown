---
title: Work
header: white
weight: 2
headline: Work
clients:
- name: Cook ai
  role: Product Design Lead
  link: https://cook.ai/
  year: 2017
- name: Razor
  role: Brand Designer
  link: https://github.com/carbonfive/razor
  year: 2017
- name: Are you a sandwich?
  role: Pro bono/fun
  link: http://areyouasandwich.com/
  year: 2016
- name: CodeXX
  role: Contract Brand/Marketing
  link: https://www.meetup.com/CodeXX/
  year: 2016
- name: Amazing Grass
  role: Logo/Packaging Design
  link: http://amazinggrass.com
  year: 2015
- name: Vizio
  role: Product Designer
  link: http://vizio.com
  year: 2015
- name: Kareo
  role: Art Director
  link: http://kareo.com
  year: 2015
- name: Blossom
  role: 'Brand Designer '
  link: http://getblossom.com
  year: 2015
- name: Biola University
  role: Designer
  link: http://biola.edu
  year: 2014
layout: default
---

{% include globals/page-header.html %}

<section class="page-body">
  <div class="post-content wrapper xs-mb6">
      <div class="xs-block gutters">
          <div class="col xs-col-12">
            <h4 class="xs-mt3 xs-mb2 xs-pr1 xs-inline-block">Recent Work</h4>
          </div>
      </div>
  </div>
</section>

<div class="shots"></div>

<section class="page-body">
  <div class="post-content wrapper xs-mt3">
      <div class="xs-block gutters">
        <div class="col xs-col-12 xs-mb4">
          <div class="xs-col-12 xs-overflow-hidden line-span">
            <h4 class="xs-mt6 xs-mb3 xs-pr1 xs-inline-block">Select Projects</h4>
          </div>
        </div>
        {% for item in page.clients %}
          <div class="col xs-col-12 md-col-6 lg-col-4 xs-mb4 xs-mt3 xs-inline-block">
            <h2 class="xs-mb2 xs-pr6"><a href="{{item.link}}">{{item.name}}</a></h2>
            <h4 class="-xs-pr6">{{item.role}}</h4>
          </div>
        {% endfor %}
      </div>
  </div>
</section>

<script type="text/javascript">
  $.jribbble.setToken('edb536adf0118d406d24bd93635da4e5ffe43425d7c5376797d8dbd32d2ccda2');

  $.jribbble.users('jaythan').shots({per_page: 14}).then(function(shots) {
    var html = [];

    shots.forEach(function(shot) {
      html.push('<span class="shots--shot">');
      html.push('<a href="' + shot.html_url + '" target="_blank">');
      html.push('<img src="' + shot.images.hidpi + '">');
      html.push('</a></span>');
    });

    $('.shots').html(html.join(''));
  });
</script>
