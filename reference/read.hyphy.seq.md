# read.hyphy.seq

parse sequences from hyphy output

## Usage

``` r
read.hyphy.seq(file)
```

## Arguments

- file:

  output of hyphy ancestral sequence inference; nexus format

## Value

DNAbin object

## Author

Guangchuang Yu

## Examples

``` r
ancseq <- system.file("extdata/HYPHY", "ancseq.nex", package="treeio")
read.hyphy.seq(ancseq)
#> 13 DNA sequences in binary format stored in a list.
#> 
#> All sequences of same length: 2148 
#> 
#> Labels:
#> Node1
#> Node2
#> Node3
#> Node4
#> Node5
#> Node12
#> ...
#> 
#> Base composition:
#>     a     c     g     t 
#> 0.335 0.208 0.237 0.220 
#> (Total: 27.92 kb)
```
