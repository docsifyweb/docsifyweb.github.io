---

# Plugins

> Create a fully functional docsify now!

Now our documentation site is beautiful and functional enough, but it doesn't seem to be advanced enough.  

Docsify's rich plugins make it easy for us to do just that. It's amazing!  

When choosing a plugin, don't forget to compare it with a plugin with the same functionality. It's going to be a pleasant trip!

## Search

Full-text search will make it easier for users to use.  

First, when using the plugin, JavaScript must be introduced.  

```html
<!-- Search -->
<script src="//fastly.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
```

Sometimes, we want to configure the plugin, and we can do it in `window.$docsify`.  

```html
<script>
  window.$docsify = {
    search: {
      paths: 'auto',
      placeholder: 'Search',
      noData: 'No Data!',
      depth: 6,
      maxAge: 60,
      hideOtherSidebarContent: true,
    },
  }
</script>
```

Of course, it's just a configuration that I think is good. It depends on your choice.  

See detailed usage to the [official documentation](https://docsify.js.org/#/plugins)!  

> [!Warning]
> Since search happens on the client side, users need to be aware of the limitations of search performance and local storage capacity.

## External Script

If the script in the document is an inline script, it can be executed directly, while if it is a backlink script, you need to use this plugin.  

```html
<!-- External Script -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/external-script.min.js"></script>
```

## Zoom image

Mediham's style picture zoom plugin.  

```html
<!-- Zoom image -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/zoom-image.min.js"></script>
```

Ignore an image.  

```markdown
![](image.png ":no-zoom")
```

## Copy to clipboard

This plugin allows you to copy the content of the page to the clipboard.  

Add a Copy to clipboard button.  

```html
<!-- Copy to clipboard -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/clipboard.min.js"></script>
```

## Emoji

This plugin allows you to use emoji in your document.  

```html
<!-- Emoji -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```

## Gitalk

A modern, Preact and Github issue-based commenting system.  

```html
<!-- Gitalk -->
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/gitalk/dist/gitalk.css">

<!-- Gitalk -->
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/gitalk.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/gitalk/dist/gitalk.min.js"></script>
<script>
  const gitalk = new Gitalk({
    clientID: 'Github Application Client ID',
    clientSecret: 'Github Application Client Secret',
    repo: 'Github repo',
    owner: 'Github repo owner',
    admin: ['Github repo collaborators, only these guys can initialize github issues'],
    distractionFreeMode: false
  })
</script>
```

## Word count

It provides the ability to count Chinese characters and English words, and excludes some special characters of Markdown syntax.  

```html
<!-- Word count -->
<script src="//unpkg.com/docsify-count/dist/countable.js"></script>
```

It can be easily configured.

## Progress

Displays the current browsing progress of the document.  

```html
<!-- Progress -->
<script src="//fastly.jsdelivr.net/npm/docsify-progress@latest/dist/progress.min.js"></script>
```

```html
<script>
  window.$docsify = {
    progress: {
      position: 'top',
      color: 'var(--theme-color,#42b983)',
      height: '2px',
    },
  }
</script>
```

It works very well.

## Footer

Add a footer to each of your documents to customize the content.  

```html
<!-- Footer -->
<script src="//fastly.jsdelivr.net/npm/@alertbox/docsify-footer/dist/docsify-footer.min.js"></script>
```

```html
<script>
  window.$docsify = {
    loadFooter: '_footer.md',
  }
</script>
```

```markdown
# The Footer
```

## Flexible alerts

Add more flexible warnings. Including Tip, Note, Warning, Attention. 2 styles to choose from.  

```html
<!-- Flexible alerts -->
<script src="//unpkg.com/docsify-plugin-flexible-alerts"></script>
```

```html
<script>
  window.$docsify = {
    'flexible-alerts': {
      // 2 styles
      style: 'call out',
      style: 'flat',
    }
  };
</script>
```

```markdown
> [!Tip]
> This is a tip.

> [!Note]
> This is a note.


> [!Warning]
> This is a warning.

> [!Attention]
> This is an attention.
```

## Pagination

When there are multiple documents, add Next and Previous at the bottom of the document.  

```html
<!-- Pagination -->
<script src="//unpkg.com/docsify-pagination/dist/docsify-pagination.min.js"></script>
```

## More

The Docsify plugin ecosystem is very rich, and even the official website doesn't list them all. If you're interested, you can search for them on GitHub.  

If your country has slow access to CDN, you can try [fastly](https://fastly.jsdelivr.net/).
