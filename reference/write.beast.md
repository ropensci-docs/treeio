# write.beast

Export `treedata` object to BEAST NEXUS file. This function was adopted
and modified from ape::write.nexus

## Usage

``` r
write.beast(treedata, file = "", translate = TRUE, tree.name = NULL)
```

## Arguments

- treedata:

  `treedata` object, list of `treedata`, `phylo`, or list of `phylo`

- file:

  output file. If file = "", print the output content on screen

- translate:

  whether to translate taxa labels

- tree.name:

  names of the trees, NULL to use existing tree names

## Value

output file or file content on screen

## Author

Guangchuang Yu

## Examples

``` r
nhxfile <- system.file("extdata/NHX", "phyldog.nhx", package="treeio")
nhx <- read.nhx(nhxfile)
write.beast(nhx)
#> #NEXUS
#> [R-package treeio, Sun Aug 30 07:22:30 2026]
#> 
#> BEGIN TAXA;
#>  DIMENSIONS NTAX = 16;
#>  TAXLABELS
#>      Prayidae_D27SS7@2825365
#>      Kephyes_ovata@2606431
#>      Chuniphyes_multidentata@1277217
#>      Apolemia_sp_@1353964
#>      Bargmannia_amoena@263997
#>      Bargmannia_elongata@946788
#>      Physonect_sp_@2066767
#>      Stephalia_dilata@2960089
#>      Frillagalma_vityazi@1155031
#>      Resomia_ornicephala@3111757
#>      Lychnagalma_utricularia@2253871
#>      Nanomia_bijuga@717864
#>      Cordagalma_sp_@1525873
#>      Rhizophysa_filiformis@3073669
#>      Hydra_magnipapillata@52244
#>      Ectopleura_larynx@3556167
#>  ;
#> END;
#> BEGIN TREES;
#>  TRANSLATE
#>      1   Prayidae_D27SS7@2825365,
#>      2   Kephyes_ovata@2606431,
#>      3   Chuniphyes_multidentata@1277217,
#>      4   Apolemia_sp_@1353964,
#>      5   Bargmannia_amoena@263997,
#>      6   Bargmannia_elongata@946788,
#>      7   Physonect_sp_@2066767,
#>      8   Stephalia_dilata@2960089,
#>      9   Frillagalma_vityazi@1155031,
#>      10  Resomia_ornicephala@3111757,
#>      11  Lychnagalma_utricularia@2253871,
#>      12  Nanomia_bijuga@717864,
#>      13  Cordagalma_sp_@1525873,
#>      14  Rhizophysa_filiformis@3073669,
#>      15  Hydra_magnipapillata@52244,
#>      16  Ectopleura_larynx@3556167
#>  ;
#>  TREE * UNTITLED = [&R] (((1[&Ev=S,ND=0,S=58]:0.0682841,(2[&Ev=S,ND=1,S=69]:0.0193941,3[&Ev=S,ND=2,S=70]:0.0121378)[&Ev=S,ND=3,S=60]:0.0217782)[&Ev=S,ND=4,S=36]:0.0607598,((4[&Ev=S,ND=9,S=31]:0.11832,(((5[&Ev=S,ND=10,S=37]:0.0144549,6[&Ev=S,ND=11,S=38]:0.0149723)[&Ev=S,ND=12,S=33]:0.0925388,7[&Ev=S,ND=13,S=61]:0.077429)[&Ev=S,ND=14,S=24]:0.0274637,(8[&Ev=S,ND=15,S=52]:0.0761163,((9[&Ev=S,ND=16,S=53]:0.0906068,10[&Ev=S,ND=17,S=54]:1e-06)[&Ev=S,ND=18,S=45]:1e-06,((11[&Ev=S,ND=19,S=65]:0.120851,12[&Ev=S,ND=20,S=71]:0.133939)[&Ev=S,ND=21,S=56]:1e-06,13[&Ev=S,ND=22,S=64]:0.0693814)[&Ev=S,ND=23,S=46]:1e-06)[&Ev=S,ND=24,S=40]:0.0333823)[&Ev=S,ND=25,S=35]:1e-06)[&Ev=D,ND=26,S=24]:0.0431861)[&Ev=S,ND=27,S=19]:1e-06,14[&Ev=S,ND=28,S=26]:0.22283)[&Ev=S,ND=29,S=17]:0.0292362)[&Ev=D,ND=8,S=17]:0.185603,(15[&Ev=S,ND=5,S=16]:0.0621782,16[&Ev=S,ND=6,S=15]:0.332505)[&Ev=S,ND=7,S=12]:0.185603)[&Ev=S,ND=30,S=9];
#> END;
```
