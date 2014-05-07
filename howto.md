clone this repository

`gh-pages` branch is equivalent to `master`

`gh-pages` branch is published to http://ncareol.github.io/wag-devops-vagrant

load [`reveal.js`](https://github.com/hakimel/reveal.js/) as `git submodule`:

    $ git submodule init && git submodule update

content is in `slides/*.md`

individual slides are delimited by `!SLIDE`

slide notes can be delimited by `!NOTE`

slide files can be added to `index.html`, *e.g.*

```html
<section data-markdown="slides/intro.md"
         data-separator="^!SLIDE\n"
         data-vertical="^^!SLIDE vertical\n"
         data-notes="^!NOTE"
         data-charset="iso-8859-15">
</section>
```

`index.html` must be loaded through a webserver so that JavaScript can parse the MarkDown files while obeying `same-origin` policy. To do this in Apache:

```
Alias /wag-devops-vagrant /Users/ej/Dropbox/NCAR/wag-devops-vagrant/
```

makes the presentation available @ http://localhost/wag-devops-vagrant

presenter mode: 'S'
