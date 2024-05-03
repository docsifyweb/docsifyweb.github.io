---

# Configuration

> Customize your docsify page.

In the `window.$docsify`, we can customize our docsify page. Here are some of the commonly used options.

## name

The `name` configuration item is used to set the title of the post at the top of the sidebar and can contain custom HTML code.  

```html
<script>
  window.$docsify = {
    name: '<h3>My Docsify Website</h3>',
  }
</script>
```

## logo

The `logo` appears at the top of the side navigation bar and can be adjusted via CSS.  

```html
<script>
  window.$docsify = {
    logo: 'https://docsify.js.org/_media/icon.svg/',
  }
</script>
```

> [!Attention]
> Only one of the name or logo can be rendered.

## el

The DOM node will be mounted at initialization. This can be either a CSS selector or a real HTML element.  

```html
<script>
  window.$docsify = {
    el: '#app',
  }
</script>
```

## repo

Configure the repository url, or a string of `username/repo`, to add the [GitHub Corner](https://tholman.com/github-corners/) widget in the top right corner of the site.  

```html
<script>
  window.$docsify = {
    repo: 'https://github.com/docsifyweb/',
  }
</script>
```

## maxLevel

Generates the maximum level of the document content navigation directory.Default is 6.  

```html
<script>
  window.$docsify = {
    maxLevel: 3,
  }
</script>
```

## hideSidebar

Hide the sidebar.  

```html
<script>
  window.$docsify = {
    hideSidebar: true,
  }
</script>
```

## auto2top

When you switch pages, you automatically scroll to the top of the page.  

```html
<script>
  window.$docsify = {
    auto2top: true,
  }
</script>
```

## homepage

Specify the master document. The default value is `README.md`.  

If you want to use other documents as your main page, this configuration is very useful.  

```html
<script>
  window.$docsify = {
    homepage: 'index.md',
  }
</script>
```

## basePath

The base path of the site. When specified, the file path of the call changes. It can also be a web address.  

```html
<script>
  window.$docsify = {
    basePath: '/path/',
  }
</script>
```

## relativePath

Enable relative paths.  

```html
<script>
  window.$docsify = {
    relativePath: true,
  }
</script>
```

## nameLink

The URL address of the name link.  

```html
<script>
  window.$docsify = {
    nameLink: {
      '/en/': 'https://docsify.js.org/',
      '/zh-cn/': 'https://docsify.js.org/zh-cn/',
    },
  }
</script>
```

## themeColor

The accent color.  

```html
<script>
  window.$docsify = {
    themeColor: '#3F51B5',
  }
</script>
```

## executeScript

Enable JavaScript scripting.  

```html
<script>
  window.$docsify = {
    executeScript: true,
  }
</script>
```

## noEmoji

Disable emoji parsing.  

```html
<script>
  window.$docsify = {
    noEmoji: true,
  }
</script>
```

## externalLinkTarget

Target to open external links inside the markdown.  

```html
<script>
  window.$docsify = {
    externalLinkTarget: '_self',
  };
</script>
```

## alias

Set the route alias. You can freely manage routing rules. Supports RegExp. Do note that order matters! If a route can be matched by multiple aliases, the one you declared first takes precedence.  

```html
<script>
  window.$docsify = {
    alias: {
      '/foo/(.*)': '/bar/$1', // supports regexp
      '/zh-cn/changelog': '/changelog',
      '/changelog':
        'https://raw.githubusercontent.com/docsifyjs/docsify/master/CHANGELOG',
      '/.*/_sidebar.md': '/_sidebar.md',
    },
  };
</script>
```

## mergeNavbar

Navbar will be merged with the sidebar on smaller screens.  

```html
<script>
  window.$docsify = {
    mergeNavbar: true,
  };
</script>
```

## topMargin

Adds a space on top when scrolling the content page to reach the selected section. This is useful in case you have a sticky-header layout and you want to align anchors to the end of your header.  

```html
<script>
  window.$docsify = {
    topMargin: 90,
  };
</script>
```

## notFoundPage

The 404 pages.  

```html
<script>
  window.$docsify = {
    notFoundPage: '404.md',
  }
</script>
```

## More

There are too many configuration items in docsify, so I won't list them here in order to keep the website simple.  

There are also some that have been discussed in detail earlier and will not be repeated.
