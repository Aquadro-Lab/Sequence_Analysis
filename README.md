# Sequence_Analysis
This is a collection of scripts that take various approaches to analyze gene sequences. Results can be insightful for evolutionary patterns as well as inform functional experiments.

Many of these analyses utilize an amino acid matrix from Miyata et al. (1979) that assigns a score to amino acid pairs that reflects their biochemical similarity. 

*Files in this repository that are not listed and described below have not been uploaded and/or polished yet.*

### Polymorphism.Rmd 
This is an R Markdown file that takes in an aligned fasta file of a gene (coding sequence) from a population. It outputs information on the derived allele frequencies and the Miyata scores of the nonsynonymous polymorphisms. The code is set to analyze the gene bag-of-marbles from a population of D. melanogaster from Zambia. To analyze your data, I've indicated which variables to change at the beginning of the file. 

### Divergence.Rmd 
This is an R Markdown file that takes in two individual fasta files consisting of aligned gene (coding) sequences from different species. It outputs information on the Miyata scores of the divergent amino acid sites. The code is set to analyze the gene bag-of-marbles from the D. melanogaster and D. simulans reference genomes, aligned with various other Drosophila species using the software PRANK. To analyze your data, I've indicated which variables to change at the beginning of the file. 

### Miyata_range.Rmd 
This is an R Markdown file that takes in two individual fasta files consisting of (1) a reference gene (coding) sequence and (2) a set of aligned gene sequences of the same gene. It outputs information on the Miyata scores for each site, e.g. what is the range and frequency of Miyata scores at each site. The code is set to analyze the output of a forward evolution simulation on the D. melanogaster bag-of-marbles gene compared to the D. mel bag-of-marbles reference genomes. To analyze your data, I've indicated which variables to change at the beginning of the file. 

### Miyata_scores.Rmd
This is an R Markdown file that takes in many individual fasta files consisting of aligned gene (coding) sequences. It outputs heatmap graphics that show the total Miyata scores (i.e. summation of Miyata scores) pairwise between input sequences. The code is set to analyze the bag-of-marbles gene between various different Drosophila species and predicted ancestral sequences. The predicted ancestral sequences were generated using PAML after aligning with PRANK. To analyze your data, I've indicated which variables to change at the beginning of the file. At the end of this file is code for two graphics that help illustrate some general information on Miyata scores.

### Degenerate_sites.Rmd
This is an R Markdown file that takes in a single nucleotide CDS fasta file. It uses the degeneracy of a site (nondegenerate, two-fold degenerate, and four-fold degenerate) to calculate the number of synonymous (nS) and nonsynonymous (nN) sites. These estimates use the formulas: nS=n4+(1/3)n2 and nN=n0+(2/3)n2 where n0 = # of nondegenerate sites, n2 = # of two-fold degenerate sites, n4 = # of four-fold degenerate sites.
