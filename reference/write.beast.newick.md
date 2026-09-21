# write.beast.newick

Export `treedata` object to BEAST Newick file. This is useful for making
BEAST starting trees with metadata

## Usage

``` r
write.beast.newick(
  treedata,
  file = "",
  append = FALSE,
  digits = 10,
  tree.prefix = ""
)
```

## Arguments

- treedata:

  `treedata` object

- file:

  output file. If file = "", print the output content on screen

- append:

  logical. Only used if the argument 'file' is the name of file (and not
  a connection or "\|cmd"). If 'TRUE' output will be appended to 'file';
  otherwise, it will overwrite the contents of file.

- digits:

  integer, the indicating the number of decimal places, default is 10.

- tree.prefix, :

  character the tree prefix, default is "".

## Value

output file or file content on screen

## Author

Guangchuang Yu

## Examples

``` r
nhxfile <- system.file("extdata/NHX", "phyldog.nhx", package="treeio")
nhx <- read.nhx(nhxfile)
write.beast.newick(nhx)
#> [1] "(((Prayidae_D27SS7@2825365[&Ev=S,ND=0,S=58]:0.0682841,(Kephyes_ovata@2606431[&Ev=S,ND=1,S=69]:0.0193941,Chuniphyes_multidentata@1277217[&Ev=S,ND=2,S=70]:0.0121378)[&Ev=S,ND=3,S=60]:0.0217782)[&Ev=S,ND=4,S=36]:0.0607598,((Apolemia_sp_@1353964[&Ev=S,ND=9,S=31]:0.11832,(((Bargmannia_amoena@263997[&Ev=S,ND=10,S=37]:0.0144549,Bargmannia_elongata@946788[&Ev=S,ND=11,S=38]:0.0149723)[&Ev=S,ND=12,S=33]:0.0925388,Physonect_sp_@2066767[&Ev=S,ND=13,S=61]:0.077429)[&Ev=S,ND=14,S=24]:0.0274637,(Stephalia_dilata@2960089[&Ev=S,ND=15,S=52]:0.0761163,((Frillagalma_vityazi@1155031[&Ev=S,ND=16,S=53]:0.0906068,Resomia_ornicephala@3111757[&Ev=S,ND=17,S=54]:1e-06)[&Ev=S,ND=18,S=45]:1e-06,((Lychnagalma_utricularia@2253871[&Ev=S,ND=19,S=65]:0.120851,Nanomia_bijuga@717864[&Ev=S,ND=20,S=71]:0.133939)[&Ev=S,ND=21,S=56]:1e-06,Cordagalma_sp_@1525873[&Ev=S,ND=22,S=64]:0.0693814)[&Ev=S,ND=23,S=46]:1e-06)[&Ev=S,ND=24,S=40]:0.0333823)[&Ev=S,ND=25,S=35]:1e-06)[&Ev=D,ND=26,S=24]:0.0431861)[&Ev=S,ND=27,S=19]:1e-06,Rhizophysa_filiformis@3073669[&Ev=S,ND=28,S=26]:0.22283)[&Ev=S,ND=29,S=17]:0.0292362)[&Ev=D,ND=8,S=17]:0.185603,(Hydra_magnipapillata@52244[&Ev=S,ND=5,S=16]:0.0621782,Ectopleura_larynx@3556167[&Ev=S,ND=6,S=15]:0.332505)[&Ev=S,ND=7,S=12]:0.185603)[&Ev=S,ND=30,S=9];"
```
