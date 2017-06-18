---
title: "Poisson hierarchical model to analyze allele specific RNA-seq data"
author: |
   | Ignacio Alvarez^1^, Jarad Niemi^1^ and Dan Nettleton^1^
   |
   | 1.  Department of Statistics, Iowa State University
output: html_document
bibliography: library_user.bib
---
**Keywords**: Fully Bayesian, Hierarchical model, GPU, RNAseq

Fully Bayesian inference of high dimensional hierarchical models is computationally demanding. Usually, approximations like empirical Bayes or nested Laplace are used to obtain inference results.  Parallel computing is a way to tackle down the computational intractability of this models, @Landau2016 propose to use graphics processing units (GPU) to take advantage of the embarrassingly parallel nature of the MCMC algorithms in conditional independent hierarchical models, implemented in **fbseq** package [@fbseqref]. We propose a hierarchical overdispersed Poisson model to study allelic gene expression in plants, fully Bayesian inference is obtained using **fbseq** package. 

Allele specific expression (ASE) is a measure relative of the gene expression level of each gene copy in a multiploid genome. Biologically, ASE is relevant to explain process like hybrid vigor in plants or to design possible treatments for diseases in humans. In plant breeding, hybrids are developed to take advantage of the genetic phenomenon known as heterosis or hybrid vigor. Heterosis occurs when hybrid offspring possess superior levels of one or more traits relative to their inbred parents. Recent genomic studies suggest phenotypic heterosis may be explained by heterosis in the expression levels of key genes. Furthermore, one possible reason for the occurrence of heterosis are genes where two distinct alleles at a heterozygous locus are differentially expressed

ASE has some characteristics different from regular RNAseq expression: it is not available for every gene, it present bias towards one of the alleles (reference allele), and it has always a split-plot design. We present statistical methods for modelling ASE and detecting genes where differential allele expression.  We propose a hierarchical overdispersed Poisson model that accommodates gene specific overdispersion, it has an internal measure of the reference allele bias, and use random effects to model the gene specific regression parameters. Simulation and real data analysis suggest the proposed model is a practical and powerful tool for the study of differential allele usage.


# References
