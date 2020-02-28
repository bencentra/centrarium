Lesní klub Malejov
==================

Website of Lesní klub Malejov, z. s.


Development
-----------

### TL;DR

- [GitHub pages][github-pages] with sources in the root directory.
- The source Jekyll theme is https://github.com/bencentra/centrarium.
- Local development using `docker-compose up`, http://localhost:4000/.


### Jekyll locally

Create a new Jekyll site ([Jekyll version used by GitHub Pages][jekyll-version]).

    mkdir -p bundle
    docker run --rm -it \
        --volume "$PWD:/srv/jekyll" \
        --volume "$PWD/bundle:/usr/local/bundle" \
        jekyll/jekyll:3.8.5 \
        jekyll new /srv/jekyll
    
Serve the site, automatically detect updates, http://localhost:4000/.

    docker run --rm -it \
        --volume "$PWD:/srv/jekyll" \
        --volume "$PWD/bundle:/usr/local/bundle" \
        --publish 4000:4000 \
        jekyll/jekyll:3.8.5 \
        jekyll serve

Clean generated files.

    docker run --rm -it \
        --volume "$PWD:/srv/jekyll" \
        --volume "$PWD/bundle:/usr/local/bundle" \
        --publish 4000:4000 \
        jekyll/jekyll:3.8.5 \
        jekyll clean

Install and update dependencies.

    rm docs/Gemfile.lock
    docker run --rm -it \
        --volume "$PWD:/srv/jekyll" \
        --volume "$PWD/bundle:/usr/local/bundle" \
        --publish 4000:4000 \
        jekyll/jekyll:3.8.5 \
        bundle install

    docker run --rm -it \
        --volume "$PWD:/srv/jekyll" \
        --volume "$PWD/bundle:/usr/local/bundle" \
        --publish 4000:4000 \
        jekyll/jekyll:3.8.5 \
        bundle update

[github-pages]: https://help.github.com/en/github/working-with-github-pages
[jekyll-version]: https://pages.github.com/versions/
