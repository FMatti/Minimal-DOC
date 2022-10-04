![](https://img.shields.io/badge/licence-MIT-green?style=flat-square)
![](https://img.shields.io/badge/language-LaTeX2e-blue?style=flat-square)

# Minimal-CV
Minimal template for typesetting a report and a presentation in LaTeX.

## Previews

Sample version of a report:

| Title page | Sample page |
:-------------------------:|:-------------------------:|
![](https://user-images.githubusercontent.com/79205741/193786926-80a56c9e-ed57-46c6-84bc-d148b8841973.png) | ![](https://user-images.githubusercontent.com/79205741/193786941-8e5e2518-1db4-4515-9163-5864c7f418c2.png)

Sample version of a presentation:

| Title slide | Sample slide |
:-------------------------:|:-------------------------:|
![](https://user-images.githubusercontent.com/79205741/193787019-5e724c16-9ebb-408f-9d12-d511af9a302d.png) | ![](https://user-images.githubusercontent.com/79205741/193787014-26fc6ff9-5edf-4c80-9cb8-28afffec66ee.png)

## Usage
To build a pdf version of the report and the presentation simply run the following commands:

    git clone https://github.com/FMatti/Minimal-DOC.git
    cd Minimal-DOC
    pdflatex Minimal-REP.tex; bibtex Minimal-REP.tex; pdflatex Minimal-REP.tex; pdflatex Minimal-REP.tex;
    pdflatex Minimal-PRE.tex; bibtex Minimal-REP.tex; pdflatex Minimal-REP.tex; pdflatex Minimal-REP.tex;

## Closing words

The template is dedicated (in honor and mockery) to the one and only Carl Friedrich Gauss whose work (including the Gauss-Bonnet theorem) and mentality has never failed to inspire me on my academic journey throughout the last couple of years.
