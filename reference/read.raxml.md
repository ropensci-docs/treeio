# read.raxml

parse RAxML bootstrapping analysis output

## Usage

``` r
read.raxml(file)
```

## Arguments

- file:

  RAxML bootstrapping analysis output

## Value

treedata object

## Author

Guangchuang Yu

## Examples

``` r
raxml_file <- system.file("extdata/RAxML", "RAxML_bipartitionsBranchLabels.H3", package="treeio")
read.raxml(raxml_file)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/RAxML/RAxML_bipartitionsBranchLabels.H3'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 64 tips and 62 internal nodes.
#> 
#> Tip labels:
#>   A_Hokkaido_M1_2014_H3N2_2014, A_Czech_Republic_1_2014_H3N2_2014,
#> FJ532080_A_California_09_2008_H3N2_2008,
#> EU199359_A_Pennsylvania_05_2007_H3N2_2007,
#> EU857080_A_Hong_Kong_CUHK69904_2006_H3N2_2006,
#> EU857082_A_Hong_Kong_CUHK7047_2005_H3N2_2005, ...
#> 
#> Unrooted; includes branch length(s).
#> 
#> with the following features available:
#>   'bootstrap'.
#> 
#> # The associated data tibble abstraction: 126 × 4
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label                                         isTip bootstrap
#>    <int> <chr>                                         <lgl>     <dbl>
#>  1     1 A_Hokkaido_M1_2014_H3N2_2014                  TRUE         NA
#>  2     2 A_Czech_Republic_1_2014_H3N2_2014             TRUE         NA
#>  3     3 FJ532080_A_California_09_2008_H3N2_2008       TRUE         NA
#>  4     4 EU199359_A_Pennsylvania_05_2007_H3N2_2007     TRUE         NA
#>  5     5 EU857080_A_Hong_Kong_CUHK69904_2006_H3N2_2006 TRUE         NA
#>  6     6 EU857082_A_Hong_Kong_CUHK7047_2005_H3N2_2005  TRUE         NA
#>  7     7 YGSIV1046_Sw_Binh_Duong_03_10_2010            TRUE         NA
#>  8     8 YGSIV1044_Sw_Binh_Duong_03_08_2010            TRUE         NA
#>  9     9 YGSIV1522_SW_HK_1071_2012                     TRUE         NA
#> 10    10 YGSIV1534_SW_HK_2454_2012                     TRUE         NA
#> # ℹ 116 more rows
```
