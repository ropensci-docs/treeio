# read.astral

parse ASTRAL output newick text

## Usage

``` r
read.astral(file)
```

## Arguments

- file:

  ASTRAL Newick file

## Value

treedata object

## Author

Guangchuang Yu

## Examples

``` r
tt <- paste0(
  "((species1,(species2,species3)'[pp1=0.75;pp2=0.24;pp3=0.01]':",
  "1.2003685744180805)'[pp1=0.98;pp2=0.02;pp3=0]':0.9679599282730038,",
  "((species4,species5)'[pp1=0.88;pp2=0.11;pp3=0.01]':1.2454851536484994))"
)
read.astral(textConnection(tt))
#> 'treedata' S4 object'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 5 tips and 5 internal nodes.
#> 
#> Tip labels:
#>   species1, species2, species3, species4, species5
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'pp1', 'pp2', 'pp3'.
#> 
#> # The associated data tibble abstraction: 10 × 6
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label    isTip   pp1   pp2   pp3
#>    <int> <chr>    <lgl> <dbl> <dbl> <dbl>
#>  1     1 species1 TRUE  NA    NA    NA   
#>  2     2 species2 TRUE  NA    NA    NA   
#>  3     3 species3 TRUE  NA    NA    NA   
#>  4     4 species4 TRUE  NA    NA    NA   
#>  5     5 species5 TRUE  NA    NA    NA   
#>  6     6 NA       FALSE NA    NA    NA   
#>  7     7 NA       FALSE  0.98  0.02  0   
#>  8     8 NA       FALSE  0.75  0.24  0.01
#>  9     9 NA       FALSE NA    NA    NA   
#> 10    10 NA       FALSE  0.88  0.11  0.01
```
