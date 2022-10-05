![](https://img.shields.io/badge/licence-MIT-green?style=flat-square)
![](https://img.shields.io/badge/language-LaTeX2e-blue?style=flat-square)

# Minimal-CV
Minimal template for typesetting a report (REP) and a presentation (PRE) in LaTeX.

## Showcase
The files `Minimal-REP.tex` and `Minimal-PRE.tex` contain, respectively, a sample report and presentation typeset using my Minimal theme.

### Sample report
| Title page | Sample page |
:-------------------------:|:-------------------------:|
![](https://user-images.githubusercontent.com/79205741/193786926-80a56c9e-ed57-46c6-84bc-d148b8841973.png) | ![](https://user-images.githubusercontent.com/79205741/193786941-8e5e2518-1db4-4515-9163-5864c7f418c2.png)

### Sample presentation
| Title slide | Sample slide |
:-------------------------:|:-------------------------:|
![](https://user-images.githubusercontent.com/79205741/193787019-5e724c16-9ebb-408f-9d12-d511af9a302d.png) | ![](https://user-images.githubusercontent.com/79205741/193787014-26fc6ff9-5edf-4c80-9cb8-28afffec66ee.png)

## Usage
To build a pdf version of the report and the presentation simply run the following commands (assuming you have both `pdflatex` and `bibtex` installed for instance from a [MiKTeX](https://miktex.org/download) distribution):

    git clone https://github.com/FMatti/Minimal-DOC.git
    cd Minimal-DOC
    pdflatex Minimal-REP.tex; bibtex Minimal-REP.tex; pdflatex Minimal-REP.tex; pdflatex Minimal-REP.tex;
    pdflatex Minimal-PRE.tex; bibtex Minimal-PRE.tex; pdflatex Minimal-PRE.tex; pdflatex Minimal-PRE.tex;

## Becoming a VSCode poweruser...
1. If not already done, install [VSCode](https://code.visualstudio.com/Download).
2. If not already done, install a LaTeX distribution (e.g. [MiKTeX](https://miktex.org/download)).
3. In VSCode go to the `Extensions` tab, search for `LaTeX Workshop`, and install this extension.
4. Go to `File > Preferences > Configure User Snippets > latex` and insert the contents of [this snippet](https://gist.github.com/FMatti/8050a519f57cba00a1e16accd4eaca96) into the `latex.json` file that you have just opened. You have now access to a variety of code snippets which will be prompted once you type a `\` character in a `.tex` document.
5. Press `ctrl + shift + p` to open the command palette. Type `Preferences: Open User Settings (JSON)` and press `enter`. In the `settings.json` file then navigate to the variable `"latex-workshop.latex.recipes"` and add a the following recipe below any previously defined recipes:
    {
        "name": "pdflatex ➞ bibtex ➞ pdflatex × 2",
        "tools": [
            "pdflatex", "bibtex", "pdflatex", "pdflatex"
        ]
    },
6. Open a `.tex` file and press `ctrl + shift + p` to open the command palette. Type `LaTeX Workshop: Build with recipe`, select the recipe named `pdflatex ➞ bibtex ➞ pdflatex × 2` and execute it.
7. To view the generated `.pdf` file, press `ctrl + shift + p` to open the command palette, type `LaTeX Workshop: View LaTeX PDF in VSCode tab` and press `enter`.

After each time you make changes to the `.tex` file, you can partially recompile the file by pressing `ctrl + s` to see the changes applied to the `.pdf` (if you do any changes to the bibliography, you will need to follow the full compilation instructions in point 6.)

## Closing words

The template is dedicated (in honor and mockery) to the one and only Carl Friedrich Gauss whose work and mentality has never failed to inspire me on my academic journey throughout the last couple of years.
