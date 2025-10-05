Project Overview

The code and results for Assessment 4: R Data Analysis Project (SLE777) are available in this repository.  The work is divided into:
 • Part 1: Analysis and visualisation of biological data (gene expression; tree growth).
 • Part 2: Comparative sequence analysis of Mycobacterium tuberculosis (MTB;GCA_001318445) and Escherichia coli K-12 MG1655, including protein k-mer (k=3–5) enrichment, base and amino acid composition, codon-usage bias, and CDS statistics
 
Repository Structure
.
├─ updated_assignment_4.Rmd          # Full analysis (section 1:Q1–Q11) and (section 2: q1-q6)  with code + answers
├─ updated_assignment_4.html/.pdf    # Rendered report
├─ data/
│  ├─ gene_expression.tsv            # Part 1 (Q1–Q5)
│  ├─ growth_data.csv                # Part 1 (Q6–Q10)
│  ├─ ecoli_cds.fa                   # E. coli coding sequences
│  └─ ooi_cds.fa                     # MTB coding sequences (organism of interest)
└─ README.md

Inputs

•	data/gene_expression.tsv — gene expression table (Part 1 Q1–Q5).
•	data/growth_data.csv — tree circumference by year/site (Part 1 Q6–Q10).
•	data/ecoli_cds.fa — E. coli CDS FASTA.
•	data/ooi_cds.fa — MTB (GCA_001318445) CDS FASTA; the report shows Ensembl path used to obtain MTB CDS (see Q1 setup: section 2)

Outputs (what the Rmd produces)

•	Tables: CDS counts, total coding DNA (Mb), mean/median CDS length, base & AA frequencies, codon usage (counts, freq, RSCU), k-mer enrichment.
•	Plots: Histograms/boxplots (Part 1), barplots for nucleotide & amino-acid frequency (Part 2), codon-usage visualisations, and k-mer over/under representation plots—supporting Q15–Q16 as required. 

How to Reproduce

1.	Open updated_assignment_4.Rmd in RStudio (R ≥ 4.x).
2.	Ensure seqinr, ggplot2, dplyr, tibble, and R.utils are installed.
3.	Knit to HTML/PDF.
o	The Rmd reads ecoli_cds.fa and ooi_cds.fa (MTB) and generates Q1–Q6 outputs (e.g., MTB CDS = 4741).


Method Summary (mapped to questions)

•	Q1–Q2: Load FASTA, count CDS number and sum coding nucleotides; present side-by-side for E. coli vs MTB. Your report shows E. coli: 4239 CDS; MTB: 4741 CDS, with total coding Mb accordingly. 

•	Q3: Compute CDS lengths and visualise via boxplot; report mean/median per organism. (table: E. coli mean 938.6 nt vs MTB 649.0 nt.) 

•	Q4: Count A/C/G/T and AA totals → barplots for each organism; compare composition (MTB high-GC vs E. coli balanced). 

•	Q5: Build codon usage tables (counts, frequency, RSCU); compare bias across species; include supporting charts. ( merged codon table includes AA, counts, freq, RSCU for E. coli & MTB.) 

•	Q6: Translate CDS to proteins, count k-mers (k=3–5), compute log2 enrichment (MTB vs E. coli); present top over/under-represented motifs with plots and a short biological rationale (GC bias, codon preference). Requirement to provide plots is stated in the brief

