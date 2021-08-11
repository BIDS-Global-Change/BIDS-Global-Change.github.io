# bids-global-change.github.io
Live here: https://bids-global-change.github.io/

# BIDS Global Change Blog

```r
library(blogdown)
setwd("site directory path") # set blog directory
# blogdown::new_site(theme = "jbub/ghostwriter") # did this step to set up blog

blogdown::new_post("2021-04-26-gbif-miracle-mile-species", ext = '.Rmd') # example of how to make new post

blogdown::serve_site() # example of how to serve the site
blogdown::stop_server() # stop serving site

blogdown::check_site() # check site to give some stats
blogdown::build_site(build_rmd = 'timestamp') # only build new posts
```

In order to suggest and track edits to the posts:
1) Cody will open an issue with a link to the post that needs editing
2) pull in current version
3) fix typos and small grammar mistakes directly on the .Rmd document
4) Larger suggestions can be made with the html comment out tag like below

```html
<!-- insert comments in the .Rmd document like this and they will not render or show up when knit -->
```
5) Issue a pull request for the comments
6) Cody will pull in comments, exit, and then close the issue

In general, all of the site features, order of the tabs, and options can be found in the config.yaml file.

### The following link has instructions for deploying a hugo site on GH pages
https://github.com/skyportal/blog/blob/master/.github/workflows/gh-pages.yml

### Syntax highlighting
The syntax was adjusted following the blogdown textbook approach in the following post:
https://www.r-bloggers.com/2019/07/adding-syntax-highlight/

Add small snippets of code to the header.html and footer.html in theme/ghostwriter/layouts/partials/ directory.
