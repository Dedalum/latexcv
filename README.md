<h1 align="center">
  <img alt="latexcv icon" src="./logo.svg" height="300px" />
  <br />
  LaTex CV and Resume Collection
</h1>

<div align="center">
  <a href="https://github.com/jankapunkt/latexcv/actions/workflows/buildall.yml">
    <img alt="buildall workflow status" src="https://github.com/jankapunkt/latexcv/actions/workflows/buildall.yml/badge.svg">
  </a>
  <a href="http://www.repostatus.org/#active" title="Project Status: Active – The project has reached a stable, usable state and is being actively developed.">
    <img src="http://www.repostatus.org/badges/latest/active.svg" alt="Project Status: Active" />
  </a>
  <img alt="license badge" src="https://img.shields.io/github/license/jankapunkt/latexcv">
</div>

<br />
<br />
<p align="center">
:necktie: A collection of simple and easy to use, yet powerful LaTeX templates for CVs and resumes. All of them are self designed and self implemented and not copied from template collections.
</p>
<p>
Now with support for Chinese, Japanese and Korean character encoding. Setup is only two lines of code! Read more <a href="docs/cjk/README.md">here</a>.
</p>	
<br />

## How to build?

### Using Docker

We now have a Dockerfile you can use to build your latex environment. 
For this you need to have Docker installed on your system.

Get Docker: https://docs.docker.com/get-docker/

We provide scripts for building the image and running the containers, 
so you should fine by simply running the `build.sh` script:

```shell
$ .docker/create_image.sh
```

You should now be able to build CVs simply by providing the folder name:

```shell
$ .docker/build.sh classic
```

Constraints: You need to be in the top-level folder of this project and the image has been created (see prior step).

You can also run a daemon and pass through build commands, suitable if you build many times in sequence:

```shell
$ .docker/daemon.sh
$ .docker/dbuild.sh classic
$ .docker/dbuild.sh modern
$ # ... and so on
```

This has originally been implemented by https://github.com/blang/latex-docker/tree/master

### Manual build

The following guide just briefly describes the requirements and build procedure as there are many ways to install a LaTeX distribution on various OS. Please create an issue, if this part is not helpful.

**Build Requirements**

You will need some minimal Texlive distrubution (The full texlive distribution is nearly 2GB large but you will need only a part of it). A good starting point is here: https://www.latex-project.org/get/#tex-distributions

If you want to install texlive from tug.org instead, you can use this guide: https://tug.org/texlive/

Users of various Linux distrubutions can also install texlive from their repositories.

This repo also contains a `texlive.profile` file in the project root, that can be used to install the minimum required texlive packages when manually installing texlive.


**Build Procedure**


 * Clone or download this project. 
 * Change to a template folder, which contains a `main.tex` file do
 * Edit the `main.tex` according to your CV credentials, optionally change settings and colors etc.
 * Run `pdflatex` (build/compile) 
 - The `main.pdf` should show the output.

