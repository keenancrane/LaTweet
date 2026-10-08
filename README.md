<p align="center">
  <img width="400" src="logo-readme.svg">
</p>

Long-form microblog authoring with rich text and math support.  Use it live at

<https://keenancrane.github.io/LaTweet/>

## Overview

**LaTweet!** converts Markdown and LaTeX markup to Unicode suitable for microblogging sites (Twitter, Threads, BlueSky, Mastodon, etc.), but can also be useful for general conversion to Unicode for other purposes (e.g., communicating math over email).  Longer threads are automatically split into multiple posts, with adjustable per-post character limits, and the ability to add numbering or images to post drafts.  It runs in the browser, providing real-time feedback as you type.

## Installing and Running

To install locally, you just need three files:

- `LaTweet.html`
- `unicode-data.js`
- `logo.svg`

Alternatively, you can clone the whole repository <a href="https://github.com/keenancrane/latweet">github.com/keenancrane/latweet</a>.

You should then be able to open `LaTweet.html` in any modern browser.  No further setup or dependencies need to be installed locally.  However, you must be connected to the internet (in order to load packages via CDN.)

## Usage

### LaTeX Math

Mathematical expressions can be written using standard LaTeX syntax. The tool converts them to Unicode symbols, following the same conventions as <a href="https://www.unicodeit.net/">unicodeit</a>, plus a few extra features.

**Inline math** using `\(...\)` or `$...$`:
```
The quadratic formula is \(x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\).
```
→ The quadratic formula is x = (-b ± √(b² - 4ac))/2a.

**Display math** using `\[...\]` with automatic centering:
```
\[E = mc^2\]
```
→

　　E = mc²

### Text Formatting

Standard LaTeX commands can be used for rich text formatting.  For example:

```
\textbf{Bold text}, \textit{italic text}, and \texttt{monospace code}.
```
→ **Bold text**, *italic text*, and `monospace code`.

### Markdown Formatting

Standard Markdown syntax can be used alongside LaTeX. Markdown is processed only outside of LaTeX expressions.

**Bold text** using `**text**` or `__text__`:
```
**Bold text** and __also bold__.
```
→ **𝐁𝐨𝐥𝐝 𝐭𝐞𝐱𝐭** and **𝐚𝐥𝐬𝐨 𝐛𝐨𝐥𝐝**.

**Italic text** using `*text*` or `_text_`:
```
*Italic text* and _also italic_.
```
→ *𝐼𝑡𝑎𝑙𝑖𝑐 𝑡𝑒𝑥𝑡* and *𝑎𝑙𝑠𝑜 𝑖𝑡𝑎𝑙𝑖𝑐*.

**Bold italic** using `***text***`:
```
***Bold and italic text***.
```
→ ***𝒃𝒐𝒍𝒅 𝒂𝒏𝒅 𝒊𝒕𝒂𝒍𝒊𝒄 𝒕𝒆𝒙𝒕***.

**Inline code** using `` `text` ``:
```
Use `console.log()` to debug.
```
→ Use `𝚌𝚘𝚗𝚜𝚘𝚕𝚎.𝚕𝚘𝚐()` to debug.

**Code blocks** using triple backticks:
````
```
function hello() {
    return "world";
}
```
````
→ 
```
𝚏𝚞𝚗𝚌𝚝𝚒𝚘𝚗 𝚑𝚎𝚕𝚕𝚘() {
    𝚛𝚎𝚝𝚞𝚛𝚗 "𝚠𝚘𝚛𝚕𝚍";
}
```

**Mixing LaTeX and Markdown**: LaTeX expressions are protected from Markdown processing:
```
The formula $E = mc^2$ is **very important** in physics.
```
→ The formula E = mc² is **𝐯𝐞𝐫𝐲 𝐢𝐦𝐩𝐨𝐫𝐭𝐚𝐧𝐭** in physics.

### Formatting Controls

Use the checkboxes in the top toolbar to enable/disable LaTeX and Markdown processing independently:

- **LaTeX formatting**: Enables `\textbf{}`, `$...$`, `\(...\)`, `\[...\]`, etc.
- **Markdown formatting**: Enables `**bold**`, `*italic*`, `` `code` ``, etc.

### Threading

The tool automatically splits long content into multiple posts based on the target platform's character limits (which can be selected from the dropdown at top).

**Auto-splitting**: When you exceed the limit while typing in the final post, a new post is automatically created.

**Smart breaking**: When this option is enabled, text will be broken at word boundaries. URLs and LaTeX expressions are not split across posts.

**Paste & Split**: If a large text block is pasted, and smart breaking is enabled, the pasted input will automatically be split into posts.

### Post Enumeration

Optional numbering can be added to your thread posts.

**Options**:
- `None`: No numbering
- `[<i>/n]`: Shows `[1/n]`, `[2/n]`, etc. (literal "n")
- `[<i>/<N>]`: Shows `[1/3]`, `[2/3]`, `[3/3]` (actual total count)

The enumeration is appended to each post's output and automatically accounted for in the character count.

### Images

One image per post can be attached by dragging and dropping or pasting from clipboard.

**Drag & drop**: Drop image files onto any post box.
**Paste**: Copy an image (screenshot, etc.) and paste with Ctrl/Cmd+V.
**Copy**: Use the image copy button to copy for pasting into social media.
**Remove**: Click the X button in the upper-right corner of the image.

### Backup and Restore

**Copy Source**: Button in the first post header copies all LaTeX input from all posts (separated by newlines).  This source can be pasted back in later to continue editing a thread.

## LaTeX Support

### Math Expressions
```latex
Inline math: \(E = mc^2\) or $F = ma$
Display math: \[a^2 + b^2 = c^2\]
```

### Text Formatting

Plain text:
```latex
\textbf{Bold text}
\textit{Italic text}
\texttt{Monospace text}
\emph{Emphasized text}
```

Math fonts:
```latex
\mathfrak{script}
\mathrm{roman}
```

##  Settings

- **Platform**: Choose character limits for different social media platforms
- **Enumeration**: Add post numbering (`None`, `[<i>/n]`, `[<i>/<N>]`)
- **Smart Breaking**: Intelligent word-boundary splitting (enabled by default)
- **Dark Mode**: Toggle between light and dark themes

## Acknowledgements

LaTweet! adapts code from <a href="https://github.com/svenkreiss/unicodeit">unicodeit</a>, <a href="https://github.com/DenverCoder1/unicode-formatter">unicode-formatter</a>, and <a href="https://github.com/twitter/twitter-text">twitter-text</a>.

