# Fancy Beamer Template for Ulm University

[![Static Badge](https://img.shields.io/badge/LaTeX-Inside-blue?style=for-the-badge&labelColor=darkorange&color=white)](https://www.latex-project.org/) [![Static Badge](https://img.shields.io/badge/SP-Institute-blue?style=for-the-badge&labelColor=%23A32638&color=white)](https://www.uni-ulm.de/in/sp/)

Please refer to the underlying [FancyBeamer template][FancyBeamer] for documentation on how to use the template and for more information on the features of the template. 

## Mirrors

This repository is available at the following locations:

- Main repo: <https://gitlab.uni-ulm.de/sp/sp-thesis-package/latex/presentation> (login required).
- Mirror 1: <https://github.com/sp-uulm/FancyBeamerUULM>
- Mirror 2: <https://spgit.informatik.uni-ulm.de/teaching/sp-thesis-package/latex/presentation> (login required)

The mirrors allow for forking on github or internal gitlab.

## Introduction

This is a university specific specialization of the [FancyBeamer][FancyBeamer] template.
While this fork does not add any specific (/fancy) features, [`fancyuulm.sty`](fancyuulm.sty) applies the color palette of Ulm University to the template.
Additionally, [`logos/`](logos/) contains the official logo of Ulm University as well as the logo of the Institute of Software Engineering and Programming Languages&nbsp;(SP) maintaining this fork.

Relevant files include:

- [`fancybeamer.sty`](fancybeamer.sty): The main style file for the [FancyBeamer template][FancyBeamer] template.
- [`fancyuulm.sty`](fancyuulm.sty): The style file for the Ulm University specific color palette.
- [`logos/`](logos/): Contains the official logo of Ulm University and the logo of the Institute of Software Engineering and Programming Languages.

Besides, we have two example presentations (both with sample configurations for a presentation at the SP institute of ulm university):

- [`demo-slides/demo-slides.tex`](demo-slides/demo-slides.tex): A simple presentation showcasing the features of the template ([PDF](https://github.com/sp-uulm/FancyBeamerUULM/tree/gh-pages/demo-slides/demo-slides.pdf)).
- [`empty-slides/empty-slides.tex`](empty-slides/empty-slides.tex): An empty starting point for your own presentation ([PDF](https://github.com/sp-uulm/FancyBeamerUULM/tree/gh-pages/empty-slides/empty-slides.pdf)).

To see the _output PDF_ have a look at the [gh-pages branch](https://github.com/sp-uulm/FancyBeamerUULM/tree/gh-pages).

## How can I obtain the template?

There are two main ways to use this template: [clone-and-own](#-clone-and-own-eg-for-overleaf) and using it as a [submodule](#-submodule-eg-for-a-git-repository). We recommend the latter, as it allows you to easily pull in updates from this repository.

### 📋 Clone and Own (e.g., for Overleaf)

For this you may download the repository as a ZIP file (using the [main version](https://github.com/sp-uulm/FancyBeamerUULM/archive/refs/heads/main.zip)).

Afterward, unpack the ZIP file to the desired directory and start with using the template (see the [base template][FancyBeamer]) We recommend you to copy the [empty slides](empty-slides/empty-slides.tex) to your root directory to start your own presentation.
In general, you neither need the [`demo-slides/`](demo-slides/) nor the [`empty-slides/`](empty-slides/) folder for your presentation so you can safely remove them.

### 🔗 Submodule (e.g., for a Git Repository)

A [git submodule][Git Submodules] is a repository embedded into another and allows you to easily pull in updates from this embedded repository.

1. Creating the submodule.

   Navigate to the root of your repository and add the submodule:

   - With SSH:

   ```shell
   git submodule add git@github.com:sp-uulm/FancyBeamerUULM.git fancy-beamer-uulm
   ```

   - With HTTPS:

   ```shell
   git submodule add https://github.com/sp-uulm/FancyBeamerUULM.git fancy-beamer-uulm
   ```

   Now, there should be a new folder `fancy-beamer-uulm` that contains the slide template:

   ```text
      + /
      | - fancy-beamer-uulm/
      |   | - fancybeamer.sty
      |   | - fancyuulm.sty
      |   | - ...
   ```

   If you have never worked with [submodules][Git Submodules], cloning with the `--recursive` flag is usually sufficient.

2. (Optional) Copy the empty slides to your root directory.

   You can copy the empty slides to your presentation folder:

   ```shell
   cp fancy-beamer-uulm/empty-slides/empty-slides.tex my-presentation.tex
   ```

   If you use `latexmk` you can copy the [_.latexmkrc_](.latexmkrc) file as well:

   ```shell
   cp fancy-beamer-uulm/empty-slides/.latexmkrc .latexmkrc
   ```

   Now you can start editing `my-presentation.tex` and see the [base template][FancyBeamer] for more information.

3. (If necessary) If you want to update the template, you can use the following command:

   ```shell
   git submodule update --remote --merge <path/to/the/submodule>
   ```

   For example:

   ```shell
   git submodule update --remote --merge fancy-beamer-uulm
   ```

   Omitting the path will update all your submodules.

[Git Submodules]: https://git-scm.com/book/en/v2/Git-Tools-Submodules
[FancyBeamer]: https://github.com/Fancy-Templates/FancyBeamer