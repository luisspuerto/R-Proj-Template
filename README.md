# Template for R Analysis Projects

![https://img.shields.io/badge/Purpose-Template-red.svg](https://img.shields.io/badge/Purpose-Template-red.svg) [![https://img.shields.io/badge/Lang-R-blue.svg](https://img.shields.io/badge/Lang-R-blue.svg)](https://www.r-project.org) [![https://img.shields.io/badge/Lang-RMarkdown-blue.svg](https://img.shields.io/badge/Lang-RMarkdown-blue.svg)](http://rmarkdown.rstudio.com) [![https://img.shields.io/badge/Lang-Markdown-yellowgreen.svg](https://img.shields.io/badge/Lang-Markdown-yellowgreen.svg)](https://en.wikipedia.org/wiki/Markdown) [![https://img.shields.io/badge/Apps-RStudio-blue.svg](https://img.shields.io/badge/Apps-RStudio-blue.svg)](https://www.rstudio.com) [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


## Introduction 


This is a small outline of folders of the template.  

| Folder                                 | Function                                                        |
| --------                               | -------------                                                   |
| [code/](code/)                         | Stores your code scripts.                                       |
| [data/](data/)                         | Stores raw or original data.                                    |
| [doc/](doc/)                           | Documents generated during the project.                         |
| [figs/](figs/)                         | Figures and graphs, or other kind of images.                    |
| [LicenseTemplates/](LicenseTemplates/) | Templates in markdown format for licenses for code and content. |
| [notes/](notes/)                       | Notes or diary documents.                                       |
| [output/](output/)                     | Other outputs, like CSVs to share data.                         |
| [R/](R/)                               | Scripts with functions created for this project.                |
| [var/](var/)                           | Stores your processed of intermediate data or variables.        |

Small outline of the files.

| File                                                 | Function                                                      |
| ---------------------------------------------------- | ------------------------------------------------------------  |
| [CONTRIBUTING.md](CONTRIBUTING-template.md)          | A template file to explain how to contribute to your project. |
| [LICENSE.md](LICENSE.md)                             | The license I attribute to the code in this project.          |
| [LICENSE4CONTENT.md](LICENSE4CONTENT.md)             | The license of the media files of this project.               |
| [README.md](README-template.md)                      | A README file template to you to modify for your project.     |
| [TODO.md](TODO-template.md)                          | A TODO file you can use in your project.                      |

## How to use this template

You can clone, fork or directly download this project to use it. If you want to clone it using Git on the shell use the following command in the folder where you want to clone. 

```
git clone https://github.com/luisspuerto/R-Proj-Template.git
```

Once you have the files I recommend you to choose a license for your the code and the content of your project, even more if you are going to share the project in GitHub, and then delete the `LicenseTemplates/` folder. Check the [License](#license) section in this document to find out more.

I recommend you delete the files related to this project itself and then use the `-template` ones in your project. 


## Contributing, cloning or forking this template

Please fell free to comment or even contribute to this project in anyway you want to this template, this is just a beginning and I want to make as useful as possible to anyone. 

I've included a CONTRIBUTING document in this template project, as well a contributing document template. 

This is a small code of conduct that explain how to contribute to this project. It's adapted from the [Contributor Covenant][homepage], version 1.4, available at https://www.contributor-covenant.org/version/1/4/code-of-conduct.html 

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```


## Built With

* [R](https://www.r-project.org) - Software environment for statistical computing and graphics 
* [RStudio](https://maven.apache.org/) - a free and open-source integrated development environment (IDE) for R
* [MacDown](https://macdown.uranusjr.com) - Markdown Editor


## Contributing

Please read [CONTRIBUTING.md](/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License

The code of this project is licensed under GNU General Public License v3.0 –see the [LICENSE.md](LICENSE.md) file for more details. The rest of the content of this project is licensed under Attribution-NonCommercial-ShareAlike 4.0 International –see the  [LICENSE4CONTENT.md](LICENSE4CONTENT.md) for more details. 

It seems that the license for R code is something tricky. R is distributed under GNU General Public License v2.0 and some people argue that since R script are a derivative work from R libraries you need to distribute you R scripts under the same license. 

## Acknowledgments

I've been inspired to create this template after I've read the following posts in the blog [Nice R Coding](https://richfitz.github.io/) of [@richfitz](https://github.com/richfitz)

* [Why I want to write nice R code](https://nicercode.github.io/blog/2013-04-05-why-nice-code/)
* [Designing projects](https://nicercode.github.io/blog/2013-04-05-projects/)
* [Organizing the project directory](https://nicercode.github.io/blog/2013-05-17-organising-my-project/)

I know about the [ProjectTemplate](http://projecttemplate.net/) and I think it's really impressive how complex a R project can be and how detailed that template is. However, I find it too complicated for my needs and for a lot of people starting in R or don't do that complicated project everyday. 

This template tries to be an intermediate template for people that doesn't need to automate that much when they are scripting in R, but they would like to have some kind of template to help them every time they create a new project and keep common structure in all their projects.


<!--This is where the variables of the document are found. -->

[homepage]:https://www.contributor-covenant.org