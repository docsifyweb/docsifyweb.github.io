---

# More Files

> Make your website great!

## Cover

Activate the cover feature by setting `coverpage` to true.

### Basic usage

Set `coverpage` to true.  

```html
<script>
  window.$docsify = {
    coverpage: true
  }
</script>
```

Next, create a `coverpage.md` and write the cover content.  

```markdown
![logo](icon.svg)

# Docsify Website

> A magical documentation site generator.

- Simple and lightweight
- No statically built html files
- Multiple themes

[GitHub](https://github.com/docsifyjs/docsify/)
[Get Started](#docsify)
```

In this way, a beautiful cover can be rendered quickly.

### Custom background

The background color is generated randomly by default. You can customize the background color or a background image.  

```markdown
![](bg.png)
```

```markdown
![color](#f0f0f0)
```

For different needs, you can freely choose the plan that suits you.

## More Pages

If you need more pages, you can simply create more markdown files in your docsify directory.

### Path

If you create a file named `guide.md`, then it is accessible via `/#/guide`.  

For example, the directory structure is as follows.  

```text
└── docs
    ├── README.md
    ├── guide.md
    └── zh-cn
        ├── README.md
        └── guide.md
```

The corresponding visit page is as follows.  

```text
docs/README.md        => http://domain.com
docs/guide.md         => http://domain.com/#/guide
docs/zh-cn/README.md  => http://domain.com/#/zh-cn/
docs/zh-cn/guide.md   => http://domain.com/#/zh-cn/guide
```

### Sidebar

In order to have a sidebar, you can create your own `_sidebar.md`.  

First, you need to set `loadSidebar` to true.  

```html
<script>
  window.$docsify = {
    loadSidebar: true
  }
</script>
```

Create the `_sidebar.md`.  

```markdown
* [Home](/)
* [Guide](guide.md)
```

> [!Attention]
> Docsify only looks for `_sidebar.md` in the current folder, and uses that, otherwise it falls back to the one configured using `window.$docsify.loadSidebar` config.

### Hierarchical Sidebar

Sometimes, our documentation is hierarchical, and we can organize the sidebar into layers.  

```markdown
* [Home](/)
* [Guide](guide.md)
  * [Subpage 1](subpage1.md)
  * [Subpage 2](subpage2.md)
```

> [!Tip]
> Docsify's sidebar can support multiple levels of structure, but having too many levels can make the sidebar less clear or harder to navigate. It's generally best to keep the hierarchy simple and straightforward to ensure users can easily find the information they need.

### Set Page Titles from Sidebar Selection

A page's `title` tag is generated from the selected sidebar item name. For better SEO, you can customize the title by specifying a string after the filename.  

```markdown
* [Home](/)
* [Guide](guide.md "The greatest guide in the world")
```

## Custom navbar

In Docsify, the navigation bar is displayed in the top right corner of the page. Again, the creation of the navigation bar is very simple.

### HTML navbar

If you need custom navigation, you can create a HTML-based navigation bar.  

> [!Note]
> that documentation links begin with `#/`.

```html
<body>
  <nav>
    <a href="#/">English</a>
    <a href="#/zh-cn/">简体中文</a>
    <a href="#/de-de/">Deutsch</a>
  </nav>
  <div id="app"></div>
</body>
```

### Markdown navbar

Alternatively, you can create a custom markdown-based navigation file by setting `loadNavbar` to true and creating `_navbar.md`.  

```html
<script>
  window.$docsify = {
    loadNavbar: true
  }
</script>
```

```markdown
* [En](/)
* [简体中文](/zh-cn/)
* [Deutsch](/de-de/)
```

> [!Tip]
> In general, the format that uses Markdown is better.

> [!Attention]
> `_navbar.md` is loaded from each level directory. If the current directory doesn't have `_navbar.md`, it will fall back to the parent directory. If, for example, the current path is `/guide/quick-start`, the `_navbar.md` will be loaded from `/guide/_navbar.md`.

### Nested navbar

You can create sub-lists by indenting items that are under a certain parent.  

```markdown
* Getting started

  * [Quick start](quickstart.md)
  * [Writing more pages](more-pages.md)
  * [Custom navbar](custom-navbar.md)
  * [Cover page](cover.md)

* Configuration
  * [Configuration](configuration.md)
  * [Themes](themes.md)
  * [Using plugins](plugins.md)
  * [Markdown configuration](markdown.md)
  * [Language highlight](language-highlight.md)
```

When the mouse pointer hovers over the navigation bar, the nested content will be displayed.
