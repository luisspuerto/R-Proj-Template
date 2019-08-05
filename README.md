[[[[#]]]] Template for R Analysis Projects

![https://img.shields.io/badge/Purpose-Template-red.svg](https://img.shields.io/badge/Purpose-Template-red.svg) 
[![https://img.shields.io/badge/Lang-R-blue.svg](https://img.shields.io/badge/Lang-R-blue.svg)](https://www.r-project.org) 
[![https://img.shields.io/badge/Lang-RMarkdown-blue.svg](https://img.shields.io/badge/Lang-RMarkdown-blue.svg)](http://rmarkdown.rstudio.com) 
[![https://img.shields.io/badge/Lang-Markdown-yellowgreen.svg](https://img.shields.io/badge/Lang-Markdown-yellowgreen.svg)](https://en.wikipedia.org/wiki/Markdown) 
[![https://img.shields.io/badge/Apps-RStudio-blue.svg](https://img.shields.io/badge/Apps-RStudio-blue.svg)](https://www.rstudio.com) 
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) 
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**Table of Contents**

<!-- MarkdownTOC -->

- [Introduction](#introduction)
- [How to use this template](#how-to-use-this-template)
- [Contents description](#contents-description)
    - [Files](#files)
        - [README.md](#readmemd)
        - [Licenses & licensing](#licenses--licensing)
        - [TODO.md](#todomd)
        - [CONTRIBUTING.md](#contributingmd)
        - [.gitignore](#gitignore)
        - [.gitkeep\(s\)](#gitkeeps)
    - [Folders](#folders)
- [Script template headers](#script-template-headers)
- [Prerequisites & recommendations](#prerequisites--recommendations)
- [Contributing, cloning or forking this template](#contributing-cloning-or-forking-this-template)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Acknowledgments](#acknowledgments)
    - [ProjectTemplate](#projecttemplate)

<!-- /MarkdownTOC -->


## Introduction 

This pretends to be a template for projects carried out mainly in R language and mainly over RStudio, but that IDE isn't necessary and of course you can use other languages like Python and C++. 

The idea is to have a common structure in all the projects so it is recognize by everyone, so everyone knows more or less where things are. 

The template right now is heavily biased towards macOS, at least explanations and direction, because it's my working environment at the moment. If you want to make contributions related to Windows and Linux, you're very much welcomed. 

## How to use this template

You can clone, fork or directly download this project to use it. If you want to clone it using Git on the shell use the following command in the folder where you want to clone. 

```
$ git clone https://github.com/luispuerto/R-Proj-Template.git
```

Once you have the files you can **copy** the `/Template` folder elsewhere —in your working folder, like `Coding` or `MyRepos` or whatever you use to store your R projects— and rename it for your project. You can then begin to customize the template to your and/or your project's needs. 

These are the suggested next steps: 

1. Start a git repo in the root of your project `git init`. Edit also the `.gitignore` file to your needs/liking. If you are on macOS I recommend to set [this][1] as your global `.gitignore` [this way][2]. You can also set up something like [this][3]. 
2. Choose a license for your code and/or your content from the [`LicenseTemplates/`][LicenseTemplates/] folder. Check the [Licenses & licensing](#licenses--licensing) section in this document to find out more. You can skip this step if you are not going to share your project just yet. 
3. Delete whatever you are not going to need, like for example [`.gitkeep`](#gitkeep) files. This can be the first step before you fire up your git repo. Really depends how you want to track your first steps.  
4. Edit the README file describing what the project is about. Even when it's a loose description that you'll expand later. 

## Contents description

This is a short description of the contents of the template. 

### Files

#### README.md

The `README.md` file is one of the more important, if not the most, files in the documentation of your project. This files should contain the description of your project, what is the purpose, how to use, how to interact and any other relevant information about it. 

Here there is provided a readme template that is mainly thought for software purposes, but don't forget that [your scripts are software too][11], in the same was it's your operative system, or your word processor. They are just a really simple piece of software.  

I recommend you to create as complete as possible readme for your project, so other, or even a future yourself, can understand it better. 

As you can see there are series of badges on the top of the readme template. There are a list of the most common one for licenses in the [`LicenseTemplates/license-badges.md`][LicenseBadges] file, but you can build your own on [shields.io][]

#### Licenses & licensing

Licensing your project isn't that important is you are working stand-alone, or in _safe context_ —whatever that means to you. But in the moment you share your code with others and other start to make contributions, things start to get complicated. For that reason, it's better state from the very beginning  what are _conditions_ of your software. Bear in mind that, while you are working _solo_ and without sharing your code, you have all the says, so you can easily change the license if you want. In the moment, your code is in the wild and someone make a contribution, they own that piece of code and they have a say if you want to change the license. 

There are two files related to licenses, `LICENSE.md` and `LICENSE4CONTENT.md`. `LICENSE.md` is relate to the code and `LICENSE4CONTENT.md` is relate to the content that isn't code. The idea is that the code and the content of your project could —and perhaps should— have different licenses since they are sometimes different entities. Licenses like [GPL or MIT or so][OpenSourceLicense] aren't really suitable for media content, and licenses like [Creative Commons][CreativeCommonsLicense] aren't really suitable for code.  

Please take into account that [IANAL][] and licensing R code sometimes is something **_controversial_**. I've seen long threads where the issue is discussed —even sometimes too passionately— to finally don't reach any clear conclusion. The problem lie in that R has a [`GPL-2-or-later` license][GPL-2-or-later] and it isn't clear if the scripts have to have the same license, since they need R to work and they aren't independent from it. 

>If you are relying on packages, this likely means that you are relying on other R scripts which are going to be interpreted as well. Your program, by relying on these scripts is a derivative of them. Thus, you need to license your whole program (the packages you rely on + the part you wrote) under GPL as well. [(Source)][5]

>Linking a GPL covered work statically or dynamically with other modules is making a combined work based on the GPL covered work. Thus, the terms and conditions of the GNU General Public License cover the whole combination. [(Source)][12]

You can see here some of the debate: 

- [License for R scripts][5]
- [If my R package uses GPL packages, does mine automatically inherit GPL?][6]
- [Guidance on R code licensing][7]
- [Recent discussion in R help][8]

However, [IMHO][], and again [IANAL][], you can choose whatever license you want for your code, if and when, you don't include any previously licensed code, and that is **a big if**. The problem is if you intertwine your code with any other code that has a GPL-2 or 3, you are going to need to license everything as GPL-2 or 3 as it's stated in those licenses, since it's a derivative work and you are distributing that code with yours. For instance:

- If you just call R base or any or the installed packages in your system. I think that's fine and you can license your code in whatever way you want. 
- If you copy some function or code from a package with GPL-2 or 3, and you use it in your code, customized or nor, it's a derivative work, so you need to license accordingly.
- You use [Rcpp][Rcpp-lic], it's a derivative work, so your package has to have the same license of the previous packages.  

Anyhow, I encourage you to choose whatever **[Open Source license][OpenSourceLicense]** you consider is suitable for your work, even more if it's [GPL compatible][GPLCompatible] although I understand it isn't always possible. If you decide —or have to— to take the latter road, I recommend you talk to your —or your institution— [IP][] lawyer. 

Related to the content, more or less the same. I encourage you to use whatever **[Creative Commons license][CreativeCommonsLicense]** you consider is the best for you, but again I understand it isn't always possible. 

Perhaps you can check some of these resources to make an informed decision: 

- [License Selector][LicenseSelector]
- [TLDRLeagal][]
- [The Legal Side of Open Source][9]
- About [licenses][r-pckg-lic] on "[R packages][r-pckg-book]" by Hadley Wickham
- [Open Data on Stack Exchange][OpenDataOnStackExchange]
- [Open Source on Stack Exchange][OpenSourceOnStackExchange]

#### TODO.md

This is the _classic TODO file_ where you can annotate what is pending to-do in your project so others can easily know, even more if you are working with more people. If you upload it to GitHub or similar, perhaps you can use the [Issues][] and/or [Projects][] sections instead. Up to you! 

#### CONTRIBUTING.md

In this file you state how others can contribute to your project and what is the code of conduct for the people contributing to it. The text is adapted from the [Contributor Covenant][ContriburorCovenant], version 1.4, available at <https://www.contributor-covenant.org/version/1/4/code-of-conduct.html>.  

#### .gitignore

This is the standard [`.gitignore`][.gitignore] file for R projects that use RSturdio. Please fell free to add here whatever you think it's suitable to ignore. It's really recommended to have one from the very beginning in your project managed with Git if you are going to use RStudio, so you don't commit files that aren't worth to commit like `.Rhistory` or `.RData` that should be temporal files. 

#### .gitkeep(s)

These are [not standard git files][10] but they are around, so Git can keep track of empty folders. You can delete them if you don't use them running the following command on the root of your project on the shell: 

```shell
$ find . -name '.gitkeep' -delete 
```

### Folders 

Inside of each of the folders there is a small `README.md` file that explain a little bit about the purpose of the folder and how to store the files in there. That same readme could serve to create a small description of the files you are going to put in there, so when someone opens the folder on their computer or in a Git server could know at glance what is in there and how it's store. 

You can delete that readme files if you don't want to use them typing on the root of your project:  

```shell
$ find ./*/ -name 'README.md' -delete 
```

- **[code/][]**: Your coding scripts where you analyze your data. 
- **[data/][]**: Raw or original data. 
- **[doc/][]**: Project documents.
- **[figs/][]**: Figures and other images you generate. 
- **[notes/][]**: Notes of the project and research diary. 
- **[output/][]**: Other outputs, like CSVs or ESRI shapes to share data.
- **[R/][]**: Scripts with functions created for this project.
- **[var/][]**: Stores your processed of intermediate data or variables. 

## Script template headers

Besides of having a standard folder structure it's also recommendable that each script have a header with some information about the script, like name, author, version of the software where it was developed, packages that uses, project name, etc. 

This way you are sure that even if the script gets strander, you, or someone, are going to know what the script is about and where it belongs. 

You can know more about them [here][scriptheaders]. 

## Prerequisites & recommendations

The clear prerequisite for this project is: 

- [**R**][RProject]: Software environment for statistical computing and graphics. (Do I really need to explain what is about the [R project][RProject]). You can install from [CRAN][], Homebrew or build it from [source][Rsource]. 

Then, I recommend you to get. 

- **[Git][]**: Git is a free and open source distributed version control system. 
- **[RStudio][]**: A free and open-source integrated development environment (IDE) for R.
- **[Sublime Tex][SublimeTex]**: Advanced text editor for catching up some of the shortcomings of RStudio. Sublime Text is my personal liking, but there other advanced text editors out there like [Atom][] or [Visual Studio Code][VisualStudioCode] and they are free. 
- **[Typora][]**: Markdown editor. Sometimes I use this wonderful markdown editor to edit my documentation since it's a [WYSIWYG][] lightweight editor. 
- **[ProjectTemplate][]**: ProjectTemplate is a system for automating the thoughtless parts of a data analysis project. It's a solid call if you want to go even further in the automation process of providing R with a template for projects. 

For the snippets in template for script headers: 

- **[RStudio][]**: A free and open-source integrated development environment (IDE) for R.
- **[`git2r` R package][git2r]**: The `git2r` package gives you programmatic access to Git repositories from R. Internally the package uses the libgit2 library which is a pure C implementation of the Git core methods.

## Contributing, cloning or forking this template

Please feel free to comment or even contribute to this project in anyway you want to this template, this is just a beginning and I want to make it as useful as possible to anyone. 

Please read [CONTRIBUTING.md][] for details on the code of conduct, and the process for submitting pull requests.

## Versioning 

I use [SemVer][] for versioning. For the versions available, see the [tags on this repository][TagsOnThisRepository].

## Authors

- **Luis Puerto ([@luispuerto][])**: Initial work. 

You can see the full list of [contributors][] who participated in this project. 

## License

The _code_ of this project is licensed under GNU General Public License v3.0 `GPL-3.0` –see the [LICENSE.md](LICENSE.md) file for more details. The rest of the content of this project is licensed under Attribution-NonCommercial-ShareAlike 4.0 International `CC-BY-NC-SA-4.0` –see the [LICENSE4CONTENT.md](LICENSE4CONTENT.md) for more details.

## Acknowledgments

I've been inspired to create this template after I've read the following posts in the blog [Nice R Coding](https://richfitz.github.io/) of [@richfitz](https://github.com/richfitz)

* [Why I want to write nice R code][4]
* [Designing projects][13]
* [Organizing the project directory][14]

### ProjectTemplate 

I know about the [ProjectTemplate][] and I think it's really impressive how complex a R project can be and how detailed that template is. However, I find it too complicated for my needs and I think other people find it too, whether because they are starting in R or they don't do that complicated projects everyday. 

This template tries to be an intermediate template for people that doesn't need to automate that much when they are scripting in R, but they would like to have some kind of template to help them every time they create a new project and keep common structure in all their projects.

Anyhow, [ProjectTemplate][] can be [customized][PTcustom] so feel free to adapt this template as a ProjectTemplate template —and share it later. :slightly_smiling_face:


<!--This is where the variables / references of the document are found. -->


[1]: https://github.com/github/gitignore/blob/master/Global/macOS.gitignore
[2]: https://timleland.com/global-git-ignore/
[3]: https://stackoverflow.com/questions/16658087/automatically-add-gitignore-and-hooks-on-git-init
[LicenseTemplates/]: LicenseTemplates/
[11]: http://www.jonzelner.net/statistics/make/docker/reproducibility/2016/05/31/script-is-a-program/
[LicenseBadges]: LicenseTemplates/license-badges.md
[shields.io]: https://shields.io
[OpenSourceLicense]: https://en.wikipedia.org/wiki/Open-source_license
[CreativeCommonsLicense]: https://en.wikipedia.org/wiki/Creative_Commons_license
[IANAL]: https://www.urbandictionary.com/define.php?term=IANAL
[GPL-2-or-later]: https://spdx.org/licenses/GPL-2.0-or-later.html#licenseText
[5]: https://opensource.stackexchange.com/questions/4666/license-for-r-scripts
[12]: https://www.gnu.org/licenses/gpl-faq.html#GPLStaticVsDynamic
[6]: https://opensource.stackexchange.com/questions/4414/if-my-r-package-uses-gpl-packages-does-mine-automatically-inherit-gpl
[7]: https://github.com/ropensci/unconf17/issues/32
[8]: http://r.789695.n4.nabble.com/Regarding-R-licensing-usage-guidance-td4758401.html
[IMHO]: https://www.urbandictionary.com/define.php?term=IMHO
[Rcpp-lic]: http://dirk.eddelbuettel.com/code/rcpp/Rcpp-FAQ.pdf
[GPLCompatible]: https://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses
[IP]: https://en.wikipedia.org/wiki/Intellectual_property
[LicenseSelector]: https://ufal.github.io/public-license-selector
[TLDRLeagal]: https://tldrlegal.com/
[9]: https://opensource.guide/legal/
[r-pckg-lic]: http://r-pkgs.had.co.nz/description.html#license 
[r-pckg-book]: http://r-pkgs.had.co.nz/
[OpenDataOnStackExchange]: https://opendata.stackexchange.com/
[OpenSourceOnStackExchange]: https://opensource.stackexchange.com/
[ContriburorCovenant]: https://www.contributor-covenant.org
[.gitignore]: https://git-scm.com/docs/gitignore
[10]: https://stackoverflow.com/questions/7229885/what-are-the-differences-between-gitignore-and-gitkeep
[code/]: template/code/
[data/]: template/data/
[doc/]: template/doc/
[figs/]: template/figs/
[notes/]: template/notes/
[output/]: template/output/
[R/]: template/R/
[var/]: template/var/
[scriptheaders]: Script%20Template%20Header.md
[RProject]: https://www.r-project.org
[CRAN]: https://cloud.r-project.org/
[Rsource]: https://cran.r-project.org/doc/manuals/r-release/R-admin.html
[Git]: https://git-scm.com
[RStudio]: https://www.rstudio.com
[SublimeTex]: https://www.sublimetext.com 
[Atom]: https://atom.io
[VisualStudioCode]: https://code.visualstudio.com
[Typora]: https://typora.io
[WYSIWYG]: https://en.wikipedia.org/wiki/WYSIWYG
[ProjectTemplate]: http://projecttemplate.net/
[CONTRIBUTING.md]: CONTRIBUTING.md
[SemVer]: http://semver.org/
[TagsOnThisRepository]: https://github.com/luispuerto/R-Proj-Template/tags
[@luispuerto]: https://github.com/luispuerto
[contributors]: https://github.com/luispuerto/R-Proj-Template/contributors
[4]: https://nicercode.github.io/blog/2013-04-05-why-nice-code/
[PTcustom]: http://projecttemplate.net/custom_templates.html
[13]: https://nicercode.github.io/blog/2013-04-05-projects/
[14]: https://nicercode.github.io/blog/2013-05-17-organising-my-project/
[Issues]: https://github.com/luispuerto/R-Proj-Template/issues
[Projects]: https://github.com/luispuerto/R-Proj-Template/projects
[git2r]: https://github.com/ropensci/git2r

