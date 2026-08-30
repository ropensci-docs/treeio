# read.hyphy

read HYPHY output

## Usage

``` r
read.hyphy(nwk, ancseq, tip.fasfile = NULL)
```

## Arguments

- nwk:

  tree file in nwk format, one of hyphy output

- ancseq:

  ancestral sequence file in nexus format, one of hyphy output

- tip.fasfile:

  tip sequence file

## Value

A hyphy object

## Author

Guangchuang Yu <https://guangchuangyu.github.io>

## Examples

``` r
nwk <- system.file("extdata/HYPHY", "labelledtree.tree", package="treeio")
ancseq <- system.file("extdata/HYPHY", "ancseq.nex", package="treeio")
read.hyphy(nwk, ancseq)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/HYPHY/labelledtree.tree'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 15 tips and 13 internal nodes.
#> 
#> Tip labels:
#>   K, N, D, L, J, G, ...
#> Node labels:
#>   Node1, Node2, Node3, Node4, Node5, Node12, ...
#> 
#> Unrooted; includes branch length(s).
```
