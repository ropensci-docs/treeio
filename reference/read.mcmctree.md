# read.mcmctree

read MCMCTree output Tree

## Usage

``` r
read.mcmctree(file, force.ultrametric = FALSE)
```

## Arguments

- file:

  the output tree file of MCMCTree

- force.ultrametric:

  logical whether convert the tree to be ultrametric, if it is not
  ultrametric, default is FALSE. When the tree is ultrametric, branch
  times will be calculated automatically.

## Value

treedata object

## Examples

``` r
file <- system.file("extdata/MCMCTree", "mcmctree_output.tree", package="treeio")
tr <- read.mcmctree(file)
tr
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/MCMCTree/mcmctree_output.tree'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 103 tips and 102 internal nodes.
#> 
#> Tip labels:
#>   Dioscorea_villosa, Colchicum_autumnale, Smilax_bona-nox, Sorghum_bicolor,
#> Zea_mays, Oryza_sativa, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   '0.95', 'reltime'.
#> 
#> # The associated data tibble abstraction: 205 × 5
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label                   isTip `0.95` reltime
#>    <int> <chr>                   <lgl> <list>   <dbl>
#>  1     1 Dioscorea_villosa       TRUE  <NULL>      NA
#>  2     2 Colchicum_autumnale     TRUE  <NULL>      NA
#>  3     3 Smilax_bona-nox         TRUE  <NULL>      NA
#>  4     4 Sorghum_bicolor         TRUE  <NULL>      NA
#>  5     5 Zea_mays                TRUE  <NULL>      NA
#>  6     6 Oryza_sativa            TRUE  <NULL>      NA
#>  7     7 Brachypodium_distachyon TRUE  <NULL>      NA
#>  8     8 Sabal_bermudana         TRUE  <NULL>      NA
#>  9     9 Yucca_filamentosa       TRUE  <NULL>      NA
#> 10    10 Acorus_americanus       TRUE  <NULL>      NA
#> # ℹ 195 more rows
```
