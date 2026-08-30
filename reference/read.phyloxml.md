# read.phyloxml

read.phyloxml

## Usage

``` r
read.phyloxml(file)
```

## Arguments

- file:

  phyloxml file

## Value

treedata class or treedataList class

## Examples

``` r
xmlfile1 <- system.file("extdata/phyloxml", "test_x2.xml", package="treeio")
px1 <- read.phyloxml(xmlfile1)
px1
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/phyloxml/test_x2.xml'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 10 tips and 9 internal nodes.
#> 
#> Tip labels:
#>   t7, t2, t3, t8, t1, t5, ...
#> 
#> Rooted; no branch length.
#> 
#> with the following features available:
#>   ''.
#> 
#> # The associated data tibble abstraction: 19 × 3
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip
#>    <dbl> <chr> <lgl>
#>  1     1 t7    TRUE 
#>  2     2 t2    TRUE 
#>  3     3 t3    TRUE 
#>  4     4 t8    TRUE 
#>  5     5 t1    TRUE 
#>  6     6 t5    TRUE 
#>  7     7 t6    TRUE 
#>  8     8 t9    TRUE 
#>  9     9 t10   TRUE 
#> 10    10 t4    TRUE 
#> # ℹ 9 more rows
xmlfile2 <- system.file("extdata/phyloxml", "phyloxml_examples.xml", package="treeio")
px2 <- read.phyloxml(xmlfile2)
px2
#> 13 phylogenetic trees 
```
