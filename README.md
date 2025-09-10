<p align="center">
  <img width="400" src="logo-readme.svg">
</p>

Long-form microblog authoring tool with rich text and LaTeX.

## Overview

**LaTweet** is a long-form microblog authoring tool that helps you write threaded posts with rich text formatting and LaTeX mathematical expressions. Perfect for academics, researchers, and anyone who needs to share complex content across Twitter, Threads, BlueSky, Mastodon, and other microblogging platforms.

## Running

Should work in most browsers with JavaScript enabled. No installation required - just open `LaTweet.html` in your browser!

## Features

### **Rich Text & Math Support**
- **LaTeX Math**: Inline math with `\(...\)` or `$...$`, display math with `\[...\]`
- **Text Formatting**: Bold (`\textbf{}`), italic (`\textit{}`), monospace (`\texttt{}`), and more
- **Unicode Conversion**: Automatically converts LaTeX to Unicode symbols for universal compatibility
- **Real-time Preview**: See your formatted output instantly as you type

### **Smart Threading**
- **Auto-splitting**: Automatically breaks long content into multiple posts
- **Character Limits**: Supports platform-specific limits (Twitter 280, Threads/Mastodon 500, etc.)
- **Smart Breaking**: Respects word boundaries and never breaks LaTeX expressions
- **Manual Control**: Add, delete, and reorder posts anywhere in your thread

### **Quality of Life**
- **Enumeration**: Optionally number your posts with `[1/n]` or `[1/3]` patterns
- **Clickable URLs**: URLs automatically become clickable links in the preview
- **Copy to Clipboard**: One-click copying of formatted text
- **Paste & Split**: Paste large text blocks and automatically split into threads
- **Syntax Highlighting**: CodeMirror editor with LaTeX syntax highlighting

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
