# WileyLabs Web Site

Uses [Jekyll](http://jekyllrb.com/) to generate a static,
[Semantic-UI](http://semantic-ui.com/) based project promo site.

## Development

```
$ bundle install # the jekyll bits
$ npm i # the semantic-ui bits
$ npm run build # once. not needed again unless customizing semantic.css
$ bundle exec jekyll serve --incremental # more optimal serve/watch
```

## Data

The `_data/repos.json` is pulled from the GitHub API for
[listing organizations](https://developer.github.com/v3/repos/#list-organization-repositories)
and customized to remove any repos we're not currently promoting.

# License

Apache License 2.0
