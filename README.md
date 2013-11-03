# pelican-sora

simple theme for Pelican. 

## Feature
* Use LESS, easy to customize
* Responsive Theme (Based on [PureCSS][purecss])
* [pelican-elegant][pelican-elegant] based theme. Thanks to [talha131][talha131]
  * Support search (Using [Tipue Search][tipue])
  * Live filter for Tags
  * Custom 404 Page

## Dependency
* [LESS](http://lesscss.org)
* pip install BeautifulSoup4
* pip install webassets

## Configure
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

[purecss]: http://purecss.io/
[talha131]: https://github.com/talha131
[pelican-elegant]: http://oncrashreboot.com/elegant-best-pelican-theme-features
[tipue]: http://www.tipue.com/search/
