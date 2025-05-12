# RNA-Seq-Analysis

This project contains an RNA-seq data analysis pipeline implemented in R using Quarto. The analysis includes data preprocessing, quality control, normalization, and visualization steps designed to explore gene expression patterns from raw count data.

## Features
- Reads and preprocesses raw count data
- Removes low-expression genes
- Visualizes library sizes for quality assessment
- Prepares data for downstream analysis using DESeq2

## Requirements
Make sure you have the following R packages installed:

r
install.packages(c("ggplot2", "pheatmap", "RColorBrewer", "stringr", "dplyr"))
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("DESeq2")

## File Structure
- RNA-Seq Analysis.qmd – The main analysis script written in Quarto Markdown.
- raw_counts.csv – Input file containing raw read counts (not included here; expected in your working directory).

## How to Use
- Clone or download this repository.
- Open RNA-Seq Analysis.qmd in RStudio or another Quarto-compatible editor.
- Ensure the raw_counts.csv file is placed in the path specified in the code or modify the path accordingly.
- Render the Quarto file to HTML using the “Render” button or by running:

r
quarto::quarto_render("RNA-Seq Analysis.qmd")

## Output
The rendered HTML file will include plots and summaries such as:
- Library size barplot
- Summary of raw counts
- NA checks and filtering logs
