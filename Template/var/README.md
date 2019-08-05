# `var` folder

This is personal addition and the purpose of this folder is to store the temporal variables and files for analysis and it's inspired in the [UNIX-like folder structure][folderstructure] `/var` folder which is defined as:  

>Variable files—files whose content is expected to continually change during normal operation of the system—such as logs, spool files, and temporary e-mail files.

You can store here R objects, variables or data files that you are going to use in further analysis. Perhaps also half backed data and temporal files. For example, scripts where you wanted to test something. It's true that it goes against the good practices to store these objects and variables and it's much better to create environmental variables from source code when they are necessary. However, sometimes analysis can take long computing time and could be useful to store intermediate data states or steps. 

You probably are thinking that this is a kind of temp folder, and you are right. I just thought that `var` name was much more suitable since the main aim is to store temporal variables and files. If you need a specific `tmp`folder perhaps you can create one in the root of the project or under this directory. 

---

_This is where the temporal variables and files of this project are storage. This variable has been used for this analysis or this script, and this other was a temporal step for this other analysis._ 

## File / folder 1 

- This is storing this or that data. 
- It was created for this purpose. 
- It's important for this or that other reason. 

## File / folder 2 

- ... 



[folderstructure]: https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard
