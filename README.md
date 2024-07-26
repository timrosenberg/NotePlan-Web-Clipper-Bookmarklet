# Installation
- Create a new bookmark in your browser, then copy/paste the minified code below into the URL field.
- The bookmarklet has been tested with Safari and Chrome. If you want to add it to Arc, there's a way to make it into a Extention and add it via developer mode. I haven't tested this yet.

# Usage
By default, clicking the bookmarklet adds the entire text of the article to your Daily Note. While this seems chaotic to me, live your life. Alternatively you can choose a selection, by either selecting all (CMD+A), or just a portion of the page, and then clicking the bookmarklet. This will import the selected text.

## Format
The formatting follows the so-called "link-post" style popularized by John Gruber, Jason Kottke, and others. The bookmarklet will grab the title of the page, the URL, and attempt to find the author. It will then assemble it in markdown as so:
```
---
## Clippings
[Title](URL) by Author
> Selected text
```
It will then open NotePlan to the Daily Note.

# Caveats
I am hardly an experienced programmer; so, this bookmarklet has a lot of rough edges that are beyond my avility to solve. Known isses include:
- When clipping more than one paragraph of text, only the first paragraph will be inside the quote block. The other quote blocks will need to be added manually after the fact.
- The `---` and the H2 tag will be added _each time_ the bookmarklet is used. If you don't want those added each time, you will need to delete them after the fact. As far as I know there's no way to target a specific header in NotePlan using the URL scheme alone. Furthermore, there's no way to check if that header exists and only add it if it doesn't exist. I believe there are plug-ins that can do this; but, I am not smart enough to know how engage them with the URL scheme.
- As with most bookmarklet web clippers, there's only so much it can do. This bookmarklet probably work on all websites.

# Credit
Almost all of the code for this bookmarklet comes from kepano's [obsidian-web-clipper.js](https://gist.github.com/kepano/90c05f162c37cf730abb8ff027987ca3). I modified a bit of the formatting and incorporated the NotePlan URL scheme. Everything else comes from his brilliant mind and I am grateful to him for the inspiration.
