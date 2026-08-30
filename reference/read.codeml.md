# read.codeml

read baseml output

## Usage

``` r
read.codeml(rstfile, mlcfile, tree = "mlc", type = "Joint")
```

## Arguments

- rstfile:

  rst file

- mlcfile:

  mlc file

- tree:

  one of 'mlc' or 'rst'

- type:

  one of 'Marginal' or 'Joint'

## Value

A `treedata` object

## Author

Guangchuang Yu

## Examples

``` r
rstfile <- system.file("extdata/PAML_Codeml", "rst", package="treeio")
mlcfile <- system.file("extdata/PAML_Codeml", "mlc", package="treeio")
read.codeml(rstfile, mlcfile)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/PAML_Codeml/rst',
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/PAML_Codeml/mlc'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 15 tips and 13 internal nodes.
#> 
#> Tip labels:
#>   A, B, C, D, E, F, ...
#> Node labels:
#>   16, 17, 18, 19, 20, 21, ...
#> 
#> Unrooted; includes branch length(s).
#> 
#> with the following features available:
#>   'subs', 'AA_subs', 't', 'N', 'S', 'dN_vs_dS', 'dN', 'dS', 'N_x_dN', 'S_x_dS'.
#> 
#> # The associated data tibble abstraction: 28 × 13
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip subs       AA_subs     t     N     S dN_vs_dS     dN     dS
#>    <dbl> <chr> <lgl> <chr>      <chr>   <dbl> <dbl> <dbl>    <dbl>  <dbl>  <dbl>
#>  1     1 A     TRUE  C214T / G… "K603R" 0.01  1515.  633.   0.0646 0.0007 0.0101
#>  2     2 B     TRUE  C222T / G… ""      0.032 1515.  633.   0.0001 0      0.0358
#>  3     3 C     TRUE  A204G / C… "N272S… 0.028 1515.  633.   0.0461 0.0013 0.0282
#>  4     4 D     TRUE  A111G / A… "K104R… 0.082 1515.  633.   0.0385 0.0033 0.0849
#>  5     5 E     TRUE  C174T / G… "T208S… 0.031 1515.  633.   0.0641 0.002  0.0305
#>  6     6 F     TRUE  T829C / C… "S277P… 0.007 1515.  633.   0.298  0.0013 0.0044
#>  7     7 G     TRUE  A5T / A69… "E2V /… 0.046 1515.  633.   0.162  0.006  0.0373
#>  8     8 H     TRUE  A112G / C… "I38V … 0.021 1515.  633.   0.103  0.002  0.0191
#>  9     9 I     TRUE  T211C / C… ""      0.015 1515.  633.   0.0001 0      0.0167
#> 10    10 J     TRUE  G295A / A… "G99R"  0.014 1515.  633.   0.0457 0.0007 0.0143
#> # ℹ 18 more rows
#> # ℹ 2 more variables: N_x_dN <dbl>, S_x_dS <dbl>
```
