---

# Embed Files

> More powerful Markdown.

With docsify 4.6 it is now possible to embed any type of file.  

You can embed these files as video, audio, iframes, or code blocks, and even Markdown files can even be embedded directly into the document.  

For example, here is an embedded Markdown file. You only need to do this.  

```markdown
[filename](example.md ':include')
```

file extensions are automatically recognized and embedded in different ways.  

Then the content of `example.md` will be displayed directly here.  

[filename](example.md ':include')

Go to [example.md](docs/example.md).  

> [!Tip]
> Normally, this will be compiled into a link, but in docsify, if you add `:include` it will be embedded. You can use single or double quotation marks around as you like. External links can be used too - just replace the target.

See the https://docsify.js.org/#/embed-files for more information.
