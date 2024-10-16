# Markdown Syntax
Markdown is a lightweight markup language with plain-text formatting syntax. It is often used to format readme files, for writing messages in online discussion forums (like Reddit), and to create rich text using a plain text editor. Default file extension is `.md`.

Here is a cheat sheet for the syntax of Markdown. Check the legend below to see which elements are supported by Discord. 

<details>
    <summary>Legend</summary>
    <ul>
        <li>✅ Totally supported by Discord.</li>
        <li>⭕ Partially supported by Discord.</li>
        <li>❌ Not (yet) supported by Discord.</li>
    </ul>
</details>

## Basic Syntax
| Element | Markdown Syntax | Supported |
| ------- | --------------- | --------- |
| Heading <br>(up to H6) | `# H1`<br>`## H2`<br>`### H3`<br>`#### H4` | ✅ |
| Bold | `**bold text**` <br> `__italicized text__` | ✅ (`__text__` underlines it) |
| Italic | `*italicized text*` <br> `_italicized text_` | ✅ |
| Strikethrough | `~~strikethrough text~~` | ✅ |
| Underline | `<u>underlined text</u>` | ❌ (use `__text__`) |
| Blockquote | `> blockquote` | ⭕ (put a > for each line) |
| Code | `` `code` `` | ✅ |
| Link | `[text](url)` | ✅ |
| Image | `![alt text](image url)` | ❌ |
| Ordered List | `1. First item`<br>`2. Second item` | ✅ |
| Unordered List | `- First item`<br>`- Second item` | ✅ |

## Extended Syntax
| Element | Markdown Syntax | Supported |
| ------- | --------------- | --------- |
| Horizontal Rule | `---` | ❌ |
| Table | `\| Header 1 \| Header 2 \|`<br>`\| --- \| --- \|`<br>`\| Row 1 \| Row 2 \|` | ❌ |
| Fence Code Block | ``\`json <br> { <br>   &nbsp;&nbsp;&nbsp; "firstName": "John",<br>&nbsp;&nbsp;&nbsp; "lastName": "Smith", <br>&nbsp;&nbsp;&nbsp;  "age": 25<br>}<br>``` | ✅ |
| Footnote | `Sentence [^1]`<br>`[^1]: Footnote text.` | ❌ |
| Custom Footnote | `Sentence [^note]`<br>`[^note]: Footnote text.` | ❌ |
| Heading ID | `## Heading {#heading-id}` | ❌ |
| Definition List | `Term`<br>`: Definition` | ❌ |
| Task List | `- [x] Task 1`<br>`- [ ] Task 2` | ❌ |

## Inline Elements
| Element | Markdown Syntax | Supported |
| ------- | --------------- | --------- |
| Highlight | `==highlighted text==` | ❌ |
| Subscript | `H~2~O` | ❌ |
| Superscript | `2^10^` | ❌ |
| Spoiler | `>! Spoiler` | ❌ (use `\|\|text\|\|`) |

## Miscellaneous
You can also use [HTML tags](https://www.w3schools.com/TAGS/default.asp) in Markdown, as well as [emojis](https://gist.github.com/rxaviers/7360908).

<br>

---

<br>

Other cheat sheets:
- [Markdown Guide](https://www.markdownguide.org/cheat-sheet/)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/markdown-cheatsheet)