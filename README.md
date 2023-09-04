
# darr

<!-- badges: start -->
[![check-bioc](https://github.com/baerlachlan/darr/actions/workflows/check-bioc.yml/badge.svg)](https://github.com/baerlachlan/darr/actions/workflows/check-bioc.yml)
[![Codecov test coverage](https://codecov.io/gh/baerlachlan/darr/branch/devel/graph/badge.svg)](https://app.codecov.io/gh/baerlachlan/darr?branch=devel)
[![Repo Status](https://img.shields.io/badge/repository%20status-active-brightgreen)](https://shields.io/)
<!-- badges: end -->

`darr` is a package designed to simplify Differential Allelic Representation (DAR) analysis using `R`.

DAR is parsimoniously defined as an unequal distribution of polymorphic loci between experimental groups; a situation likely to be encountered in RNA-seq experiments involving organisms that lack isogenicity. When unequally-represented polymorphic loci are also expression quantitative trait loci (eQTLs), differences in gene expression between sample groups can be incorrectly interpreted as a consequence of the experimental condition. DAR analysis is therefore recommended as a complementary technique alongside Differential Expression analysis. DAR analysis results in an easy-to-interpret value between 0 and 1 for each feature (e.g. gene) of interest, where 0 represents identical allelic representation and 1 represents complete diversity. This metric can be used to identify features prone to false-positive calls in Differential Expression analysis, and can be leveraged with statistical techniques to alleviate the impact of such artefacts on RNA-seq data.

## Installation

`BiocManager` is recommended for the installation of this package.

```r
install.packages("BiocManager")
BiocManager::install("darr")
```

The development version of this package can also be installed from GitHub.

```r
BiocManager::install("baerlachlan/darr")
```