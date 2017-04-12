
kdevine
=======

> Multivariate kernel density estimation with vine copulas

[![Build status Linux](https://travis-ci.org/tnagler/kdevine.svg?branch=master)](https://travis-ci.org/tnagler/kdevine) [![Build status Windows](https://ci.appveyor.com/api/projects/status/epfs987wspjqkwlk/branch/master?svg=true)](https://ci.appveyor.com/project/tnagler/kdevine) [![CRAN version](http://www.r-pkg.org/badges/version/kdevine)](https://cran.r-project.org/package=kdevine) [![CRAN downloads](http://cranlogs.r-pkg.org/badges/kdevine)](https://cran.r-project.org/package=kdevine)

This package implements a vine copula based kernel density estimator. The estimator does not suffer from the curse of dimensionality and is therefore well suited for high-dimensional applications (see, Nagler and Czado, 2016). The package is built on top of the copula density estimators in [kdecopula](https://github.com/tnagler/kdecopula) and let's you choose from all its implemented methods. The package can handle discrete and categorical data via [continuous convolution](https://github.com/tnagler/cctools).

-   [How to install](#how-to-install)
-   [Functionality](#functionality)
-   [References](#references)

------------------------------------------------------------------------

How to install
--------------

You can install:

-   the stable release on CRAN:

    ``` r
    install.packages("kdevine")
    ```

-   the latest development version:

    ``` r
    devtools::install_github("tnagler/kdevine")
    ```

Functionality
-------------

The package provides the following functionality:

-   Class `kdevine` and its methods:

    -   `kdevine`: Multivariate kernel density estimation based on vine copulas. Implements the estimator of (see, Nagler and Czado, 2016).

    -   `dkdevine`, `rkdevine`: Density and simulation functions.

-   Class `kdevinecop` and its methods:

    -   `kdevinecop`: Kernel estimator for the vine copula density (see, Nagler and Czado, 2016).

    -   `dkdevinecop`, `rkdevinecop`: Density and simulation functions.

    -   `contour`: Matrix of contour plots of all pair-copulas.

-   Class `kde1d` and its methods:

    -   `kde1d`: Univariate kernel density estimation for bounded and unbounded support.

    -   `dke1d`, `pkde1d`, `rkde1d`: Density, cdf, and simulation functions.

    -   `plot`, `lines`: Plots the estimated density.

See the [package documentation](https://cran.r-project.org/web/packages/kdevine/kdevine.pdf) for more details on arguments and options.

References
----------

Nagler, T., Czado, C. (2016)
Evading the curse of dimensionality in nonparametric density estimation with simplified vine copulas
*Journal of Multivariate Analysis 151, 69-89* ([doi:10.1016/j.jmva.2016.07.003](http://dx.doi.org/10.1016/j.jmva.2016.07.003))
[preprint](http://arxiv.org/abs/1503.03305)

Nagler, T., Schellhase, C. and Czado, C. (2017)
Nonparametric estimation of simplified vine copula models: comparison of methods
[preprint](http://arxiv.org/abs/1701.00845)
