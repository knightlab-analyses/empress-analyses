# empress-analyses

This document outlines the steps needed to recreate figure 1A, 1B and 2A-C. To
generate the artifacts in these figures, we recommend following the steps in
the Jupyter notebooks (see the `notebooks` folder).

## Figure 1A

[TBD]

## Figure 1B

[TBD]

## Figure 2A

[TBD]


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
