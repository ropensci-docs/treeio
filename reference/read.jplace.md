# read.jplace

read jplace file

## Usage

``` r
read.jplace(file)
```

## Arguments

- file:

  jplace file

## Value

`jplace` instance

## Author

Guangchuang Yu

## Examples

``` r
jp <- system.file("extdata", "sample.jplace", package="treeio")
read.jplace(jp)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/sample.jplace'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 13 tips and 12 internal nodes.
#> 
#> Tip labels:
#>   A, B, C, D, E, F, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'nplace'.
#> 
#> # The associated data tibble abstraction: 25 × 4
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip nplace
#>    <int> <chr> <lgl>  <dbl>
#>  1     1 A     TRUE       0
#>  2     2 B     TRUE       0
#>  3     3 C     TRUE       0
#>  4     4 D     TRUE       0
#>  5     5 E     TRUE       0
#>  6     6 F     TRUE       1
#>  7     7 G     TRUE       0
#>  8     8 H     TRUE       0
#>  9     9 I     TRUE       0
#> 10    10 J     TRUE       0
#> # ℹ 15 more rows
```
