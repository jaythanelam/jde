---
title: Site Credits
header: white
hide: true
headline: Site Credits
technical:
- Hosted on [Github](https://github.com/) and cloned from [John Choura Jr.](https://github.com/johnchourajr/john.design)
- Domain with [Dreamhost](https://www.dreamhost.com)
- Built with [Jekyll](https://jekyllrb.com/)
- CMS with [Siteleaf](https://www.siteleaf.com/)
- Code Written on [Atom](https://atom.io/)
- Web Tech [Liquid](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers),
  [jQuery](https://jquery.com/), [Vanilla Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript),
  and [SCSS](http://sass-lang.com/)
- Fonts [Your Native Sans-Serif](https://www.smashingmagazine.com/2015/11/using-system-ui-fonts-practical-guide/)
  and [Space Mono](https://fonts.google.com/specimen/Space+Mono)
- Nav Show/Hide learned from [here](https://medium.com/@mariusc23/hide-header-on-scroll-down-show-on-scroll-up-67bbaae9a78c#.l6t9zfowf)
- Gifs made using [Giphy](http://giphy.com)
other:
- Thank you Andrew for pushing to learn Jekyll.
- I hope to write more than just one post in the journal, but who really knows. I'd certainly hope too.
-
layout: default
---

{% include globals/page-header.html %}

<section class="page-body md-pt6">
  <div class="post-content wrapper xs-mt3">
    <div class="xs-block gutters">
      <div class="col md-col-5">
        <h1>Technical</h1>
        <ul class="xs-mb6">
          {% for item in page.technical %}
            <li><h4 class="text-black xs-mb1">{{ item | markdownify }}</h4></li>
          {% endfor %}
        </ul>
      </div>
      <div class="col md-col-5 md-offset-2">
        <h1>Acknowledgements</h1>
          {% for item in page.other %}
            <h2 class="text-black">
              {{ item }}
            </h2>
          {% endfor %}
      </div>
    </div>
  </div>
</section>
