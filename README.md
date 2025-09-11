<p align="center">
  <img width="400" src="logo-readme.svg">
</p>

Long-form microblog authoring tool with rich text and LaTeX.

## Overview

**LaTweet!** converts LaTeX markup to Unicode for posting on social media platforms. Write mathematical expressions and formatted text that displays correctly on Twitter, Threads, BlueSky, Mastodon, and other microblogging sites.

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
