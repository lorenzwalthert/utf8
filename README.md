
utf8 [![Travis-CI Build Status](https://travis-ci.org/krlmlr/utf8.svg?branch=master)](https://travis-ci.org/krlmlr/utf8) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/krlmlr/utf8?branch=master&svg=true)](https://ci.appveyor.com/project/krlmlr/utf8) [![Coverage Status](https://img.shields.io/codecov/c/github/krlmlr/utf8/master.svg)](https://codecov.io/github/krlmlr/utf8?branch=master) [![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/utf8)](https://cran.r-project.org/package=utf8)
=============================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

A simple class for storing UTF-8 strings

The values are stored as a character vector. Special care is taken that updates maintain the UTF-8 encoding.

``` r
library(utf8)
utf8(c("a", "ä"))
#> [1] "a" "ä"
as.utf8(1)
#> [1] "1"

a <- utf8("ä")
a[2] <- "ö"
class(a)
#> [1] "utf8"

data.frame(abc = letters[1:3], utf8 = utf8(letters[1:3]))
#>   abc utf8
#> 1   a    a
#> 2   b    b
#> 3   c    c
```

Install the package from GitHub:

``` r
# install.packages("devtools")
devtools::install_github("krlmlr/utf8")
```
