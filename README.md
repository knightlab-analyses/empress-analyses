# empress-analyses

This document outlines the steps needed to recreate figure 1A, 1B and 2A-C. To
generate the artifacts in these figures, we recommend [installing
Empress](https://github.com/biocore/empress), cloning this repository, and
following the steps in the Jupyter notebooks (see the `notebooks` folder).

For visualizing the QZV files **we recommend using Safari or
Firefox**, since Google Chrome is known to show degraded performance when
loading large files in certain cases (for example Figure 1A-B). See
[here](https://stackoverflow.com/a/59438847/10730311) for details on this.

## Figure 1A

[Link to QZV of EMPire plot.](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig1/output/EMP_empire.qzv)

1. Change `Layout` to `Circular`
2. Color tips by phylum assignment
    1. `Feature Metadata Coloring` color by `phylum_assignment`
    2. Set `Color Map` to `Dark`
    3. Click `Update`
3. EMPO 1 barplot
    1. Check `Draw barplots?` in `Barplots` menu
    2. Click `Sample Metadata`
    3. Show sample info for `empo_1`
    4. Set `Color Map` to `Yellow-Orange-Red`
    5. Set `Length` to 150
    6. Click `Update`
4. Search for specific feature
    1. Copy `TACGTAGGTCCCGAGCGTTGTCCGGATTTATTGGGCGTAAAGCGAGCGCAGACGGTTACTTAAGCAGGATGTGAAATCCCCGGGCTCAAC` into search bar
    2. Click `Search`

After configuring the tree, you can now configure the ordination panel on the right:

1. Go to the `Color` tab on the right and select `empo_1` as the `Color Category` (in the first dropdown menu).
2. In the second dropdown menu in the `Color` tab, select `Yellow-Orange-Red`.

## Figure 1B

[Link to QZV of EMPress plot.](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig1/output/ph_EMP_empress.qzv)

1. Change `Layout` to `Circular`
2. Phylum assignment barplot
    1. Check `Draw barplots?` in `Barplots` menu
    2. Click `Feature Metadata`
    3. Color by `phylum_assignment`
    4. Set `Color Map` to `Dark`
    5. Set length to 150
3. Mean pH barplot
    1. Click `Add another layer`
    2. Click `Feature Metadata`
    3. Color by `arithmetic_mean`
    4. Set `Color Map` to `Yellow-Green-Blue`
    5. Check `Continuous values?`
    6. Set length to 150
4. Add space between barplots
    1. Check `Add a border around barplot layers?`
    2. Set `Length` to 20
    3. Click `Update`

## Figure 2A

[Link to QZV of EMPress plot.](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig2a/output/covid-plot-no-emperor.qzv)

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
    4. Set `Color Map` to `Viridis`
    5. Click `Add another layer`
    6. Color by `covid_pn_sig`
    7. Set `Color Map` to `Viridis`
    8. Check `Add a border around barplot layers?`
    9. Change `Border Color` to `black`
    10. Set border `Length` to `5`
    11. Click the `Update` Button
    12. Note: No significant difference = 0, Lower in COVID-19 samples = -1, Higher in COVID-19 samples = 1
4. Double click on the `Carbon-carbon lyases` clade (the larger red clade)
5. In `Search by node name...`, search for `4.1.1.20`
 

## Figure 2B

[Link to QZV of the EMPress plot](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig2b/output/fig2b.qzv).

To reproduce the figure within this QZV:

1. Change `Layout` to `Circular`
2. Color tips by their supperclass annotation:
    1. Use `Feature Metadata Coloring` to color by `superclass`.
    2. Set the `Extra Line Width` to `15`, hit enter.
    3. Click `Update`.
3. In the `Barplots` tab, click the checkbox marked `Draw barplots?`.
4. Add a barplot for the common meal type annotation. Within the `Layer 1` section:
    1. Click on `Sample Metadata`.
    2. Click on `Show sample info for ...` and select `common_meal_type`.
    3. Set the `Color Map` to `Accent`.
    4. Set `Length` to 700.
5. Click `Update`.

See the [notebook](https://nbviewer.jupyter.org/github/knightlab-analyses/empress-analyses/blob/master/notebooks/fig2b.ipynb) for details on how we merged the data, generated an EMPress visualization, and configured the visualization.

## Figure 2C (and Supplemental Figure 1)

[Link to QZV of the EMPress plot](https://view.qiime2.org/visualization/?src=https://raw.githubusercontent.com/knightlab-analyses/empress-analyses/master/notebooks/fig2c/output/tree-viz.qzv).

To reproduce the figure within this QZV:

1. Change `Layout` to `Circular`
2. Color tips by their phylum-level taxonomic classifications:
    1. Use `Feature Metadata Coloring` to color by `Level 2`.
    2. Set `Extra Line Width` to `15`.
    3. Click `Update`.
3. In the `Barplots` tab, click the checkbox marked `Draw barplots?`.
4. Add a barplot for the Songbird differentials. Within the `Layer 1` section:
    1. Click on `Color by...` and select `C(brushing_event)[T.before]`.
    2. Set the `Color Map` to `Red-Blue`.
    3. Check the `Continuous values?` checkbox.
    4. Set `Default length` to 500.
5. Click `Update`.
6. Add a barplot for the ALDEx2 effect sizes. Click `Add another layer`. Within
   the `Layer 2` section:
    1. Click on `Color by...` and select `sfit.effect`.
    2. Set the `Color Map` to `Red-Blue`.
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
