
D-Lab class 
2020.10.22
Notes in inet-dev-class/notes/

some jupyter notebook file i played with saved in tin/ 
	tmp container bind mount /home/tin/tin-gh/DIOS_demonstration:/mnt  so 
	cp -pi  /home/tin/tin-gh/DIOS_demonstration/code/RadvDataM* ~tin/tin-gh/advanced-data-wrangling-in-R/tin

~~~~~

 
around
## line 136 of  https://github.com/dlab-berkeley/advanced-data-wrangling-in-R/blob/master/code/03_summarizing.Rmd


lm_model( nested$data[[1]]  )
nested$data[[1]]  %>% lm_model  # same as above, just diff syntax

map(nested$data, lm_model) %>% head(2)

lapply(nested$data, lm_model) %>% head(2)
## map and lapply are very similar, map has better syntax for some common use cases.
## see https://stackoverflow.com/questions/45101045/why-use-purrrmap-instead-of-lapply
## ++ add to R.html


We tasted a little bit about how `map()` function works. Let's dig into it deeper as this family of functions is really useful. For more information, see Rebecca Barter's wonderful tutorial on the `purrr` package. In her words, this is "the tidyverse's answer to apply functions for iteration". `map()` function can take a vector (of any type), a list, and a dataframe for input. 

purrr is for functional programming in R


