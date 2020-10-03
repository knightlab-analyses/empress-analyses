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

[Link to QZV of EMPress plot.](https://view.qiime2.org/visualization/?type=html&src=https%3A%2F%2Fraw.githubusercontent.com%2Fknightlab-analyses%2Fempress-analyses%2Fmaster%2Fnotebooks%2Ffig2a%2Finput%2Fcovid-plot-no-emperor.qzv)

1. In the `Layout` tab
    1. Change `Layout` to `Circular`
    2. Change `Sort clades based on tip count?` to `No sorting`
2. In the `Feature Metadata Coloring` tab
    1. Select `custom_level` for `Color by...`  
    2. Set `Color Map` to `Spectral`
    3. Check `Collapse Clades`
3. In the `Barplots` tab
    1. Check `Draw barplots?`
    2. Click `Feature Metadata`
    3. Color by `covid_hc_sig`
    4. Set `Color Map` to `Spectral`
4. Double click on the `Carbon-carbon lyases` clade (the larger red clade)
5. In `Search by node name...`, search for `4.1.1.20`
 

## Figure 2B

[TBD]


## Figure 2C

[Link to QZV of the EMPress plot](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig2c/output/tree-viz.qzv).

To reproduce the figure within this QZV:

1. Change `Layout` to `Circular`
2. Color tips by their phylum-level taxonomic classifications:
    1. Use `Feature Metadata Coloring` to color by `Level 2`.
    2. Click `Update`.
3. In the `Barplots` tab, click the checkbox marked `Draw barplots?`.
4. Add a barplot for the Songbird differentials. Within the `Layer 1` section:
    1. Click on `Color by...` and select `C(brushing_event)[T.before]`.
    2. Set the `Color Map` to `Spectral`.
    3. Check the `Continuous values?` checkbox.
    4. Set `Default length` to 500.
5. Click `Update`.
6. Add a barplot for the ALDEx2 effect sizes. Click `Add another layer`. Within
   the `Layer 2` section:
    1. Click on `Color by...` and select `sfit.effect`.
    2. Set the `Color Map` to `Spectral`.
    3. Check the `Continuous values?` checkbox.
    4. Set `Default length` to 500.
7. Click `Update`.
8. Add a barplot for the ANCOM W-statistics. Click `Add another layer`. Within
   the `Layer 3` section:
    1. Click on `Color by...` and select `W_stat`.
    2. Set the `Color Map` to `Purples`.
    3. Check the `Continuous values?` checkbox.
    4. Set `Default length` to 500.
9. Click `Update`.
10. Add a border around each barplot layer:
    1. Click the `Add a border around barplot layers?` checkbox.
    2. Set `Length` to 100.
11. Click `Update`.

See the [notebook](https://nbviewer.jupyter.org/github/knightlab-analyses/empress-analyses/blob/master/notebooks/fig2c.ipynb) for details on how we merged the data, generated an EMPress visualization, and configured the visualization.
