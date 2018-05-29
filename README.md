# The Scrawl theme

**Organize documentation, playbooks, and other composition with Scrawl**

Scrawl is a page-centric theme for Jekyll.  Rather than catering to posts like most Jekyll themes, Scrawl focuses on providing categorization and navigation for pages.

*The Scrawl theme is based on GitHub's [Primer theme](https://github.com/pages-themes/primer) and the left navigation is inspired by Steve Smith's [Minimal](https://github.com/orderedlist/minimal).*

## Installation

Set Jekyll's `_config.yml` to pull the theme from the `lightster/jekyll-theme-scrawl` remote theme:

```yaml
remote_theme: lightster/jekyll-theme-scrawl
```

## Usage

Scrawl is all about pages.

### Pages and their URLs

You will most likely want to create an `index.md` in the root of your Jekyll site.  This is the page that the browser will load when first arriving at your site.

You can create more pages in the root of your Jekyll site, as well as subdirectories of the Jekyll site.  Page URLs match the paths that appear in your site directory structure.

We like our page URLs to leave off the `.html`, so we include the following in our `_config.yml`:
```yaml
permalink: pretty
```

### Layouts

Scrawl provides the following layouts:

 - `base` — The `base` layout is the base layout used by all other layouts.  The base layout has two side-by-side independently scrolling panes.  The left pane contains the site title, the site description, and the navigation.  The right pane is wider and is used for displaying the content.
 - `page` — The `page` layout is the default layout that pages use.  The page layout is similar to the base layout but with a few additions:
   - The `title` value provided in the page's front matter is displayed as a header above the page content
   - The `summary` value provided in the page's front matter is displayed below the page title
   - A table of contents is displayed below the page title and summary.  The table of contents is generated based on the page's level 2, 3, and 4 headers (`<h2>`, `<h3>`, and `<h4>` tags).
 - `sitemap` — The `sitemap` layout breaks the navigation into four columns that takes up the width of the layout.

You can set the layout for a page in the page's Jekyll front matter:
```yaml
---
layout: base
---
```

#### Widths

For the `default` and `page` layouts, there is a `width` setting for controlling how wide the content pane should be:
 - `fixed` — The `fixed` width is the default.  The fixed width layout stays the same width unless the browser window is not wide enough, in which case the navigation is moved into a hamburger menu and the page takes up the width of the browser window.
 - `fluid` - The `fluid` width takes up the width of the browser window.  If the browser window is not wide enough, the navigation is moved into a hamburger menu.
 - `no-nav` – The `no-nav` width behaves like the `fixed` width setting, but it removes the navigation, allowing the content pane to take up the entirety of the fixed width.

#### Mobile-friendly

All layouts and widths are mobile-friendly.

## Development

To set up your environment to develop this theme, fork this repo, clone your fork to your localhost, and run `bundle install`.

The theme is setup just like a normal Jekyll site. Run `bundle exec jekyll serve` and open your browser to [`http://localhost:4000`](http://localhost:4000). As you make changes to your clone of the theme, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When the theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git are bundled.

## License

The theme is available as open source under the terms of the [MIT License](LICENSE).
