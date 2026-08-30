# read.codeml_mlc

read mlc file of codeml output

## Usage

``` r
read.codeml_mlc(mlcfile)
```

## Arguments

- mlcfile:

  mlc file

## Value

A `codeml_mlc` object

## Author

Guangchuang Yu

## Examples

``` r
mlcfile <- system.file("extdata/PAML_Codeml", "mlc", package="treeio")
read.codeml_mlc(mlcfile)
#> 'treedata' S4 object that stored information
#> of
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
#>   't', 'N', 'S', 'dN_vs_dS', 'dN', 'dS', 'N_x_dN', 'S_x_dS'.
#> 
#> # The associated data tibble abstraction: 28 × 11
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip     t     N     S dN_vs_dS     dN     dS N_x_dN S_x_dS
#>    <dbl> <chr> <lgl> <dbl> <dbl> <dbl>    <dbl>  <dbl>  <dbl>  <dbl>  <dbl>
#>  1     1 A     TRUE  0.01  1515.  633.   0.0646 0.0007 0.0101    1      6.4
#>  2     2 B     TRUE  0.032 1515.  633.   0.0001 0      0.0358    0     22.7
#>  3     3 C     TRUE  0.028 1515.  633.   0.0461 0.0013 0.0282    2     17.9
#>  4     4 D     TRUE  0.082 1515.  633.   0.0385 0.0033 0.0849    5     53.8
#>  5     5 E     TRUE  0.031 1515.  633.   0.0641 0.002  0.0305    3     19.3
#>  6     6 F     TRUE  0.007 1515.  633.   0.298  0.0013 0.0044    2      2.8
#>  7     7 G     TRUE  0.046 1515.  633.   0.162  0.006  0.0373    9.2   23.6
#>  8     8 H     TRUE  0.021 1515.  633.   0.103  0.002  0.0191    3     12.1
#>  9     9 I     TRUE  0.015 1515.  633.   0.0001 0      0.0167    0     10.6
#> 10    10 J     TRUE  0.014 1515.  633.   0.0457 0.0007 0.0143    1      9  
#> # ℹ 18 more rows
```
