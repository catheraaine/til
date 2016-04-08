## Creating a Page Jump in Markdown

#### [Jump from here!](#jump)

A "page jump" is when a link is anchored to a point later on on the same page.

By using a tiny bit of HTML, page jumps can be added to Markdown files. This is especially useful for longer files with skimmable content, where a reader may wish to access only specific sections.

Start by creating a link in your markdown file. Instead of a normal url, we'll add a hash in front of a key word.

```
[Jump from here!](#jump)
```

Then, add an empty anchor tag in front of the content you would like linked to. This is probably a heading, or similar.  The `href` attribute should equal the keyword.

```
#### <a name="jump"></a> Jump to here!
```

Check out my [contents file](../contents.md) for live examples, or click the subheading at the top of this page.

#### <a name="jump"></a> Jump to here!
