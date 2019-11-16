# Rmarkdown_Word
Some Word macros used to tidy the Word documents produced by Rmarkdown

All you really need is the wordmacros.txt file. You can download this by opening it in github (double click on it), then clicking the raw button once the viewer opens. That will enable you to copy the code to your own computer. However, if you want the rest you could always download a zip file or clone the repository.

I use these macros when using the captioner R package (from CRAN), written by Alathea Letaw, to number my figures, tables and equations. 

A typical arrangement put into the setup R code following the YAML hgeader might include:

library(captioner)

tab_nums <- captioner(prefix = "Table")
fig_nums <- captioner(prefix = "Figure")
equ_nums <- captioner(prefix = "Equ.")

which might be used in the body of the document like:


`r equ_nums("d1")`

$${{N}_{t+1}}={{N}_{t}}+{{r}{N}_{t}}\left( 1-{{\left( \frac{{{N}_{t}}}{K} \right)}} \right)-{{C}_{t}}$$


Notice the title of each equation, set in the setup, starts with Equ. where the "." is important. It is important because when I refer to an equation in the text I omit the fullstop. That way, when the macro lines up the number with the equation it only makes those changes for display equations and not references to equations in the text.
