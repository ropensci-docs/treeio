# rename_taxa

rename tip label of phylogenetic tree

## Usage

``` r
rename_taxa(tree, data, key = 1, value = 2)
```

## Arguments

- tree:

  tree object, either treedata or phylo

- data:

  data frame

- key:

  column in data that match tip label (use 1st column by default)

- value:

  column in data for rename tip label (use 2nd column by default)

## Value

tree object

## Author

Guangchuang Yu

## Examples

``` r
tree <- rtree(3)
d <- data.frame(old = paste0('t', 1:3), new = LETTERS[1:3])
rename_taxa(tree, d)
#> 
#> Phylogenetic tree with 3 tips and 2 internal nodes.
#> 
#> Tip labels:
#>   A, B, C
#> 
#> Rooted; includes branch length(s).
rename_taxa(tree, d, old, new)
#> 
#> Phylogenetic tree with 3 tips and 2 internal nodes.
#> 
#> Tip labels:
#>   A, B, C
#> 
#> Rooted; includes branch length(s).
```
