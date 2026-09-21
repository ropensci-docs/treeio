# spt method

spt method

## Usage

``` r
spt(x, from, to, weights = NULL, ...)
```

## Arguments

- x:

  a igraph object

- from:

  a specific node of network.

- to:

  other nodes of the network, length of it must be larger than 2.

- weights:

  a numeric vector giving edge weights or a character. If this is `NULL`
  and the graph has a `weight` edge attribute, then the attribute is
  used. If this is `NA` then no weights are used even if the graph has a
  `weight` attribute. If this is a character, the graph has the edge
  attribute which is numeric, then it will be used, default is `NULL`.

- ...:

  additional parameters

## Value

phylo object

## Examples

``` r
library(igraph)
set.seed(123)
g <- igraph::sample_gnp(100, .1) %>% 
     set_edge_attr(name='weight', value=abs(rnorm(E(.),3)))
tr1 <- spt(g, from = 6, to=V(g), weights = 'weight')
tr1
#> 
#> Phylogenetic tree with 65 tips and 35 internal nodes.
#> 
#> Tip labels:
#>   4, 7, 8, 9, 10, 12, ...
#> Node labels:
#>   6, 1, 32, 3, 82, 2, ...
#> 
#> Rooted; includes branch length(s).
tr2 <- spt(g, from = 6, to = V(g), weights = NA)
tr2
#> 
#> Phylogenetic tree with 70 tips and 30 internal nodes.
#> 
#> Tip labels:
#>   4, 5, 7, 8, 9, 10, ...
#> Node labels:
#>   6, 1, 40, 2, 32, 3, ...
#> 
#> Unrooted; no branch length.
```
