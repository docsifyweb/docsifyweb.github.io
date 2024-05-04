---

# Links

> Handle special links.

Sometimes we will use some other relative path for the link, and we have to tell docsify that we don't need to compile this link. For example.  

```markdown
[link](/demo/)
```

It will be compiled to `<a href="/#/demo/">link</a>` and will load `/demo/README.md`. Maybe you want to jump to `/demo/index.html`.  

```markdown
[link](/demo/ ':ignore')
```

You will get `<a href="/demo/">link</a>` html. Do not worry, you can still set the title for the link.  

```markdown
[link](/demo/ ':ignore title')

<a href="/demo/" title="title">link</a>
```

Set target attribute for link.  

```markdown
[link](/demo ':target=_blank')
[link](/demo2 ':target=_self')
```

Disable link.  

```markdown
[link](/demo ':disabled')
```
