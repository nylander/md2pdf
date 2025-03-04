---
title:  \LARGE \bf Markdown to PDF using Pandoc and \LaTeX
author: "Johan Nylander"
institute: NRM
date: 2025
theme: "metropolis"
classoption:
- aspectratio=169
---

# Note

This README.md file will render slightly different on
[github.com](https://github.com/nylander/md2pdf) compared to the output from using
the scripts in this repository ([`md2pdf`](md2pdf) or [`md2beamer`](md2beamer)).

Normally, one would design the markdown text specifically for the final
target media, but the examples given here are pretty portable. See further
[here](https://pandoc.org/chunkedhtml-demo/8.22-markdown-variants.html).

Take-home note: You can mix markdown, html, and tex!

---

# Prerequisites

On a Debian-based system:

    $ apt install pandoc texlive-xetex

---

# Usage

Plain PDF

    $ ./md2pdf README.md

. . .

Beamer presentation

    $ ./md2beamer README.md

---

# To get slides in beamer

1. Start the slide with a single `#`
2. End the slide with `---`

Note that in plain PDF, `---`, is rendered as a horizontal line.

---

# Change font size and use a footnote

\tiny
tiny text

\scriptsize
scriptsize text

\normalsize
normalsize text, ~~this is over strike~~, *this is italics*, **this in bold**

\Large
Large text with a footnote[^1]

\LARGE
LARGE text

\Huge
Huge text

\normalsize

[^1]: Footnote text

---

# Lists

1. Numbered item
2. Numbered item

- Bullet item
- Bullet item

- [X] Checklist item
- [ ] Checklist item

---

# Table with text alignment

| Some | thing | else |
| :--- | :----: | ---: |
| A | B | C |
| D | E | F |

---

# Insert image

![Figure caption](img/the_general_problem.png){width=70%}\

---

# Another way of inserting and images, and a code block

The image above was inserted using the following syntax (here displayed as **inline code**):
`![Figure caption](img/the_general_problem.png){width=70%}\`

One alternative is to use this text in the markdown file (displayed as a **code block**):

```latex
\begin{figure}
  \begin{center}
    \includegraphics[width=0.7\textwidth]{img/the_general_problem.png}
   \end{center}
\end{figure}
```

---

# Adding images next to each other

![](img/the_general_problem.png){width=40%}\ ![](img/the_general_problem.png){width=40%}

---

# Further reading

- [pandoc](https://pandoc.org)
- [xetex](https://tug.org/xetex)
- [markdown syntax (pandoc)](https://pandoc.org/chunkedhtml-demo/8-pandocs-markdown.html)
- [markdown syntax (github)](https://github.github.com/gfm)
- [markdownguide.org](https://www.markdownguide.org)
- [xkcd](https://xkcd.com)

