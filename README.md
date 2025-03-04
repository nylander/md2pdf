---
title:  \LARGE \bf Markdown to PDF using Pandoc and \LaTeX
author: "Johan Nylander"
institute: NRM
date: 2025
theme: "metropolis"
classoption:
- aspectratio=169
---

# Prerequisites

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

- [ ] Checklist item
- [ ] Checklist item

---

# Table with text alignment

| Some | thing | else |
| :--- | :----: | ---: |
| A | B | C |
| D | E | F |

---

# Insert image

![Figure text.](img/the_general_problem.png){width=70%}

---

# Another way of inserting and images, and a code block

Displayed as a code block:

```latex
\begin{figure}
  \begin{center}
    \includegraphics[width=0.7\textwidth]{img/the_general_problem.png}
   \end{center}
\end{figure}
```

The other way of inserting the image was done by (here displayed as inline code):
`![Figure text.](img/the_general_problem.png){width=60%}`

---

# Adding images next to each other

![](img/the_general_problem.png){width=40%}\ ![](img/the_general_problem.png){width=40%}

---

# Further reading

- [pandoc](https://pandoc.org)
- [xetex](https://tug.org/xetex)
- [markdown syntax (github flavored)](https://github.github.com/gfm)
- [markdownguide.org](https://www.markdownguide.org)
- [xkcd](https://xkcd.com)

