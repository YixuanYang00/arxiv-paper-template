# arXiv Paper Template

A reusable LaTeX article template for research manuscripts and arXiv preprints.

- [TeX source](arxiv_paper_template.tex)
- [PDF preview](arxiv_paper_template.pdf)

## Features

- A4 paper, 10pt text and 1-inch margins.
- Author–year citations with `natbib`: `\citet{key}` for narrative citations
  and `\citep{key}` for parenthetical citations.
- Deep-blue literature citations and URLs: RGB `(0, 0.19, 0.56)`.
- Dark-red internal reference numbers: RGB `(0.7, 0, 0)`.
- Theorem, lemma, proposition, corollary, assumption, definition and remark
  environments with named cross-references.
- Algorithm, figure and table examples.
- References followed by an automatically generated appendix-only contents
  page. Appendix contents and PDF bookmarks use dark red.
- A self-contained example bibliography and figure placeholder.

## Use

Use GitHub's **Use this template** button to start a new repository, or copy
`arxiv_paper_template.tex` into your paper project. Replace the sample title,
content and bibliography with your own material.

Compile with a TeX Live or MiKTeX installation:

```sh
latexmk -pdf -synctex=1 arxiv_paper_template.tex
```

Alternatively, run `pdflatex arxiv_paper_template.tex` at least twice to
refresh citations and appendix page numbers.

The example compiles as a single file. If switching to a `.bib` database,
use an author–year-compatible bibliography style, such as `plainnat`, as
shown in the source comments.

## Customize

Edit `ReferenceBlue` and `CrossReferenceRed` in the **COLORS AND LINKS**
block to change the palette. The main article text, equations and captions
stay black; internal reference numbers use dark red, and literature links
use deep blue.

The PDF is tracked as a preview. Regenerate it after editing the TeX source.
Temporary LaTeX compilation files are excluded by `.gitignore`.
