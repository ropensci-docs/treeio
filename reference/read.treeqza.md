# read.treeqza

read.treeqza

## Usage

``` r
read.treeqza(treeqza, node.label = "label", ...)
```

## Arguments

- treeqza:

  the qiime2 output file contained tree file.

- node.label:

  parse node label as 'label' or 'support' value.

- ...:

  additional parameter, passed to 'read.tree'.

## Value

phylo tree object or treedata object when node.label was parsed
'support'.

## Examples

``` r
qzafile1 <- system.file("extdata/qiime2treeqza", "fasttree-tree.qza", package="treeio")
qzafile2 <- system.file("extdata/qiime2treeqza", "iqt-tree.qza", package="treeio")
qzafile3 <- system.file("extdata/qiime2treeqza", "raxml-cat-tree.qza", package="treeio")
tr1 <- read.treeqza(qzafile1)
tr1
#> 
#> Phylogenetic tree with 20 tips and 18 internal nodes.
#> 
#> Tip labels:
#>   '682e91d7e510ab134d0625234ad224f647c14eb0', '206656bec2abdbc4aee37a661ef5f4a62b5dd6ae', 'b31aa3f04bc9d5e2498d45cf1983dfaf09faa258', '606c23e79bb730ad74e3c6efd72004c36674c17a', '0469f8d819bd45c7638d1c8b0895270a05f34267', '5525fb6dab7b6577960147574465990c6df070ad', ...
#> Node labels:
#>   , 0.765, 0.000, 0.554, 0.926, 0.917, ...
#> 
#> Unrooted; includes branch length(s).
tr2 <- read.treeqza(qzafile2)
tr2
#> 
#> Phylogenetic tree with 20 tips and 18 internal nodes.
#> 
#> Tip labels:
#>   e84fcf85a6a4065231dcf343bb862f1cb32abae6, 5525fb6dab7b6577960147574465990c6df070ad, d162ed685007f5adede58f14aece31dfa1b60c18, 0469f8d819bd45c7638d1c8b0895270a05f34267, 8a1c44eb462ed58b21f3fdd72dd22bb657db2980, 606c23e79bb730ad74e3c6efd72004c36674c17a, ...
#> 
#> Unrooted; includes branch length(s).
tr3 <- read.treeqza(qzafile3)
tr3
#> 
#> Phylogenetic tree with 20 tips and 18 internal nodes.
#> 
#> Tip labels:
#>   ed1acad8a98e8579a44370733533ad7d3fed8006, 9b220cae8d375ea38b8b481cb95949cda8722fcb, 5aba6bd9debc23ded7041ffdcfe5d68a427e8ce8, 2e3b2c075901640c4de739473f9246385430b1ed, 682e91d7e510ab134d0625234ad224f647c14eb0, d44b129a6181f052198bda3813f0802a91612441, ...
#> 
#> Rooted; includes branch length(s).
# parse node label as 'support' value.
qzafile4 <- system.file("extdata/qiime2treeqza", "raxml-cat-bootstrap-tree.qza", package="treeio")
tr4 <- read.treeqza(qzafile4, node.label="support")
tr4
#> 'treedata' S4 object'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 20 tips and 18 internal nodes.
#> 
#> Tip labels:
#>   d44b129a6181f052198bda3813f0802a91612441,
#> aa4698d2e2b1fa71d08e2934a923aad7374a18f6,
#> 6a36152105590b1eb095b9503e8f1f226fc73e43,
#> 418f1d469f08c99976b313028cf6d3f18f61dd55,
#> 9b220cae8d375ea38b8b481cb95949cda8722fcb,
#> 5aba6bd9debc23ded7041ffdcfe5d68a427e8ce8, ...
#> 
#> Unrooted; includes branch length(s).
#> 
#> with the following features available:
#>   'support'.
#> 
#> # The associated data tibble abstraction: 38 × 4
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label                                    isTip support
#>    <int> <chr>                                    <lgl>   <dbl>
#>  1     1 d44b129a6181f052198bda3813f0802a91612441 TRUE       NA
#>  2     2 aa4698d2e2b1fa71d08e2934a923aad7374a18f6 TRUE       NA
#>  3     3 6a36152105590b1eb095b9503e8f1f226fc73e43 TRUE       NA
#>  4     4 418f1d469f08c99976b313028cf6d3f18f61dd55 TRUE       NA
#>  5     5 9b220cae8d375ea38b8b481cb95949cda8722fcb TRUE       NA
#>  6     6 5aba6bd9debc23ded7041ffdcfe5d68a427e8ce8 TRUE       NA
#>  7     7 2e3b2c075901640c4de739473f9246385430b1ed TRUE       NA
#>  8     8 206656bec2abdbc4aee37a661ef5f4a62b5dd6ae TRUE       NA
#>  9     9 b31aa3f04bc9d5e2498d45cf1983dfaf09faa258 TRUE       NA
#> 10    10 606c23e79bb730ad74e3c6efd72004c36674c17a TRUE       NA
#> # ℹ 28 more rows
```
