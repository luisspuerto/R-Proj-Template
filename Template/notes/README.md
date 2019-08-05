# `notes` folder

Here is where you store your research notes, AKA RMarkdown notebooks. As you probably may know, the idea of RMarkdown is to mix R code —and other languages— and markdown in the same file to create richer content in form of documents or webs. On RMarkdown you can run the codeblocks and use the produced content —figures, tables, results or just data— directly in your documents. You can know more about the RMarkdown notebooks [here][rmarkdown].

The idea is you can store here your research notes about whatever you want or you are working on, or even you can produce a research diary where each file could be a journal entry about your research or your analysis. Which is a good practice of reproducible research or just to remember down the road what you've done and how you've done it. 

The suggested filename for your journal entries could be `YYYY-MM-DD-Entry-Title.Rmd` taking inspiration of the [Jelkyll posts][JelkyllPosts] file naming, but, of course, you can use whatever works for you best. If you are working in the project with more people, perhaps it has sense to create a folder for each person you are working with, or just create a join entry with different sections where coworkers explain what they been working in different sections. 

As a header of the journal —or yaml from matter— you can use this as a template: 

```yaml 
---
title: "Research Diary"
subtitle: "Subtitle" 
date: Sun, 04 Aug 2019
author: Name Surname, Name Surname... 
output: html_notebook
---
```

I've also created a snippet that you have to put in the markdown section of the snippets: 

```
snippet header.diary
  ---
  title: "${1:Research Diary}"
  subtitle: "${2:Subtitle}" 
  date: `r paste(format(Sys.time(),"%a, %d %b %Y"))`
  author: ${3:Name Surname, Name Surname...}
  output: html_notebook
  ---
  
  ${0}
```

Remember that for insert snippets on markdown, you have to write the full name of the snippet and then push `Shift + Tab`. 

On this readme you can also explain a little bit about the purpose of the different research notes fields and create a small description. 

---

_These are my research notes on the project this and that, they are mainly about this and that. There is also a couple of reports I've done for this and that._

## Notes / folder 1 

- They are about this. 
- Using this data
- I have this ideas 

## Notes / folder 2  

- ... 


[rmarkdown]: https://rmarkdown.rstudio.com
[JelkyllPosts]: https://jekyllrb.com/docs/posts/
