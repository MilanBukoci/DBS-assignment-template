# DBS Assignment Template — FIIT STU

LaTeX template for student assignment protocols in the **Database Technologies (DBS)** course at the Faculty of 
Informatics and Information Technologies, Slovak University of Technology in Bratislava.

## Project structure

```
.
├── assets/
│   └── logo.png              # FIIT STU logo (used on the cover page)
├── src/
│   ├── main.tex              # Template — edit this file
│   ├── references.bib        # Bibliography entries
│   └── lang/
│       ├── en.tex            # English labels
│       └── sk.tex            # Slovak labels
├── Makefile
└── README.md
```

## Build

Requires `pdflatex` and `bibtex` (TeX Live, MiKTeX, or MacTeX).

```bash
make          # build src/main.pdf
make clean    # remove build artifacts
```

Or upload `src/` and `assets/` to [Overleaf](https://www.overleaf.com/).

## Language

Switch language by changing one line in `main.tex`:

```latex
\input{lang/en}    % English
\input{lang/sk}    % Slovak
```

To add a new language, copy `lang/en.tex`, translate the `\newcommand` values, and `\input` your file.

## Bibliography

Add entries to `src/references.bib` and cite them in text with `\cite{key}`:

```latex
According to the documentation \cite{postgresql-docs}, ...
```

The bibliography is rendered automatically at the end of the document via `\printbibliography`.

## How to use

1. Open `src/main.tex`
2. Set your language (`lang/en` or `lang/sk`)
3. Fill in student details:
   ```latex
   \newcommand{\StudentName}{Name Surname}
   \newcommand{\StudyGroup}{Tuesday 11:00}
   \newcommand{\AssignmentNumber}{1}
   \newcommand{\AssignmentTitle}{Assignment Title}
   \newcommand{\AcademicYear}{2025/2026}
   ```
4. Add sections as needed:
   ```latex
   \section{Your Section Title}

   Your content here.
   ```
5. Add references to `references.bib`
6. Run `make` and submit the PDF

---
![](assets/fiit.png)

Made with ❤️ and ☕️ FIIT STU (c) 2022-2026
