---

# Quick Start

> Start your documentation journey now!

## Initialize

If you want to write the documentation in the `./docs` subdirectory, you can use the `init` command.  

```bash
docsify init ./docs
```

## Writing content

After the init is complete, you can see the file list in the `./docs` subdirectory.  

- `index.html` as the entry file
- `README.md` as the home page
- `.nojekyll` prevents GitHub Pages from ignoring files that begin with an underscore

You can easily update the documentation in `./docs/README.md`, of course you can add more pages.  

Of course, you can also add more files to help render a better website.

## Preview your site

Run the local server with `docsify serve`. You can preview your site in your browser on http://localhost:3000.  

```bash
docsify serve docs
```

While you may not have started writing documentation yet, you might as well take a look at how it renders. I'm sure you'll love it!

## Loading dialog

If you want, you can show a loading dialog before docsify starts to render your documentation.  

```html
<div id="app">Loading……</div>
```

## Themes

There is a handful of themes available, both official and community-made. Copy [Vue](https://vuejs.org/) and [buble](https://buble.surge.sh/) website custom theme and [@liril-net](https://github.com/liril-net) contribution to the theme of the black style.  

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/vue.css">
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/buble.css">
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/dark.css">
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/pure.css">
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/dolphin.css">
```

Choose the theme that's right for you.
