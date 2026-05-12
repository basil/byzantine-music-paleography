# Paleography of Byzantine Music

This repository turns Maria Alexandrou's
[Paleography of Byzantine Music](https://repository.kallipos.gr/handle/11419/6487)
into a bilingual, browsable web edition.

The book is an undergraduate textbook on the written memory of Byzantine music:
Greek paleography and codicology, the dating of manuscripts, phonetic and local
notations, Paleo-Byzantine systems, Middle Byzantine notation, the octoechos,
metrophony, variation, melos, gesture, the Great Signs, and the long work of
musical explanation that leads toward the New Method of 1814.

The aim of this project is practical access. The original Greek PDF has been
converted to Markdown, organized as a Hugo site, paired with its extracted
figures, and accompanied by an English translation so readers can move through
the material chapter by chapter instead of wrestling with a monolithic file.

## What's Here

- The Greek text, converted from the Kallipos PDF into Markdown.
- An English translation generated from that Markdown.
- The book's figures and plates, kept alongside the pages that use them.
- A Hugo Book site with Greek as the default language and English available as a
  second language.
- Contents files for quick orientation:
  [Greek](CONTENTS.md) and [English](CONTENTS.en.md).

## Read It

The live site is intended for GitHub Pages:

<https://basil.github.io/byzantine-music-paleography/>

The source material starts in [content](content/):

- Greek chapters: [content/chapters](content/chapters/)
- English chapters: `content/chapters/**/*.en.md`
- Greek appendices: [content/appendices](content/appendices/)
- English appendices: `content/appendices/**/*.en.md`

## Editorial Status

This is a working edition, not a critical edition.

The Markdown conversion and English translation were produced with AI assistance.
They have been cleaned up, but they have not been exhaustively proofread. Treat
the English as a reading aid, not as an authority. When precision matters, read
it beside the original Greek PDF from Kallipos.

Corrections are welcome, especially for OCR mistakes, mistranslations, broken
figures, malformed musical examples, and places where the English smooths over a
technical distinction in the Greek.

## Local Development

This site uses Hugo with the `hugo-book` theme loaded as a Go module.

Prerequisites:

- Hugo Extended
- Go

Run the site locally:

```sh
hugo server
```

Build the static site:

```sh
hugo --gc --minify
```

The GitHub Actions workflow in [.github/workflows/hugo.yaml](.github/workflows/hugo.yaml)
builds the site and deploys it to GitHub Pages from `master`.

## Source and License

Original textbook:

Alexandrou, M. (2017). *Paleography of Byzantine Music* [Undergraduate
textbook]. Kallipos, Open Academic Editions.
<https://dx.doi.org/10.57713/kallipos-684>

The Kallipos record lists the work under the
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
License](https://creativecommons.org/licenses/by-nc-sa/4.0/).
