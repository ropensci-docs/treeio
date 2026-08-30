# read.beast

read beast/mrbayes/mega Nexus output

read beast/mrbayes/mega newick file format

## Usage

``` r
read.beast(file, threads = 1, verbose = FALSE)

read.mrbayes(file, threads = 1, verbose = FALSE)

read.beast.newick(file, threads = 1, verbose = FALSE)

read.mega(file, threads = 1, verbose = FALSE)
```

## Arguments

- file:

  newick file

- threads:

  number of threads for multithreading (default: 1)

- verbose:

  set TRUE to log progress (default: FALSE)

## Value

treedata object

treedata object

## Author

Guangchuang Yu <https://guangchuangyu.github.io>

Bradley R Jones

## Examples

``` r
file <- system.file("extdata/BEAST", "beast_mcc.tree", package="treeio")
read.beast(file)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/BEAST/beast_mcc.tree'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 15 tips and 14 internal nodes.
#> 
#> Tip labels:
#>   A_1995, B_1996, C_1995, D_1987, E_1996, F_1997, ...
#> 
#> Rooted; includes branch length(s).
#> 
#> with the following features available:
#>   'height', 'height_0.95_HPD', 'height_median', 'height_range', 'length',
#> 'length_0.95_HPD', 'length_median', 'length_range', 'posterior', 'rate',
#> 'rate_0.95_HPD', 'rate_median', 'rate_range'.
#> 
#> # The associated data tibble abstraction: 29 × 16
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label  isTip height height_0.95_HPD height_median height_range length
#>    <int> <chr>  <lgl>  <dbl> <list>                  <dbl> <list>        <dbl>
#>  1     1 A_1995 TRUE      18 <dbl [2]>                  18 <dbl [2]>     1.34 
#>  2     2 B_1996 TRUE      17 <dbl [2]>                  17 <dbl [2]>     3.30 
#>  3     3 C_1995 TRUE      18 <dbl [2]>                  18 <dbl [2]>     3.33 
#>  4     4 D_1987 TRUE      26 <dbl [2]>                  26 <dbl [2]>     9.14 
#>  5     5 E_1996 TRUE      17 <dbl [2]>                  17 <dbl [2]>     3.29 
#>  6     6 F_1997 TRUE      16 <dbl [2]>                  16 <dbl [2]>     0.849
#>  7     7 G_1992 TRUE      21 <dbl [2]>                  21 <dbl [2]>     5.21 
#>  8     8 H_1992 TRUE      21 <dbl [2]>                  21 <dbl [2]>     2.19 
#>  9     9 I_1994 TRUE      19 <dbl [2]>                  19 <dbl [2]>     1.76 
#> 10    10 J_1983 TRUE      30 <dbl [2]>                  30 <dbl [2]>     1.60 
#> # ℹ 19 more rows
#> # ℹ 8 more variables: length_0.95_HPD <list>, length_median <dbl>,
#> #   length_range <list>, posterior <dbl>, rate <dbl>, rate_0.95_HPD <list>,
#> #   rate_median <dbl>, rate_range <list>
file <- system.file("extdata/MrBayes", "Gq_nxs.tre", package="treeio")
read.mrbayes(file)
#> 'treedata' S4 object that stored information
#> of
#>  '/github/home/R/x86_64-pc-linux-gnu-library/4.6/treeio/extdata/MrBayes/Gq_nxs.tre'.
#> 
#> ...@ phylo:
#> 
#> Phylogenetic tree with 12 tips and 10 internal nodes.
#> 
#> Tip labels:
#>   B_h, B_s, G_d, G_k, G_q, G_s, ...
#> 
#> Unrooted; includes branch length(s).
#> 
#> with the following features available:
#>   'length_0.95HPD', 'length_mean', 'length_median', 'prob', 'prob_percent',
#> 'prob+-sd', 'prob_range', 'prob_stddev'.
#> 
#> # The associated data tibble abstraction: 22 × 11
#> # The 'node', 'label' and 'isTip' are from the phylo tree.
#>     node label isTip length_0.95HPD length_mean length_median prob  prob_percent
#>    <int> <chr> <lgl> <list>         <chr>       <chr>         <chr> <chr>       
#>  1     1 B_h   TRUE  <dbl [2]>      0.14346674… 0.1431799378… 1     100         
#>  2     2 B_s   TRUE  <dbl [2]>      0.19250543… 0.1922242167… 1     100         
#>  3     3 G_d   TRUE  <dbl [2]>      0.05472613… 0.0546279278… 1     100         
#>  4     4 G_k   TRUE  <dbl [2]>      0.06285712… 0.0627032472… 1     100         
#>  5     5 G_q   TRUE  <dbl [2]>      0.06322611… 0.0631496765… 1     100         
#>  6     6 G_s   TRUE  <dbl [2]>      0.01057880… 0.0103911008… 1     100         
#>  7     7 G_t   TRUE  <dbl [2]>      0.00726860… 0.0071387519… 1     100         
#>  8     8 M_s   TRUE  <dbl [2]>      0.29502722… 0.2943109745… 1     100         
#>  9     9 N_m   TRUE  <dbl [2]>      0.22779248… 0.2275137837… 1     100         
#> 10    10 P_h   TRUE  <dbl [2]>      0.22505344… 0.2250620826… 1     100         
#> # ℹ 12 more rows
#> # ℹ 3 more variables: `prob+-sd` <chr>, prob_range <list>, prob_stddev <chr>
tr <- read.beast.newick(
        textConnection(
          '(a[&rate=1]:2,(b[&rate=1.1]:1,c[&rate=0.9]:1)[&rate=1]:1);'
        )
)
```
