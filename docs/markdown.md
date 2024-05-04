---

# Markdown

> The best text markup language.

The content of this article is from [Markdown Tutorial](https://commonmark.org/help/tutorial/) by CommonMark.  

Markdown is a lightweight markup language with a concise typography syntax that allows people to focus more on the content itself than on the layout. It writes documents in an easy-to-read, easy-to-write plain text format that can be mixed with HTML and can be exported in HTML, PDF, and its own `.md` format. Because of its conciseness, efficiency, readability, and ease of writing, Markdown is widely used, such as Github, Wikipedia, etc.

## Paragraph

To create a paragraph, use a blank line to separate one or more lines of text.  

```markdown
I really like using Markdown. 

I think I'll use it to format all of my documents from now on.
```

> [!Attention]
> In the rendered page, there is no line break between the two lines. If you want to wrap lines, please refer to the following.

## Line breaks

Add two or more spaces at the end of a line and press `enter` to create a line break (`<br>`).  

```markdown
I really like using Markdown.  

I think I'll use it to format all of my documents from now on.
```

> [!Note]
> Here 2 spaces are added to the end of the line, resulting in a line break. These 2 spaces will not be rendered.

2 spaces may not be inconspicuous, so adding `<br>` at the end of a line is also a good idea.  

```markdown
I really like using Markdown.<br>

I think I'll use it to format all of my documents from now on.
```

## Bold

To create bold, wrap with `**` or `__`.  

```markdown
This text is **emphasized**.
```

```markdown
This text is __emphasized__.
```

> [!Tip]
> For compatibility, use `**` if you are bold in the middle of a word or phrase.

## Italic

To create italic, wrap with `*` or `_`.  

```markdown
This text is *emphasized*.
```

```markdown
This text is _emphasized_.
```

> [!Tip]
> For compatibility, use `*` if you are italic in the middle of a word or phrase.

## Bold italics

To create bold and italic, wrap with `***` or `___`.  

No more code shown.  

> [!Tip]
> For compatibility, use `***` if you are bold and italic in the middle of a word or phrase.

## Title

To create a title, add `#` in front of a word or phrase. The number of `#` represents the level of the title.  

```markdown
# Title 1
## Title 2
### Title 3
#### Title 4
##### Title 5
###### Title 6
```

> [!Note]
> Only Level 1 to Level 6 headings can be created.

## Blockquotes

To create a block reference, add a `>` symbol before the paragraph.  

```markdown
> This is a blockquote.
```

```markdown
> This is line 1.
>
> This is line 2.
```

Blockquotes can be nested, and can also contain other formatting.  

```markdown
> Blockquote 1
>> Blockquote 2
```

```markdown
> #### Blockquote
```

## Lists

Multiple entries can be organized into an ordered or unordered list.  

Ordered List:  

```markdown
1. First item
2. Second item
3. Third item
```

```markdown
1. First item
1. Second item
1. Third item
```

> [!Note]
> The numbers don't have to be in mathematical order, but the list should start with the number 1.

Unordered List:  

```markdown
+ First item
+ Second item
+ Third item
```

```markdown
- First item
- Second item
- Third item
```

```markdown
* First item
* Second item
* Third item
```

> [!Note]
> Markdown applications don't agree on how to handle different delimiters in the same list. For compatibility, don't mix and match delimiters in the same list - pick one and stick with it.

## Code

To represent text as a single line of code, use <code>`</code>.  

```markdown
At the command prompt, type `python`.
```

To create a multi-line block of code, use <code>```</code>.  

```markdown
```python
print("Hello World!")
```‎
```

After the first <code>```</code>, you can add or not add a language identifier.  

> [!Attention]
> For proper code highlighting, use the correct language identifier. This is case-sensitive.

## Horizontal Rule

To create a horizontal line, use `---`, `***` or `___` on a separate line. The line cannot contain anything else.  

```markdown
# Title 1

---

# Title 2
```

## Links

The link text is placed in middle brackets, and the link address is placed in the following parentheses.  

```markdown
[Link](https://docsifyweb.github.io/)
```

There is also a `title` to choose from.  

```markdown
[Link](https://docsifyweb.github.io/ "Docsify Website")
```

If you don't need link text, use `<>`.  

```markdown
<https://docsifyweb.github.io/>
```

## Images

To add an image, use an `!`, then add alt text in square brackets, and the image link in parentheses, which can be followed by an optional image title text.  

```markdown
![Image](image.jpg "Image Title")
```

The title can be left unattached.  

The link here can also be an image page.  

Sometimes, we want to click on an image and go to a different URL.  

```markdown
[![Image](image.jpg "Image Title")](https://docsifyweb.github.io/)
```

In Docsify, there is also support for scaling images.  

```markdown
![logo](https://docsify.js.org/_media/icon.svg ':size=WIDTHxHEIGHT')
![logo](https://docsify.js.org/_media/icon.svg ':size=50x100')
![logo](https://docsify.js.org/_media/icon.svg ':size=100')
![logo](https://docsify.js.org/_media/icon.svg ':size=10%') <!-- Support percentage -->
```

## Escape characters

To display the characters that were originally used to format a Markdown document, add a `\` in front of the character.  

```markdown
\* Without the backslash, this would be a bullet in an unordered list.
```

Escape characters can escape almost all Markdown characters, including itself.  

This can be useful at some point.  

> [!Tip]
> Because Markdown can contain HTML tags, try using HTML tags when escaping characters doesn't solve the problem!
