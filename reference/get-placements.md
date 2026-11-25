# get.placements

access placement information

## Usage

``` r
get.placements(tree, ...)

# S3 method for class 'jplace'
get.placements(tree, by = "best", ...)
```

## Arguments

- tree:

  tree object

- ...:

  additional parameters

- by:

  one of 'best' and 'all'

## Value

placement tibble

## Details

The `node` column is the node number of the reference tree, that is the
node the branch leads to (a tip or an internal node, numbered 1:Ntip for
the tips and Ntip+1:Ntip+Nnode for the internal nodes). It is translated
from the `edge_num` of the jplace file, which EPA and pplacer number by
a post-order traversal of the tree;
[`edgeNum2nodeNum()`](https://docs.ropensci.org/treeio/reference/edgeNum2nodeNum.md)
does that translation, \#22
