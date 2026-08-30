# read.phylip

parsing phylip tree format

## Usage

``` r
read.phylip(file)
```

## Arguments

- file:

  phylip file

## Value

an instance of 'phylip'

## Author

Guangchuang Yu

## Examples

``` r
phyfile <- system.file("extdata", "sample.phy", package="treeio")
read.phylip(phyfile)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/sample.phy'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 15 tips and 13 internal nodes.
#> 
#> Tip labels:
#>   K, N, D, L, J, G, ...
#> 
#> Unrooted; no branch length.
```
