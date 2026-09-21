# read.r8s

parse output from r8s

## Usage

``` r
read.r8s(file)
```

## Arguments

- file:

  r8s output log file

## Value

multiPhylo object

## Author

Guangchuang Yu

## Examples

``` r
read.r8s(system.file("extdata/r8s", "H3_r8s_output.log", package="treeio"))
#> 3 phylogenetic trees
```
