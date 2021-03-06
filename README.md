[![Travis-CI Build Status](https://travis-ci.org/waldronlab/MicrobiomeWorkshop.svg?branch=master)](https://travis-ci.org/waldronlab/MicrobiomeWorkshop)

# A workshop on microbiome data analysis in Bioconductor

Bioconductor provides significant resources for microbiome data acquisition, analysis, and visualization. This workshop introduces the common analyses of differential abundance and ordination using the `phyloseq`, `edgeR`, and `DESeq2`. For data it utilizes the  `curatedMetagenomicData` package, a resource providing uniformly processed taxonomic and metabolic functional profiles for more than 6,000 whole metagenome shotgun sequencing samples from 26 publicly available studies, including the Human Microbiome Project, along with curated participant data.  At the end of this workshop, users will be able to access publicly available metagenomic data and to perform differential abundance tests, visualization and
multivariate statistical analyses of these and other data in R/Bioconductor.

Presentation materials from Dec 15, 2017 NYC R/Bioconductor Meetup: https://github.com/waldronlab/MicrobiomeWorkshop/issues/7

# Installation

Try this to install the workshop materials and open the vignette (source is in the [vignettes](./vignettes) directory):

If you do not yet have Bioconductor and devtools installed:
```
source("https://bioconductor.org/biocLite.R")
biocLite()
install.packages("devtools")
```

Then workshop-specific materials:
```
BiocInstaller::biocLite("waldronlab/curatedMetagenomicData", dependencies=TRUE)
BiocInstaller::biocLite("GenomeInfoDbData", dependencies=TRUE)
BiocInstaller::biocLite("waldronlab/microbiomeworkshop", dependencies=TRUE, build_vignettes=TRUE)
library(MicrobiomeWorkshop)
vignette("MicrobiomeWorkshop")
```
