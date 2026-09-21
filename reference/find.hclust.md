# find the hierarchical cluster analysis among the nodes of graph based on the length of all the shortest paths in the graph.

find the hierarchical cluster analysis among the nodes of graph based on
the length of all the shortest paths in the graph.

## Usage

``` r
find.hclust(
  x,
  graph.mst = FALSE,
  weights = NULL,
  hclust.method = "average",
  ...
)
```

## Arguments

- x:

  a igraph object

- graph.mst:

  logical whether obtain the minimum spanning tree first then
  find.hclust, default is FALSE.

- weights:

  a numeric vector giving edge weights or a character. If this is `NULL`
  and the graph has a `weight` edge attribute, then the attribute is
  used. If this is `NA` then no weights are used even if the graph has a
  `weight` attribute. If this is a character, the graph has the edge
  attribute which is numeric, then it will be used, default is `NULL`.

- hclust.method:

  the agglomeration method to be used, This should be (an unambiguous
  abbreviation of) one of `"ward.D"`, `"ward.D2"`, `"single"`,
  `"complete"`, `"average"` (= UPGMA), `"mcquitty"` (= WPGMA),
  `"median"` (= WPGMC) or `"centroid"` (= UPGMC).

- ...:

  additional parameters

## Value

hclust object

## Examples

``` r
library(igraph)
#> 
#> Attaching package: ‘igraph’
#> The following object is masked from ‘package:treeio’:
#> 
#>     parent
#> The following objects are masked from ‘package:stats’:
#> 
#>     decompose, spectrum
#> The following object is masked from ‘package:base’:
#> 
#>     union
set.seed(123)
g <- igraph::sample_gnp(100, .1) %>%
     set_edge_attr(name='weight', value=abs(rnorm(E(.),3)))
tr1 <- find.hclust(g, weights = NA)
tr2 <- find.hclust(g)
tr3 <- find.hclust(g, graph.mst = TRUE)
```
