# Sequence_Analysis
This is a collection of scripts that take various approaches to analyze gene sequences. Results can be insightful for evolutionary patterns as well as inform functional experiments.

Many of these analyses utilize an amino acid matrix from Miyata et al. (1979) that assigns a score to amino acid pairs that reflects their biochemical similarity. 

### Polymorphism.Rmd 
This is an R Markdown file that takes in an aligned fasta file of a gene from a population. It outputs information on the derived allele frequencies and the Miyata scores of the nonsynonymous polymorphisms. The code is set to analyze the gene bag-of-marbles from a population of D. melanogaster from Zambia. To analyze your data, I've indicated which variables to change at the beginning of the file. 

### Divergence.Rmd 
This is an R Markdown file that takes in two individual fasta files consisting of aligned gene sequences from different species. It outputs information on the Miyata scores of the divergent amino acid sites. The code is set to analyze the gene bag-of-marbles from the D. melanogaster and D. simulans reference genomes, aligned with various other Drosophila species using the software PRANK. To analyze your data, I've indicated which variables to change at the beginning of the file. 
