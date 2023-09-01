# Bioinformatics pipeline for "Experimental evidence on the influence of root-associated fungi on plant growth along altitude"

This pipeline is a pre-release version of the [OptimOTU pipeline](https://www.github.com/brendanf/optimotu-pipeline), which is
implemented in R using the [{targets}](https://books.ropensci.org/targets/)
pipeline tool.
It is probably difficult to run it outside of the [CSC](https://www.csc.fi)
Puhti computing cluster where it was developed and executed for this project,
and the code is included primarily for reference purposes to accompany the paper.
A more portable and user-friendly execution process will be implemented in the
public release of the OptimOTU pipeline R package.

That said, in principle the steps to execute it would be:

1) Clone this Git repository

2) Install all prerequisites listed in `conda/bistorta_vivipara_pipeline.yaml`,
either using [conda](https://anaconda.org) or by other means.
If using conda, activate the conda environment.

3) Download ProtaxFungi (link TBD) and unzip it into the sister directory

4) Download the raw sequence files (link TBD) into `sequences/01_raw`

5) In R:

```R
library(targets)
tar_make()
```
