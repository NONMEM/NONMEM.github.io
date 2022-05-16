# Coding conventions in R
* [Style guide · Advanced R. (had.co.nz)](http://adv-r.had.co.nz/Style.html)
* [Tidyverse style Guide](https://style.tidyverse.org/)

# syntax
Use spaces:
* After a comma, just like writing sentences
* Around infix operators `=`, `+`, `-`, `<-`, etc...
* Not after `:`, `::`, `:::` operators
* making it more readable
```R
# Good
average <- mean(feet / 12 + inches, na.rm = TRUE)
list(
  total =  a + b + c,
  mean  = (a + b + c) / n)
)

# Bad
average<-mean(feet/12+inches,na.rm=TRUE)
```
