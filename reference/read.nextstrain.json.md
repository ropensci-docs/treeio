# read.nextstrain.json

read.nextstrain.json

## Usage

``` r
read.nextstrain.json(x)
```

## Arguments

- x:

  the json tree file of auspice from nextstrain.

## Value

treedata object

## Author

Shuangbin Xu

## Examples

``` r
file1 <- system.file("extdata/nextstrain.json", "minimal_v2.json", package="treeio") 
tr <- read.nextstrain.json(file1)
tr
#> 'treedata' S4 object'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 31 tips and 25 internal nodes.
#> 
#> Tip labels:
#>   Thailand/1610acTw, SG_018, SG_056, SG_027, SG_074, ZKC2/2016, ...
#> Node labels:
#>   NODE_0000031, NODE_0000011, NODE_0000012, NODE_0000013, NODE_0000009,
#> NODE_0000010, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'num_date', 'div', 'country', 'region'.
#> 
#> # The associated data tibble abstraction: 56 × 7
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label             isTip num_date     div country          region       
#>    <dbl> <chr>             <lgl>    <dbl>   <dbl> <chr>            <chr>        
#>  1     1 Thailand/1610acTw TRUE     2017. 0.00522 Thailand         Southeast As…
#>  2     2 SG_018            TRUE     2017. 0.00401 Singapore        Southeast As…
#>  3     3 SG_056            TRUE     2017. 0.00391 Singapore        Southeast As…
#>  4     4 SG_027            TRUE     2017. 0.00391 Singapore        Southeast As…
#>  5     5 SG_074            TRUE     2017. 0.00363 Singapore        Southeast As…
#>  6     6 ZKC2/2016         TRUE     2016. 0.00447 American Samoa   Oceania      
#>  7     7 SMGC_1            TRUE     2016. 0.00447 American Samoa   Oceania      
#>  8     8 1_0087_PF         TRUE     2014. 0.00242 French Polynesia Oceania      
#>  9     9 1_0181_PF         TRUE     2014. 0.00252 French Polynesia Oceania      
#> 10    10 1_0199_PF         TRUE     2014. 0.00242 French Polynesia Oceania      
#> # ℹ 46 more rows
```
