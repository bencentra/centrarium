# Centrarium

A custom theme for [my Jekyll blog][bencentra]. If you like it, you're welcome to use it, too!

Built with these awesome libraries: 
* [Bourbon][bourbon] 
* [Neat][neat]
* [Bitters][bitters]
* [Refills][refills]
* [Font Awesome][fontawesome]
* [HighlightJS][highlightjs]
* [Lightbox][lightbox]

Demo: TO-DO

Cover image by Chris M. Morris ([flickr][cover]).

## Features

This theme comes with a number of features that a base Jekyll site doesn't have, including:
* Social media integration (Twitter, Facebook, LinkedIn, GitHub, Google+)
* A categorized archive of all posts
* Default pagination on the homepage
* Disqus integration for post comments
* Lightbox for viewing full-screen photos or albums

## Installation

TO-DO

## Configuration

All configuration options can be found in `_config.yml`. 

### Site Settings

* __title:__ The title for your site. Displayed in the navigation menu, the `index.html` header, and the footer.
* __subtitle:__ The subtitle of your site. Displayed in the `index.html` header.
* __email:__ Your email address, displayed with the Contact info in the footer.
* __name:__ Your name. _Currently unused._
* __descriptionL__ The description of your site. Used for search engine results and displayed in the footer.
* __baseurl:__ The subpath of your site (e.g. /blog/).
* __url:__ The base hostname and protocol for your site.
* __cover:__ The relative path to your site's cover image.
* __logo:__ The relative path to your site's logo. Used in the navigation menu instead of the title if provided.

### Build Settings

* __markdown:__ Markdown parsing engine. Default is kramdown.
* __paginate:__ Number of posts to include on one page.
* __paginate_path:__ URL structure for pages.

### Disqus Settings

You can enable [Disqus][disqus] comments for you site by including one config option:

* __disqus_shortname:__ Your Disqus username. If the property is set, Disqus comments will be included with your blog posts.

### Social Settings

Your personal social network settings are combined with the social sharing options. In the __social__ seciton of `_config.yml`, include an entry for each network you want to include. For example:

```yml
social:
  - name: Twitter                         # Name of the service
    icon: twitter                  		  # Font Awesome icon to use (minus fa- prefix)
    username: "@TheBenCentra"             # (User) Name to display in the footer link
    url: https://twitter.com/TheBenCentra # URL of your profile (leave blank to not display in footer)
    desc: Follow me on Twitter            # Description to display as link title, etc
    share_url: http://twitter.com/share   # URL for sharing to the service (leave blank to disable sharing)
    share_title: ?text=                   # Title parameter for sharing URL
    share_link: "&amp;url="               # Link parameter for sharing URL
```

Any of the __share__ prefixed options are used in blog posts for the social share bar. The other options are used in the Contact info section of the footer.

[bencentra]: http://bencentra.com
[bourbon]: http://bourbon.io/
[neat]: http://neat.bourbon.io/
[bitters]: http://bitters.bourbon.io/
[refills]: http://refills.bourbon.io/
[fontawesome]: http://fortawesome.github.io/Font-Awesome/
[highlightjs]: https://highlightjs.org/
[lightbox]: http://lokeshdhakar.com/projects/lightbox2/
[cover]: https://www.flickr.com/photos/79666107@N00/3796678503/in/photolist-6MuYfc-61Rtft-8XzPmY-a6Cozm-54eSMs-6oMJmk-aepZQq-9YkPHp-fiAEGE-dVP4Z5-oxPyJP-atKUFJ-9YHWA5-9YF2f2-9YF2gR-9YHVGN-9YHVvs-qZYYQ6-4JqP2i-a2peGy-9YHVUm-9YHVF7-9YHVCL-9YF3NK-cYteMo-aiPmb9-69dtAi-9YF21x-4aWpmn-7SLiUL-77pqVX-8vXbYv-4HGDSH-a2h5P1-8LsZrQ-9aj1ez-auPZ7q-9YHVMd-9YF2bi-9YF23D-8LpWpn-9an6KL-9YHVZL-dqZ3Cz-2GuvnX-9YHWUo-9YHVWd-p5Roh5-i1zTbv-6sYrUT
[disqus]: https://disqus.com/
