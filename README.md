# gini

`gini` is an R function that calculates the Gini index of inequality.


### Inputs

* `pay` = a vector of raw income values
* `corr` =  an optional Boolean value. If `corr = T`, the small-sample correction is applied. (see Deltas, George. "The small-sample bias of the Gini coefficient: results and implications for empirical research." Review of economics and statistics 85.1 (2003): 226-234.)

### Output
Returns a decimal value for the Gini index.


### Example:

```R
library(RcppArmadillo)
library(Rcpp)

sourceCpp("gini.cpp")

# create lognormal distribution of income
pay = rlnorm(10^6, 1, 1)

# get gini index
gini(pay)

[1] 0.5206577

```


### Installation
To use `gini`, install the following R packages:
 * [Rcpp](https://cran.r-project.org/web/packages/Rcpp/index.html) 
 * [RcppArmadillo](https://cran.r-project.org/web/packages/RcppArmadillo/index.html) 

Put the source code (`gini.cpp`) in the directory of your R script. Then source it with the command `sourceCpp('gini.cpp')`.




