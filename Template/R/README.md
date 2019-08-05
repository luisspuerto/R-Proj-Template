# `R` folder

In this folder you store your files with function definitions, but only function definitions, no code that actually runs. Code that you run is mean to be storage in [`code`](../code). You usually call this files at the beginning of your scripts and the purpose of the `sapply(list.files(pattern="[.]R$", path="R", full.names=TRUE), source)` line in the header templates if to load this files all at once. Whether you use that line or you load one by one using `source()` is up to you. 

As in other cases, you can create a subfolder structure if necessary, but keep it simple. It's also recommendable to create a small description and / or state the purpose of each file in this readme for future reference or sharing purposes.

---

These are my function definition files and they are mainly for function for this and that purpose. This file is specially important for this and that. 

## File / folder 1 

- This file do this. 
- This file is implemented mainly in this script. 
- It has the following dependencies. 

## File / folder 2 

- ... 

