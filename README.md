# empress-analyses

This document outlines the steps needed to recreate figure 1A, 1B and 2A-C. To
generate the artifacts in these figures, we recommend following the steps in
the Jupyter notebooks (see the `notebooks` folder).

## Figure 1A

[Link to QZV of EMPire plot.](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig1/output/EMP_empire.qzv)

1. Change `Layout` to `Circular`
2. Color tips by phylum assignment
    1. `Feature Metadata Coloring` color by `phylum_assignment`
    2. Set `Color Map` to `Dark`
    3. Click `Update`
3. EMPO 2 barplot
    1. Check `Draw barplots?`
    2. Click `Sample Metadata`
    3. Show sample info for `empo_2`
    4. Set `Color Map` to `Set1`
    5. Set `Length` to 500
    6. Click `Update`
4. Search for specific feature
    1. Copy `TACGTAGGTCCCGAGCGTTGTCCGGATTTATTGGGCGTAAAGCGAGCGCAGACGGTTACTTAAGCAGGATGTGAAATCCCCGGGCTCAAC` into search bar
    2. Click `Search`

## Figure 1B


[Link to QZV of EMPress plot.](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig1/output/ph_EMP_empress.qzv)

1. Change `Layout` to `Circular`
2. Color tips by phylum assignment
    1. `Feature Metadata Coloring` color by `phylum_assignment`
    2. Set `Color Map` to `Dark`
    3. Click `Update`
3. Mean pH barplot
    1. Check `Draw barplots?`
    2. Click `Feature Metadata`
    3. Color by `arithmetic_mean`
    4. Set `Color Map` to `Blues`
    5. Check `Continuous values?`
4. Sample presence barplot
    1. Check `Draw barplots?`
    2. Click `Feature Metadata`
    3. Color by `log10_sample_presence`
    4. Set `Color Map` to `Reds`
    5. Check `Continuous values?`
5. Add space between barplots
    1. Check `Add a border around barplot layers?`
    2. Set `Length` to 50
    3. Click `Update`

## Figure 2A

[TBD]


## Figure 2B

[TBD]


## Figure 2C

[TBD]
