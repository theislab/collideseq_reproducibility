Read-me summarising reproducibility notebooks
=============================================

The notebooks are divided into three chapter by data set studied:

    - Chapter I: Analysis of the AFMOS (Ascl1-Foxa2-Myod1-Oct4-Sox2) data set (2 replicates scRNA-seq at 72h).
        The corresponding data sets are: 
            - download/P21037
    - Chapter II: Analysis of the AHMO (Ascl1-Hnf1a-Myod1-Oct4) data set (1 replicate scRNA-seq at 24h, 48h, 72h each and a separate measurement at 72h).
        The corresponding data sets are: 
            - download/rev6_fluorophores
    - Chapter III: Analysis of the multiome (Ascl1-mutantAscl1-Myod1) data set (1 replicate of scRNA-ATAC-seq at 72h + 2 CUT&RUN samples).
        The corresponding data sets are: 
            - download/P21060
            - download/cutnrun2

Within each chapter, the notebooks can be sequentially executed as indicated by numbering. 
They create temporary data (such as h5ad files used in subsequent notebooks) and results files (such as figure panels and tables).


The notebooks by chapter contain the following code:
    - Chapter I: 
        - R markdown notebook 1a: contains ambient RNA correction with SoupX that is used in Notebook 1.
        	Note: On GEO, the unfiltered .h5 is supplied, not the .mtx. Export this file into the .mtx format for SoupX compatibility.
        - Notebook 1: All basic unsupervised analysis of the data, preparing data objects that are used by other notebooks that perform specialised analyses.
        - Notebook 2: RNA velocity (scvelo) and Cellrank analysis.
        - Notebook 3: Analysis of developemental progress along lineages corresponding to each transcription factor.
        - Notebook 4: Predictive modelling of RNA states as a function of transgene expression.
    - Chapter II: 
        - R markdown notebook 1a: contains ambient RNA correction with SoupX that is used in Notebook 1.
        	Note: On GEO, the unfiltered .h5 is supplied, not the .mtx. Export this file into the .mtx format for SoupX compatibility.
        - Notebook 1: All basic unsupervised analysis of the data, preparing data objects that are used by other notebooks that perform specialised analyses.
        - Notebook 2: RNA velocity (scvelo) and Cellrank analysis
        - Notebook 3: Interactions of transgenes
        - Notebook 4: Doublet analysis
    - Chapter III: 
        - R markdown notebook 1a: contains ambient RNA correction with SoupX that is used in Notebook 1.
            Note: On GEO, the unfiltered .h5 is supplied, not the .mtx. Export this file into the .mtx format for SoupX compatibility.
        - Notebook 1: All basic unsupervised analysis of the data, preparing data objects that are used by other notebooks that perform specialised analyses.
        - Notebook 2: Multiome analysis including CUT&RUN data.

Notes on execution:
    - Execute notebooks within a chapter in numeric order and make sure that temporary h5ad files are accessible to subsequent notebooks.
    - All notebooks assume a common input data and results directory structure. 
        - Make sure that the data directory structure is not changed from the supplied structure. 
        - All paths are defined at the top of the notebooks and rely on absolut paths defined in a single cell. Adapt the absolute paths in that cell to your machine.
