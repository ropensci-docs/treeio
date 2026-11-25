# edgeNum2nodeNum

convert edge number to node number for EPA/pplacer output

## Usage

``` r
edgeNum2nodeNum(jp, edgeNum)
```

## Arguments

- jp:

  a `jplace` object

- edgeNum:

  the edge number of a placement, the `edge_num` column of a jplace
  file. EPA and pplacer number the edges by a post-order traversal, they
  are not the row numbers of `jp@phylo$edge`

## Value

the node number of the reference tree, `NA` for an edge number that is
not in the tree

## Author

Guangchuang Yu

## Examples

``` r
jpfile <- system.file("extdata", "sample.jplace", package="treeio")
jp <- read.jplace(jpfile)
edgeNum2nodeNum(jp, c(0, 1, 2))
#> [1] NA  1  2
```
