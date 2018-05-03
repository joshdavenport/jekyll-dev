# jekyll-theme-dev

Allows for easier local development when using a path based theme in jekyll. e.g. when your jekyll site gemspec looks something like this:

```ruby
gem "a-jekyll-theme", :path => "../a-jekyll-theme"
```

This is most useful when either devleping a theme you're going to distribute or when you're developing a theme that you're reusing in multiple jekyll sites.

By default livereload is also provided, but you can disable this, see [Options](#options)

## Installation

```shell
npm install -g jekyll-theme-dev
```

## Options

See `jekyll-theme-dev` for full list of options. However here are some commonly used ones:

* `--no-livereload` - Disable livereload

## Potential Usage & Workflow

Here's a scenario where this tool may be useful, if previous descriptions haven't already communicated that to you.

1. Create a jekyll site and a theme:

   ```shell
   ## create a site named jekyll-site
   jekyll new jekyll-site

   ## create a theme named jekyll-theme-sample
   jekyll new-theme a-jekyll-theme
   ```

2. Add the theme to your site's `Gemfile`

   ```ruby
   ## replace default theme `gem "minima", ...`
   gem "a-jekyll-theme", :path => "../a-jekyll-theme"
   ```

3. Add the following to your site's `_config.yml` to activate the theme:

   ```yaml
   ## replace any other theme already here (e.g. `theme: minima`)
   theme: a-jekyll-theme
   ```

4. Start to develop:

   ```shell
   cd jekyll-site
   jekyll-theme-dev
   ```

## License

MIT
