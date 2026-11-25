# read.nhx

read nhx tree file

## Usage

``` r
read.nhx(file)
```

## Arguments

- file:

  nhx file

## Value

nhx object

## Author

Guangchuang Yu <https://guangchuangyu.github.io>

## Examples

``` r
nhxfile <- system.file("extdata/NHX", "ADH.nhx", package="treeio")
read.nhx(nhxfile)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/NHX/ADH.nhx'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 8 tips and 4 internal nodes.
#> 
#> Tip labels:
#>   ADH2, ADH1, ADHY, ADHX, ADH4, ADH3, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'V1', 'B', 'D', 'S'.
#> 
#> # The associated data tibble abstraction: 12 × 7
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip    V1     B D     S       
#>    <int> <chr> <lgl> <dbl> <dbl> <chr> <chr>   
#>  1     1 ADH2  TRUE     NA    NA NA    human   
#>  2     2 ADH1  TRUE     NA    NA NA    human   
#>  3     3 ADHY  TRUE     NA    NA NA    nematode
#>  4     4 ADHX  TRUE     NA    NA NA    insect  
#>  5     5 ADH4  TRUE     NA    NA NA    yeast   
#>  6     6 ADH3  TRUE     NA    NA NA    yeast   
#>  7     7 ADH2  TRUE     NA    NA NA    yeast   
#>  8     8 ADH1  TRUE     NA    NA NA    yeast   
#>  9     9 NA    FALSE    NA    NA N     NA      
#> 10    10 NA    FALSE    NA    NA N     metazoa 
#> # ℹ 2 more rows
```
