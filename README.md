# pelican-sora

## What is pelican-sora?
pelican-sora is a [pelican][pelican] theme
based on [pelican-elegant][pelican-elegant] theme and [PureCSS][purecss].

* Use LESS, easy to customize
* Responsive Theme
* Many same features in [pelican-elegant][pelican-elegant] based theme. Thanks to [talha131][talha131]
  * Support search (Using [Tipue Search][tipue])
  * Live filter for Tags
  * Custom 404 Page
  * etc...

## Preview
* [LiveDemo](http://static-blog-sample.libsora.so/)
* [OxAA.so](http://0xaa.so/)

![article-desktop](https://raw.github.com/if1live/pelican-sora/master/document/article-desktop.png)

![article-mobile](https://raw.github.com/if1live/pelican-sora/master/document/article-mobile.png)

![index-desktop](https://raw.github.com/if1live/pelican-sora/master/document/index-desktop.png)

![index-mobile](https://raw.github.com/if1live/pelican-sora/master/document/index-mobile.png)

## Variables & Configure

[Look my configure.](https://github.com/static-blog-sample/blog/blob/master/pelicanconf.py)

```python
DEFAULT_PAGINATION = False

# attributes for pelican-sora
PLUGINS = [
	'tipue_search',
	'sitemap',
	'related_posts',
    'assets',
    ]
	
DIRECT_TEMPLATES = (('index', 'tags', 'categories','archives', 'search', '404'))
MD_EXTENSIONS = ['codehilite(css_class=highlight)', 'extra', 'headerid']
STATIC_PATHS = ['theme/images', 'images', 'static']

SITEMAP = {
    'format': 'xml',
    'priorities': {
        'articles': 0.5,
        'indexes': 0.5,
        'pages': 0.5
    },
    'changefreqs': {
        'articles': 'monthly',
        'indexes': 'daily',
        'pages': 'monthly'
    }
}

# optional attributes for pelican-sora
SITE_DESCRIPTION = u'libsora.so'
SITESUBTITLE = ''
SITE_LICENSE = ''
RECENT_ARTICLES_COUNT = 10
```

## Installation
### Dependency
* [LESS](http://lesscss.org)
* [BeautifulSoup4](https://pypi.python.org/pypi/beautifulsoup4)
* [webassets](https://pypi.python.org/pypi/webassets)

```
$ git clone https://github.com/if1live/pelican-sora.git
$ pelican-themes -s path/to/pelican-sora
```

```
THEME = "pelican-sora"
```

[pelican]: http://blog.getpelican.com/
[purecss]: http://purecss.io/
[talha131]: https://github.com/talha131
[pelican-elegant]: http://oncrashreboot.com/elegant-best-pelican-theme-features
[tipue]: http://www.tipue.com/search/
