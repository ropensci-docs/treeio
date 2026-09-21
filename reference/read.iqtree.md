# read.iqtree

parse IQ-TREE output

## Usage

``` r
read.iqtree(file)
```

## Arguments

- file:

  IQ-TREE Newick text

## Value

treedata object

## Details

`read.iqtree()` parses the tree file of an IQ-TREE run (e.g.
`*.treefile`, the report file `*.iqtree` is not a tree file) and splits
the node labels into the SH-aLRT and the UFBoot support values. The two
values are expected to be separated by a `/`, which is what IQ-TREE
writes when both were requested. If the branch support was assessed with
a single method (e.g. the standard non-parametric bootstrap or SH-aLRT
alone), the node label holds one value only and there is no way to tell
which method produced it; the value is then stored in both columns and a
message is emitted. Use
[`read.newick()`](https://docs.ropensci.org/treeio/reference/read.newick.md)
to import such a tree without guessing.

## Author

Guangchuang Yu
