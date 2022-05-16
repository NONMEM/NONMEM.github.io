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

# Documentation (RTM)
Read the manual
```R
# find instructions for function
?package::function_name
?function name
```

# Loading libraries
Only load tidyverse, and possibly xpose4. For the rest, use `::` to use functions from other libraries.
```R
# Good
library(tidyverse)
betareg::betareg(Formula, data = df)

# Bad
library(tidyverse)
library(betareg)
betareg(Formula, data = df)
```

# Using arguments
```R
# function documentation
rename(.data, ...)
rename_with(.data, .fn, .cols = everything(), ...)

# Named arguments always after unnamed arguments
rename(a1 = b1, a2 = b2, .data = df)

# Writing too much
df %>% dplyr::rename(a1 = b1, .data = .)
# Shorter syntax:
df %>% rename(a1 = b1)
```
