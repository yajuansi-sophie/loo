[![Travis-CI Build Status](https://travis-ci.org/stan-dev/loo.svg?branch=master)](https://travis-ci.org/stan-dev/loo)
[![codecov](https://codecov.io/gh/stan-dev/loo/branch/master/graph/badge.svg)](https://codecov.io/github/stan-dev/loo?branch=master)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/loo?color=blue)](http://cran.r-project.org/web/packages/loo)
[![RStudio_CRAN_mirror_downloads_badge](http://cranlogs.r-pkg.org/badges/grand-total/loo?color=blue)](http://cran.r-project.org/web/packages/loo)

### **loo** R package

Efficient leave-one-out cross-validation and WAIC for fitted Bayesian models

### Resources

* [mc-stan.org/loo](http://mc-stan.org/loo) (online documentation, vignettes)
* [Ask a question](http://discourse.mc-stan.org) (Stan Forums on Discourse)
* [Open an issue](https://github.com/stan-dev/loo/issues) (GitHub issues for bug reports, feature requests)


### Installation

* Install from CRAN:

```r
install.packages("loo")
```

* Install from GitHub (requires [devtools](https://github.com/hadley/devtools) package):

```r
if (!require(devtools)) install.packages("devtools")
devtools::install_github("stan-dev/loo", build_vignettes = TRUE)
```

### About

Leave-one-out cross-validation (LOO) and the widely applicable information
criterion (WAIC) are methods for estimating pointwise out-of-sample
prediction accuracy from a fitted Bayesian model using the log-likelihood
evaluated at the posterior simulations of the parameter values. LOO and WAIC
have various advantages over simpler estimates of predictive error such as
AIC and DIC but are less used in practice because they involve additional
computational steps.

This package implements the fast and stable computations for LOO and WAIC from
*Practical Bayesian model evaluation using leave-one-out cross-validation and WAIC* 
([preprint](http://arxiv.org/abs/1507.04544), 
[published](http://link.springer.com/article/10.1007%2Fs11222-016-9696-4)).
From existing posterior simulation draws, we compute LOO using Pareto smoothed
importance sampling (PSIS), a new procedure for regularizing importance weights.
As a byproduct of our calculations, we also obtain approximate standard errors
for estimated predictive errors and for comparing predictive errors between two
models.


### Python and Matlab/Octave Code
Corresponding Python and Matlab/Octave code can be found at the
[avehtari/PSIS](https://github.com/avehtari/PSIS) repository.

