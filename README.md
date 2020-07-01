# GSEA_Analysis
Generic scripts to create .gmt and .rnk files for GSEA analysis and run GSEA analysis.

### 1. scClusterAnnotation_GeneSetEnrichmentAnalysis.ipynb
There are various approaches to Cell Type annotation in single cell data for eg: GARNETT, SingleR etc. One of them is using Gene Set Enrichment Analysis (GSEA). This script exploits the Seurat functionality of FindAllMarkers for annotation of single cell Clusters. In the first step, the script creates ".gmt" file from a list of pre-acquired annotations. The second step uses the result of FindAllMarkers, to create ".rnk" files. The thrird step utilises the above 2 files to run GSEAPreranked v4.0.3 to annotate clusters to view which Gene Sets are Up/Down regulated in a Clsuter, thereby helping annotation. 

