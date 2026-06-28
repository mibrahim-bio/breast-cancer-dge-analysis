# Differential Gene Expression Analysis — GSE45827 (Breast Cancer)

## Overview
In this project I performed differential gene expression (DGE) analysis on the 
GSE45827 breast cancer microarray dataset from NCBI GEO, comparing Basal 
(Triple Negative) subtype against other subtypes (Her2, Luminal A, Luminal B).

## Dataset
- Source: NCBI GEO — GSE45827
- Platform: Affymetrix Human Genome microarray
- Samples: 141 total (41 Basal, 30 Her2, 29 Luminal A, 30 Luminal B)

## Methods
- Data retrieval using GEOparse
- Subtype separation based on GEO metadata
- Differential expression: two-sample t-test per gene
- Thresholds: p-value < 0.05, |log2FC| > 1
- Visualization: volcano plot, top genes bar chart, hierarchical heatmap

## Results
- Total genes tested: 29,873
- Significant DEGs identified: 3,745
- Upregulated in Basal: 1,742
- Downregulated in Basal: 2,003

## Key Findings
The most upregulated gene in Basal subtype was probe 205044_at (log2FC = 6.71, 
p = 1.4e-24). The most downregulated was 209173_at (log2FC = -8.52, p = 2.8e-40).
The large number of DEGs and high fold changes confirm the known molecular 
distinctiveness of Basal/Triple Negative breast cancer from hormone 
receptor-positive subtypes.

## Tools Used
Python 3, GEOparse, pandas, numpy, scipy, matplotlib, seaborn

## Files<img width="1500" height="1050" alt="volcano_plot" src="https://github.com/user-attachments/assets/f2926052-a336-4859-b5f9-7131b8f8e915" />

- genomics_analysis.ipynb — full analysis notebook with outputs
- figures/ — volcano plot, top genes chart, heatmap
- significant_DEGs.csv — list of 3,745 significant genes with stats
