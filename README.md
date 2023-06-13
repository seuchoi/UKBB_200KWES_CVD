# UKBB_200KWES_CVD
General functions used in the main analyses for
Jurgens, Choi, Morrill et al (2021). _Analysis of rare genetic variation underlying cardiometabolic diseases and traits among 200,000 individuals in the UK Biobank._
Nat Genet. in press. Summary statistics for this paper can be found at https://cvd.hugeamp.org/downloads.html 

In particular, adaptations of and wrappers around GENESIS are included in this repository that are optimized for large-scale sequencing analyses of databases with case-control imbalance.

To use any of the functions specifically for gene-based analyses in a dataset, one only needs to source the 'GENESIS_adaptation_source.R' script. For meta-analyses, and various other pos-processing functions, other scripts are available. A list of dependencies is provided in the 'GENESIS_adaptation_source.R' script as well. More easily, you can download a tar file with all needed R-packages (and more) from [https://www.dropbox.com/scl/fo/0m3so6sfc7acsszsdlhi0/h?dl=0&rlkey=vwb5jzps5n0t97auom68sh04g ](https://www.dropbox.com/scl/fo/8vqwy4vqcv1jogtbid4zl/h?dl=0&rlkey=rymd1zuubnf88umb5c0z97x5c). For instance, when running on a Cloud machine, simply follow the following steps:

```
# First download tar file into Cloud machine, and then untar:
tar -xvf rpackages4_1_3.tar.gz

# Clone repos
git clone --branch patch-1 https://github.com/seanjosephjurgens/TOPMed_AFib_pipeline.git
git clone --branch v1.2 https://github.com/seanjosephjurgens/UKBB_200KWES_CVD.git
```

Then make sure that within R-scripts you want to run, you reference the un-tarred library and source any needed analyses scripts, for instance:
```
#!/usr/bin/env Rscript
.libPaths(c("rpackages4_1_3",.libPaths()))
source("UKBB_200KWES_CVD/Cauchy_test.R")
source("UKBB_200KWES_CVD/GENESIS_adaptation_source.R")
```

To note, this repository is under active development, and any suggestions are welcome. Also, we are happy to consider request regarding analyses in the paper not covered in this repository. 


