# WileyLabs Web Site

Uses [Jekyll](http://jekyllrb.com/) to generate a static,
[Semantic-UI](http://semantic-ui.com/) based project promo site.

## Development

You'll need [Ruby](https://www.ruby-lang.org/).

```
$ gem install jekyll bundler
$ bundle install # the jekyll bits
$ npm i # the semantic-ui bits
$ npm run build # once. not needed again unless customizing semantic.css
$ bundle exec jekyll serve --incremental # more optimal serve/watch
```

## Data

The `_data/repos.json` is pulled from the GitHub API for
[listing organizations](https://developer.github.com/v3/repos/#list-organization-repositories)
and customized to remove any repos we're not currently promoting.

You can easily update the `_data/repos.json` file with this curl command:
```bash
$ curl https://api.github.com/orgs/wileylabs/repos?type=sources > _data/repos.json
```

# License

Apache License 2.0
