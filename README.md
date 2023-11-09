# A Global Transcriptional Atlas of the Effect of Sleep Loss in the Mouse Cortex

Kaitlyn Ford<sup>1*</sup>, Elena Zuin<sup>2*</sup>, Dario Righelli<sup>3</sup>, Christine Muheim<sup>1</sup>, Elizabeth Medina<sup>1</sup>, Hannah Schoch<sup>1</sup>, Kristan Singletary<sup>1</sup>, Christine Muheim<sup>1</sup>, Marcos G. Frank<sup>1</sup>, Stephanie Hicks<sup>4,5,6,7</sup>, Davide Risso<sup>3</sup> and Lucia Peixoto<sup>1</sup>
 
1. Department of Translational Medicine and Physiology, Washington State University, Spokane, WA 
2. 
3. Department of Statistical Sciences, University of Padova, Italy
4. Department of Biostatistics, Johns Hopkins Bloomberg School of Public Health, Baltimore, MD
5. Department of Biomedical Engineering, Johns Hopkins School of Medicine, Baltimore, MD, USA
6. Center for Computational Biology, Johns Hopkins University, Baltimore, MD, USA
7. Malone Center for Engineering in Healthcare, Johns Hopkins University, MD, USA


# Abstract 

Sleep deprivation (SD) has negative effects on brain function. Sleep problems are prevalent in neurodevelopmental, neurodegenerative and psychiatric disorders. Thus, understanding the molecular consequences of SD is of fundamental importance in neuroscience. In this study we present the first simultaneous bulk and single single-nuclear (sn)RNA sequencing characterization of the effects of SD in the prefrontal cortex (PFC). We show that SD predominantly affects glutamatergic neurons, specifically in layers 4 and 5, and produces isoform switching of thousands of transcripts. At both the global and cell-type specific level, SD has a large repressive effect on transcription, down-regulating thousands of genes and transcripts; underscoring the importance of accounting for the effects of sleep loss in transcriptome studies of brain function. As a resource we provide extensive characterization of cell-types, genes, transcripts and pathways affected by SD; as well as tutorials for data analysis.

## About this tutorial

This repository shares all the code developed for the analysis of the "A Global Transcriptional Atlas of the Effect of Sleep Loss in the Mouse Cortex" paper.

At the link [https://rissolab.github.io/AtlasCortexSD/](https://rissolab.github.io/AtlasCortexSD/), in the Articles section, it is possible to retrieve all the 
reports for reproducing the entire analysis.

In some cases, because some of the steps are time demanding the code is reported, 
but not live executed. 

## Docker container

To run this tutorial in a
[Docker container](ghcr.io/rissolab/atlascortexsd:latest),
pull the Docker image via

```
docker pull ghcr.io/rissolab/atlascortexsd:latest
``` 

and then run the image via

```
docker run -e PASSWORD=bioc -p 8787:8787 ghcr.io/rissolab/atlascortexsd
```

Once running, navigate to http://localhost:8787/ in your browser and login with
username `rstudio` and password `bioc`.

## Local installation

This tutorial can be installed like an ordinary R package via:

```
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

if (!require("remotes", quietly = TRUE))
    install.packages("remotes")

BiocManager::install("RissoLab/AtlasCortexSD",
                     dependencies = TRUE,
                     build_vignettes = TRUE)
```

# Data Availability

Sequencing data have been deposited in NCBI’s Gene Expression Omnibus (GEO) under the accession number GSE211088. The bulk RNA-seq replicates (5 SD, 5 HC) were previously deposited in GEO under accession number GSE113754, and downloaded from GEO for this analysis. 

# Acknowledgements:

This work was supported by the National Institute of General Medical Sciences (NIGMS) under project number R35GM147020 and by the National Institute of Neurological Disorders and Stroke (NINDS) under project number R56NS124805 to L.P.
