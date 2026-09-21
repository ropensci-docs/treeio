# read.paml_rst

read rst file from paml (both baseml and codeml) output

## Usage

``` r
read.paml_rst(rstfile, type = "Joint")
```

## Arguments

- rstfile:

  rst file

- type:

  one of 'Marginal' or 'Joint'

## Value

A `treedata` object

## Author

Guangchuang Yu <https://guangchuangyu.github.io>

## Examples

``` r
rstfile <- system.file("extdata/PAML_Baseml", "rst", package="treeio")
read.paml_rst(rstfile)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/PAML_Baseml/rst'.
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
#>   'subs', 'AA_subs'.
#> 
#> # The associated data tibble abstraction: 28 × 5
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip subs                                                AA_subs
#>    <dbl> <chr> <lgl> <chr>                                               <chr>  
#>  1     1 A     TRUE  C214T / G294T / G785A / T966C / C1641T / A1808G / … "R262K…
#>  2     2 B     TRUE  C222T / G555A / C732A / G785A / C828T / G939T / T9… "R262K"
#>  3     3 C     TRUE  A204G / C222T / G504A / A815G / C891T / G1023T / T… "N272S…
#>  4     4 D     TRUE  A111G / A168G / T211C / A213G / T214C / G243A / A3… "K104R…
#>  5     5 E     TRUE  C174T / G243A / G321A / A622T / T831C / A894G / G9… "T208S…
#>  6     6 F     TRUE  T829C / C1353T / A1443G / T1548C / C1645A           "S277P…
#>  7     7 G     TRUE  A5T / A69G / G106T / C156T / C237T / G295A / G301C… "E2V /…
#>  8     8 H     TRUE  A112G / C132A / G774T / A792C / T1002C / G1020A / … "I38V …
#>  9     9 I     TRUE  T211C / C582T / C891T / A894G / G1083A / G1116A / … ""     
#> 10    10 J     TRUE  G295A / A618G / A783C / C996T / G1593A / A1845G / … "G99R" 
#> # ℹ 18 more rows
```
