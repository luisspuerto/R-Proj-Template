# Templates for R Scripts

These are templates for the R scripts' headers. You can incorporate them to the RStudio snippets, so you can easily insert them when you start a new script typing for instance `header.long` and then press `Tab` and the full header will get inserted. 

**Table of Contents**

<!-- MarkdownTOC -->

- [Dependencies](#dependencies)
- [Fields explanation](#fields-explanation)
- [Long one](#long-one)
- [Short one](#short-one)
- [Snippets for RStudio](#snippets-for-rstudio)
    - [Updating fields](#updating-fields)
        - [Date & Update](#date--update)
        - [System](#system)
        - [RVersion](#rversion)

<!-- /MarkdownTOC -->

## Dependencies

The only dependencies are [RStudio][] and the package [`git2r`][git2r] if you want to fully enjoy the snippets, since the snippets check if the current working directory is a git repository. If it's not, a `Version` field will be added to the header.  

```r 
install.package("git2r")
```

## Fields explanation

- `Title`: Descriptive title of the script. Try to be as concise as possible. 
- `Author/s`: The main authors of the script. On the contributors list you'll find the full list of authors. 
- `Username/s`: This username of the authors, in the same order as the authors on the server —GitHub, GitLab, Bitbucket...— where the script is hosted. 
- `Email/s`: Emails of the authors in the same order as the authors. 
- `Date`: Creation date of the script. This date is automatically inserted the first time you insert the header with the snippet. Check [updating fields](#updating-fields) section for instruction about how to update. 
- `Updated`: When was the last time the script was updated after it was created. Check [updating fields](#updating-fields) section for instruction about how to update.
- `Version`: The version of the script. This field is only necessary when there is not VCS in place. 
- `Project`: The project where this script belongs. The first time you add the script the name of the working directory is going to be inserted here. You can —you should— change to something more meaningful if you want. 
- `Description`: A small and concise description of what the script does and/or which is it's purpose.
- `System`: In which system was the script created and in which ones have been tested. This field is automatically populated when you insert the snippet. Check [updating fields](#updating-fields) section for instruction about how to update.   
- `R version`:  Last version of R where the script was working as expected. This filed is automatically populated when you insert the snippet. Check [updating fields](#updating-fields) section for instruction about how to update.
- `License`: What is the license of the script. I license all my script with `GPL-3`, but you can change this to whatever you want. 
- `Packages & Sources`: Here is were you call all the packages or script that are necessary to run the script. It's recommendable to at least give a reason why you load that specific source or package. 
    + `Loading all functions in R/`: This _just_ loads all the functions you have on the `R/` folder. You can disable or delete this if you just want to load specific ones, or you don't use the `R/` folder. 

Some of the fields, like date or update, or even the authors and usernames  are perhaps a little bit redundant or even unnecessary if you are _running the show_ with the help of a VCS like git, where all that data usually are register. However, and IMHO, it's good to keep a little bit of old fashion meta-data for two reasons: 

1. Sometimes scripts get stranded, they are copied, or moved, from their original working or project directories, so they lose the connection with the meta-data provided by the VCS.
2. It helps to have an idea _at glance_ of what is the script about, who created it and so on. 

## Long one

```r
#!/usr/bin/env Rscript 
# Header ####
# Title       : Template for R Scripts
# Author/s    : Name Surname
# Username/s  : @username
# Email/s     : your.email@email.com
# Date        : Fri, 02 Aug 2019
# Updated     : Not yet
# Version     : 0.1 <- This field only appears if there isn't git repo in WD.
# Project     : Your project
# Description : 
#   This is a template for R scripts. For the general ones.
# System/s    : macOS 10.14.6
# R version   : 3.6.1 (2019-07-05) -- "Action of the Toes"
# License     : General Public License 3 (GPL-3.0)

# Packages & Sources ####
# Ex: library(XXXX) # why? version? source? 

# Loading all functions in R/
sapply(list.files(pattern="[.]R$", path="R", full.names=TRUE), source)   

# Script's Body ####
```

## Short one

```r
#!/usr/bin/env Rscript 
# Header ####
# Title       : Template for R Scripts
# Author/s    : Name Surname (luispuerto)
# Email       : your.email@email.com
# Date        : Fri, 02 Aug 2019  
# Version     : 0.1 <- This field only appears if there isn't git repo in WD.
# Description : 
#   This is a template for R scripts. For the general ones.
# License     : General Public License 3 (GPL-3.0)

# Packages & Sources ####
# Ex: library(XXXX) # why? version? source?

# Loading all functions in R/
sapply(list.files(pattern="[.]R$", path="R", full.names=TRUE), source)

# Script's Body ####
```

## Snippets for RStudio

Bellow you can find all the snippets I've created for RStudio. You can c&p them on the snippet section in RStudio. You can check how to access and create RStudio snippets [here][snippets]. From RStudio documentation: 

>Snippets show up alongside other code completion results and can be inserted by picking them from the completion list. By default the completion list will show up automatically when you pause typing for 250 milliseconds and can also be manually activated via the `Tab` key. In addition, if you have typed the character sequence for a snippet and want to insert it immediately (without going through the completion list) you can press `Shift+Tab`.

>Note, that for markdown snippets within R Markdown documents —or inside code comments— you always need to use the `Shift+Tab` sequence as there is no standard tab completion available within the markdown editing mode.

Since the snippets file is read from top to bottom, snippets are added from top to bottom to the _stack_. In other words, the last snippets are the first one to show up in the list when their names are similar. For that reason the one I use the most, is the last one. 

### Updating fields

I've created a couple of snippets to update existing fields in the heathers. As mentioned above you need to write the full _snippets code_ and press `Shift+Tab`. 

#### Date & Update

`date` will insert just the date in the short format `%a, %d %b %Y` in other words: Day of the week, day of the month, month, year. For instance, "Fri, 02 Aug 2019". 

#### System

`os.version` will insert the name of the operative system, version code name and version. For instance, "macOS Mojave 10.14.6". It produces the same output as the `osVersion` object on the R console. 

#### RVersion

`r.version` will produce the current version of R, the release date and the code name. For instance, '3.6.1 (2019-07-05) -- "Action of the Toes"'. 

```r
# Snippets for the header

snippet r.version
    `r paste0(
          version[["major"]],
          ".",
          version[["minor"]],
          " (",
          version[["year"]],
          "-",
          version[["month"]],
          "-",
          version[["day"]],
          ") -- \"",
          version[["nickname"]],
          "\""
        )`

snippet os.version
    `r paste0(osVersion)`

snippet date
    `r paste(format(Sys.time(),"%a, %b %d %Y"))`

snippet header.short
    #!/usr/bin/env Rscript
    # Header ####
    # Title       : ${1:Script Title}
    # Author/s    : ${2:Name Surname} (${3:@username})
    # Email/s     : ${4:your.email@email.com}
    `r paste0("# Date        : ", format(Sys.time(),"%a, %b %d %Y"),
                ifelse(git2r::in_repository(),"","\n# Version     : 0.1"))`
    # Description : 
    #   ${6:Short description of this script}
    # License     : General Public License 3 (GPL-3.0)
    
    # Packages & Sources ####
    # Ex: library("XXXX") # why? version? source?
    
    # Loading all functions in R/
    sapply(list.files(pattern="[.]R$", path="R", full.names=TRUE), source)
    
    # Script's Body ####
    ${0}

snippet header.long
    #!/usr/bin/env Rscript
    # Header ####
    # Title       : ${1:Script Title}
    # Author/s    : ${2:Name Surname}
    # Username/s  : ${3:@username}
    # Email/s     : ${4:your.email@email.com}
    `r paste0("# Date        : ", format(Sys.time(),"%a, %b %d %Y"))`
    # Updated     : Not yet`r ifelse(git2r::in_repository(),"" ,"\n# Version     : 0.1")`
    # Project     : ${6:`r basename(getwd())`}
    # Description : 
    #   ${7:Short description of this script}
    `r paste0("# System/s    : ", osVersion)`
    `r paste0(
          "# R version   : ",
          version[["major"]],
          ".",
          version[["minor"]],
          " (",
          version[["year"]],
          "-",
          version[["month"]],
          "-",
          version[["day"]],
          ") -- \"",
          version[["nickname"]],
          "\""
        )`
    # License     : General Public License 3 (GPL-3.0)
    
    # Packages & Sources ####
    # Ex: library("XXXX") # why? version? source?
    
    # Loading all functions in R/
    sapply(list.files(pattern="[.]R$", path="R", full.names=TRUE), source)
    
    # Script's Body ####
    ${0}
```

[snippets]: https://support.rstudio.com/hc/en-us/articles/204463668-Code-Snippets
[git2r]: https://github.com/ropensci/git2r
[RStudio]: https://www.rstudio.com
