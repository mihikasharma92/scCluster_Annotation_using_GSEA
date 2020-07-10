# scCluster_Annotation_using_GSEA
GSEA: https://www.gsea-msigdb.org/gsea/index.jsp
<br/>Generic scripts for pre-processing and running GSEA analysis.

### 1. scClusterAnnotation_GeneSetEnrichmentAnalysis.ipynb
There are various approaches to Cell Type annotation in single cell data for eg: GARNETT, SingleR etc. One of them is using Gene Set Enrichment Analysis (GSEA). This script exploits the Seurat functionality of FindAllMarkers for annotation of single cell Clusters. 
<br/>
<br/>STEP 1 creates ".gmt" (Example.gmt) file from a list of pre-acquired annotations. 
<br/>
<br/>STEP 2 uses the result of FindAllMarkers(from Seurat), to create ".rnk" (Example.rnk) files. 
<br/>
<br/>STEP 3 utilises the above 2 files to run GSEAPreranked v4.0.3 to annotate clusters to view which Gene Sets are relevant to a Cluster, thereby helping annotation. 
<br/>
<br/>STEP 4 creates a matrix to help summarise the results of GSEA analysis by parsing html results into a matrix format for each Cluster against each gene set, populating the values with "FDR q-val". 
<br/>
<br/>STEP 5 enables visualization of these results in the form of a HeatMap with Dendrogram to help categorize the similarities within clusters and also annotate them. 
<br/>
<br/>STEP 2 through STEP 5 contain sub-divisions based on the requirement to use Average log FC/ Absolute log FC/ Unweighted analysis respectively. STEP 0 enables clearing the environment of all the DataFrames to prevent incorrect results. It is imperative to run STEP 0 if running multiple cycles of STEP 4.
