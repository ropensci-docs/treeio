# write.jplace

Export `jplace` object to jplace file.

## Usage

``` r
write.jplace(x, outfile)
```

## Arguments

- x:

  a jplace object.

- outfile:

  the output file name

## Examples

``` r
jp <- system.file("extdata", "sample.jplace", package="treeio")
tr1 <- read.jplace(jp)
outfile <- tempfile()
write.jplace(tr1, outfile)
tr2 <- read.jplace(outfile)
tr2
#> 'treedata' S4 object that stored information
#> of
#>  '/tmp/RtmpI7tZPw/file80d4ae1431f'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 13 tips and 12 internal nodes.
#> 
#> Tip labels:
#>   A, B, C, D, E, F, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'nplace'.
#> 
#> # The associated data tibble abstraction: 25 × 4
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip nplace
#>    <int> <chr> <lgl>  <dbl>
#>  1     1 A     TRUE       0
#>  2     2 B     TRUE       0
#>  3     3 C     TRUE       0
#>  4     4 D     TRUE       0
#>  5     5 E     TRUE       0
#>  6     6 F     TRUE       1
#>  7     7 G     TRUE       0
#>  8     8 H     TRUE       0
#>  9     9 I     TRUE       0
#> 10    10 J     TRUE       0
#> # ℹ 15 more rows
```
