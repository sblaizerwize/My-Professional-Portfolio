# Integrative Analysis of Differential Gene Expression, Transcript Usage, and RNA Secondary Structure in Early- and Late-Onset Colorectal Cancer

by Salomon Marquez

11/02/2025 

This site contains a summary of my bioinformatics master's thesis developed at CIMA University of Navarra under the supervision of Fernando Pastor Rodriguez and Igor Ruiz de los Mozos.

For a detailed overview of the project, you can check the following resources:

- :material-file-document: [Thesis document](integrative-analysis-dge-dtu-rss-crc/reports/project-progress/tfm-bioinformatics-semv-manuscript.pdf)
- :material-github: [GitHub repository](https://github.com/sblaizerwize/master-bioinformatics)
- :octicons-video-24: [YouTube video](https://youtu.be/atpuYKZB7xI)

<div style="display: flex; justify-content: center;">
  <iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/atpuYKZB7xI?si=yhnjEBqGL0c8NW1M"
    title="YouTube video player"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>


---
## Abstract

Colorectal cancer is increasingly diagnosed in individuals younger than 50 years, a
trend referred to as early-onset colorectal cancer. This study applied an integrative
transcriptomic workflow to characterize molecular differences between early-onset
and late-onset colorectal cancer. A total of 86 matched tumor and normal samples
were analyzed using a combination of differential gene expression, differential
transcript usage, and RNA secondary structure prediction.

Differential gene expression analysis identified a 40-gene signature uniquely deregulated
in early-onset colorectal cancer, enriched in immune-related, inflammatory, and
cell-matrix adhesion processes. Differential transcript usage analysis revealed substantial
differences in transcript-level complexity between cohorts, with late-onset
colorectal cancer showing extensive isoform remodeling, whereas early-onset tumors
displayed a more restricted pattern of transcript usage. Despite these global differences,
six conserved isoform switches were consistently detected in both cohorts,
including TPM2, LMNB2, MAP3K20, and the long non-coding RNA HOXB-AS3.
RNA secondary structure prediction further characterized significant isoforms, revealing
a predominance of stem motifs.

These results indicate that gene-level and isoform-level analyses capture complementary
aspects of colorectal cancer transcriptomic variation. The integrative framework
presented here provides a methodological basis for future large-scale studies
and supports the exploration of RNA structural features as potential biomarkers
and therapeutic targets in colorectal cancer.

**keywords**: `colorectal-cancer`, `deseq2-analysis`, `dtu-analysis`, `rna-structure-prediction`, `nf-core-rnaseq`, `isoformSwitchAnalyzeR`, `hpc-cluster`, `nextflow`

---
## Objective  

The primary goal of this project is to identify genes and transcripts that are differentially
regulated in early-onset and late-onset colorectal cancer, and to evaluate whether changes
in isoform usage are associated with differences in their RNA secondary structure through
computational prediction.

---
## Proposed solution
We adopted an integrative transcriptomic strategy to investigate molecular differences
between early-onset and late-onset colorectal cancer (EOCRC and LOCRC). Building
upon a previously conducted gene-level study from [Marx et al.](https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2024.1365762/full), we extend the analysis by incorporating
isoform-level regulation and RNA secondary structure prediction, thereby moving beyond expression
changes alone to explore post-transcriptional and structural layers of regulation. The overall integrative analysis workflow is summarized below:

![tfm-workflow](integrative-analysis-dge-dtu-rss-crc/images/tfm-schematics.svg)
Schematic overview of the integrative transcriptomic analysis workflow implemented in this study.

---
## From concept to implementation
The main milestones of this project were tracked using a dedicated 🏁 [roadmap](https://github.com/users/sblaizerwize/projects/5/views/4?visibleFields=%5B%22Title%22%2C%22Status%22%2C%22Milestone%22%2C224733603%2C224733604%5D&sortedBy%5Bdirection%5D=desc&sortedBy%5BcolumnId%5D=224733604) on GitHub projects, which facilitated version control and documentation of analytical decisions. Among these decisions, the main technical and methodological challenges encountered during the development of this project and the mitigation strategies adopted are listed below:

- [Report 1](integrative-analysis-dge-dtu-rss-crc/reports/project-progress/tfm-proposal.pdf) - the proposal
- [Report 2](integrative-analysis-dge-dtu-rss-crc/reports/project-progress/tfm-report-update-1.pdf) - the starting point
- [Report 3](integrative-analysis-dge-dtu-rss-crc/reports/project-progress/tfm-report-update-2.pdf) - the tipping point

---
## Summary of products obtained
This project produced the following deliverables.

- :material-file-document: A [master’s thesis manuscript](integrative-analysis-dge-dtu-rss-crc/reports/project-progress/tfm-bioinformatics-semv-manuscript.pdf) documenting the analytical workflow, results, and their
biological interpretation.
- :simple-nextflow: A configured and validated **nf-core/rnaseq Nextflow pipeline** for reproducible RNA-seq
analysis on high-performance computing (HPC) clusters.
- :simple-zenodo: A [Zenodo repository](https://doi.org/10.5281/zenodo.17801437) hosting primary and processed
data generated in this study.
- :material-github: A [GitHub repository](https://github.com/sblaizerwize/master-bioinformatics) containing primary scripts and documentation.

---
## Results
This is a summary of results after the implementation of the integrative transcriptomic workflow for the analysis of EOCRC and LOCRC samples.

### **1. nf-core/rnaseq pipeline — EOCRC**
SRA study [SRP357925](https://trace.ncbi.nlm.nih.gov/Traces/index.html?view=study&acc=SRP357925)  
21 EOCRC patient pairs

- [MultiQC Report](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-42samples/multiqc_report.html)
- [Nextflow Report](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-42samples/report.html)
- [Nextflow Timeline](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-42samples/timeline.html)

### **2. nf-core/rnaseq pipeline — LOCRC**
SRA study [SRP479528](https://trace.ncbi.nlm.nih.gov/Traces/index.html?study=SRP479528)  
22 LOCRC patient pairs

- [MultiQC Report](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-44samples/multiqc_report.html)
- [Nextflow Report](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-44samples/report.html)
- [Nextflow Timeline](integrative-analysis-dge-dtu-rss-crc/reports/nfcore-rnaseq-44samples/timeline.html)

### **3. Differential Gene Expression (DGE)**
- [EOCRC samples](integrative-analysis-dge-dtu-rss-crc/reports/dge-analysis/Deseq2_42crc.html)
- [LOCRC samples](integrative-analysis-dge-dtu-rss-crc/reports/dge-analysis/Deseq2_44crc.html)

### **4. Differential Transcript Usage (DTU)**

- IsoformSwitchAnalyzeR Analysis

??? note "Show R script"

    === "Input"

        ``` r
        # Install and load modules and libraries 
        .libPaths("~/R/x86_64-pc-linux-gnu-library/4.4")
        
        # Check if package is installed, if not then install
        if (!require("IsoformSwitchAnalyzeR", quietly = TRUE)) {
            if (!require("BiocManager", quietly = TRUE))
                install.packages("BiocManager")
            BiocManager::install("IsoformSwitchAnalyzeR")
        }
        
        library(scales)
        library(ggplot2)
        library(tidyr)
        library(dplyr)
        library(S4Vectors)
        library(reshape2)
        library(corrplot)
        library(factoextra)
        library(SummarizedExperiment)
        library(DESeq2)
        library(IsoformSwitchAnalyzeR)
        library(tidyverse)
        library(dbplyr)
        library(BiocParallel)
        library(Biostrings)
        
        ## ------------------------------------------------------------------------------------------------
        # Adjust workers according to cluster cores
        ncores <- 16
        register(MulticoreParam(workers = ncores))
        
        # Import quantifications
        salmonQuant <- importIsoformExpression(
            parentDir = "dtu_data/salmon"
        )
        
        head(salmonQuant$abundance, 2)
        head(salmonQuant$counts, 2)
        
        saveRDS(salmonQuant, file = "dtu_data/salmonQuant_42_44.rds")
        
        ## ------------------------------------------------------------------------------------------------
        # Read 'se' object 
        se_42 <- readRDS("dtu_data/gene.SummarizedExperiment.metadata_42.rds")
        se_44 <- readRDS("dtu_data/gene.SummarizedExperiment.metadata_44.rds")
        
        # Display 'se' object
        se_42
        se_44
        
        # Display colNames 
        colnames(se_42)
        colnames(se_44)
        
        # Display condition
        colData(se_42)$condition
        colData(se_44)$condition
        
        # Display condition in salmonQuant
        colnames(salmonQuant$abundance)
        
        ## ------------------------------------------------------------------------------------------------
        # Define design matrix
        myDesign <- data.frame(
            sampleID = colnames(salmonQuant$abundance)[-1],    # Exclude isoform_id column and include all sample names
            condition = c(colData(se_42)$condition, colData(se_44)$condition)  # Combine conditions from both se_42 and se_44
        )
        myDesign
        
        # Define comparisonsToMake
        mycomparisonsToMake <- data.frame(
            condition_1 = c("normal_eocrc", "normal_locrc"),
            condition_2 = c("tumor_eocrc", "tumor_locrc") 
        )
        mycomparisonsToMake
        
        ## ------------------------------------------------------------------------------------------------
        cat("1. Create switchAnalyzeRlist...\n")
        
        # Create switchAnalyzeRlist
        aSwitchList <- importRdata(
            isoformCountMatrix   = salmonQuant$counts,
            isoformRepExpression = salmonQuant$abundance,
            designMatrix         = myDesign,
            comparisonsToMake    = mycomparisonsToMake,
            isoformExonAnnoation = "dtu_data/gencode.v49.primary_assembly.annotation.gtf.gz",
            isoformNtFasta       = "dtu_data/gencode.v49.transcripts.fa.gz",
            fixStringTieAnnotationProblem = TRUE,
            showProgress = TRUE
        )
        
        cat("View aSwitchList summary...\n")
        
        # View summary report
        summary(aSwitchList)
        saveRDS(aSwitchList, file = "dtu_outputs/aSwitchList_gencode_42_44.rds")
        
        ## ------------------------------------------------------------------------------------------------
        cat("2. Prefiltering...\n")
        cat("Prefiltering summary with geneExpressionCutoff = 1; isoformExpressionCutoff = 0; Isoform fraction = 0...\n")
        
        # Prefilter
        mySwitchList <- preFilter(aSwitchList)
        summary(mySwitchList)
        saveRDS(mySwitchList, file = "dtu_outputs/mySwitchList_gencode_42_44_filstandard.rds")
        
        ## ------------------------------------------------------------------------------------------------
        cat("3. Differential Expression Analysis using TestSatuRn...\n")
        
        # Identify differentially used isoforms with SatuRn
        mySwitchList <- isoformSwitchTestSatuRn(
            mySwitchList,
            reduceToSwitchingGenes = TRUE,  # focus on switching genes relevant to CRC
            showProgress = TRUE
        )
        
        # Summarize results
        extractSwitchSummary(mySwitchList)
        
        ## ------------------------------------------------------------------------------------------------
        cat("4. Obtain Open Reading Frames (ORFs)...\n")
        
        # Obtain Open Reading Frames (ORFs)
        mySwitchList <- analyzeORF(
            mySwitchList,
            showProgress = TRUE 
        )
        
        ## ------------------------------------------------------------------------------------------------
        cat("5. Extracting sequences...\n")
        
        # Extract Sequences
        mySwitchList <- extractSequence(
            mySwitchList,
            outputPrefix = "dtu_42_44"
        )
        saveRDS(mySwitchList, file = "dtu_outputs/mySwitchList_42_44_nt.rds")
        
        ## ------------------------------------------------------------------------------------------------
        cat("6. Alternative and intron retention analysis...\n")
        
        # Analyze alternative splicing
        mySwitchList <- analyzeAlternativeSplicing(
            switchAnalyzeRlist = mySwitchList,
            quiet = TRUE
        )
        
        ## ------------------------------------------------------------------------------------------------
        # Analyze Intron Retention
        mySwitchList <- analyzeIntronRetention(
            switchAnalyzeRlist = mySwitchList,
            onlySwitchingGenes = TRUE,
            alpha = 0.05,
            dIFcutoff = 0.1,
            showProgress = TRUE,
            quiet = TRUE
        )
        
        saveRDS(mySwitchList, file = "dtu_outputs/mySwitchList_Asplicing_Iretention_42_44.rds")
        
        # Extract 10 top switching genes (by q-value)
        extractTopSwitches(
            mySwitchList, 
            filterForConsequences = FALSE, 
            n = 10, 
            sortByQvals = TRUE
        )
        
        ## ------------------------------------------------------------------------------------------------
        cat("7. Analyze Consequences of Isoform Switches...\n")
        
        # AnalyzeSwitchConsequences
        # tss -> alternative 5'UTR
        # tts -> alternative 3'UTR
        
        consequencesOfInterest <- c(
            "tss",
            "tts",
            "exon_number",
            "intron_structure",
            "intron_retention"
        )
        
        bioMechanismeAnalysis <- analyzeSwitchConsequences(
            mySwitchList,
            consequencesToAnalyze = consequencesOfInterest, 
            showProgress = TRUE
        )
        
        extractSwitchSummary(bioMechanismeAnalysis, filterForConsequences = FALSE)
        extractSwitchSummary(bioMechanismeAnalysis, filterForConsequences = TRUE)
        
        saveRDS(bioMechanismeAnalysis, file = "dtu_outputs/mySwitchList_consequences_42_44.rds")
        ```

    === "Output"

        ``` r
        class: SummarizedExperiment 
        dim: 78428 42 
        metadata(8): abstract Accession ... Submission Relevance
        assays(5): counts counts_length_scaled counts_scaled lengths tpm
        rownames(78428): ENSG00000000003.17 ENSG00000000005.6 ...
          ENSG00000310592.1 ENSG00000310593.1
        rowData names(3): transcript_id gene_id gene_name
        colnames(42): srr17866817 srr17866818 ... srr17866857 srr17866858
        colData names(32): age_at_surgery tissue ... source_name condition
        class: SummarizedExperiment 
        dim: 78428 44 
        metadata(9): abstract Accession ... Submission Relevance
        assays(5): counts counts_length_scaled counts_scaled lengths tpm
        rownames(78428): ENSG00000000003.17 ENSG00000000005.6 ...
          ENSG00000310592.1 ENSG00000310593.1
        rowData names(3): transcript_id gene_id gene_name
        colnames(44): srr27320655 srr27320656 ... srr27320697 srr27320698
        colData names(33): age_at_surgery tissue ... source_name condition
        [1] "srr17866817" "srr17866818" "srr17866819" "srr17866820" "srr17866821"
        [6] "srr17866822" "srr17866823" "srr17866824" "srr17866825" "srr17866826"
        [11] "srr17866827" "srr17866828" "srr17866829" "srr17866830" "srr17866831"
        [16] "srr17866832" "srr17866833" "srr17866834" "srr17866835" "srr17866836"
        [21] "srr17866837" "srr17866838" "srr17866839" "srr17866840" "srr17866841"
        [26] "srr17866842" "srr17866843" "srr17866844" "srr17866845" "srr17866846"
        [31] "srr17866847" "srr17866848" "srr17866849" "srr17866850" "srr17866851"
        [36] "srr17866852" "srr17866853" "srr17866854" "srr17866855" "srr17866856"
        [41] "srr17866857" "srr17866858"
        [1] "srr27320655" "srr27320656" "srr27320657" "srr27320658" "srr27320659"
        [6] "srr27320660" "srr27320661" "srr27320662" "srr27320663" "srr27320664"
        [11] "srr27320665" "srr27320666" "srr27320667" "srr27320668" "srr27320669"
        [16] "srr27320670" "srr27320671" "srr27320672" "srr27320673" "srr27320674"
        [21] "srr27320675" "srr27320676" "srr27320677" "srr27320678" "srr27320679"
        [26] "srr27320680" "srr27320681" "srr27320682" "srr27320683" "srr27320684"
        [31] "srr27320685" "srr27320686" "srr27320687" "srr27320688" "srr27320689"
        [36] "srr27320690" "srr27320691" "srr27320692" "srr27320693" "srr27320694"
        [41] "srr27320695" "srr27320696" "srr27320697" "srr27320698"
        [1] tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc 
        [6] normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc
        [11] tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc 
        [16] normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc
        [21] tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc 
        [26] normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc
        [31] tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc 
        [36] normal_eocrc tumor_eocrc  normal_eocrc tumor_eocrc  normal_eocrc
        [41] tumor_eocrc  normal_eocrc
        Levels: normal_eocrc tumor_eocrc
        [1] normal_locrc tumor_locrc  normal_locrc tumor_locrc  normal_locrc
        [6] tumor_locrc  normal_locrc tumor_locrc  normal_locrc tumor_locrc 
        [11] normal_locrc tumor_locrc  normal_locrc tumor_locrc  normal_locrc
        [16] tumor_locrc  normal_locrc tumor_locrc  normal_locrc tumor_locrc 
        [21] normal_locrc tumor_locrc  normal_locrc tumor_locrc  normal_locrc
        [26] tumor_locrc  normal_locrc tumor_locrc  normal_locrc tumor_locrc 
        [31] normal_locrc tumor_locrc  normal_locrc tumor_locrc  normal_locrc
        [36] tumor_locrc  normal_locrc tumor_locrc  normal_locrc tumor_locrc 
        [41] normal_locrc tumor_locrc  normal_locrc tumor_locrc 
        Levels: normal_locrc tumor_locrc
        [1] "isoform_id"  "srr17866817" "srr17866818" "srr17866819" "srr17866820"
        [6] "srr17866821" "srr17866822" "srr17866823" "srr17866824" "srr17866825"
        [11] "srr17866826" "srr17866827" "srr17866828" "srr17866829" "srr17866830"
        [16] "srr17866831" "srr17866832" "srr17866833" "srr17866834" "srr17866835"
        [21] "srr17866836" "srr17866837" "srr17866838" "srr17866839" "srr17866840"
        [26] "srr17866841" "srr17866842" "srr17866843" "srr17866844" "srr17866845"
        [31] "srr17866846" "srr17866847" "srr17866848" "srr17866849" "srr17866850"
        [36] "srr17866851" "srr17866852" "srr17866853" "srr17866854" "srr17866855"
        [41] "srr17866856" "srr17866857" "srr17866858" "srr27320655" "srr27320656"
        [46] "srr27320657" "srr27320658" "srr27320659" "srr27320660" "srr27320661"
        [51] "srr27320662" "srr27320663" "srr27320664" "srr27320665" "srr27320666"
        [56] "srr27320667" "srr27320668" "srr27320669" "srr27320670" "srr27320671"
        [61] "srr27320672" "srr27320673" "srr27320674" "srr27320675" "srr27320676"
        [66] "srr27320677" "srr27320678" "srr27320679" "srr27320680" "srr27320681"
        [71] "srr27320682" "srr27320683" "srr27320684" "srr27320685" "srr27320686"
        [76] "srr27320687" "srr27320688" "srr27320689" "srr27320690" "srr27320691"
        [81] "srr27320692" "srr27320693" "srr27320694" "srr27320695" "srr27320696"
        [86] "srr27320697" "srr27320698"
              sampleID    condition
        1  srr17866817  tumor_eocrc
        2  srr17866818 normal_eocrc
        3  srr17866819  tumor_eocrc
        4  srr17866820 normal_eocrc
        5  srr17866821  tumor_eocrc
        6  srr17866822 normal_eocrc
        7  srr17866823  tumor_eocrc
        8  srr17866824 normal_eocrc
        9  srr17866825  tumor_eocrc
        10 srr17866826 normal_eocrc
        11 srr17866827  tumor_eocrc
        12 srr17866828 normal_eocrc
        13 srr17866829  tumor_eocrc
        14 srr17866830 normal_eocrc
        15 srr17866831  tumor_eocrc
        16 srr17866832 normal_eocrc
        17 srr17866833  tumor_eocrc
        18 srr17866834 normal_eocrc
        19 srr17866835  tumor_eocrc
        20 srr17866836 normal_eocrc
        21 srr17866837  tumor_eocrc
        22 srr17866838 normal_eocrc
        23 srr17866839  tumor_eocrc
        24 srr17866840 normal_eocrc
        25 srr17866841  tumor_eocrc
        26 srr17866842 normal_eocrc
        27 srr17866843  tumor_eocrc
        28 srr17866844 normal_eocrc
        29 srr17866845  tumor_eocrc
        30 srr17866846 normal_eocrc
        31 srr17866847  tumor_eocrc
        32 srr17866848 normal_eocrc
        33 srr17866849  tumor_eocrc
        34 srr17866850 normal_eocrc
        35 srr17866851  tumor_eocrc
        36 srr17866852 normal_eocrc
        37 srr17866853  tumor_eocrc
        38 srr17866854 normal_eocrc
        39 srr17866855  tumor_eocrc
        40 srr17866856 normal_eocrc
        41 srr17866857  tumor_eocrc
        42 srr17866858 normal_eocrc
        43 srr27320655 normal_locrc
        44 srr27320656  tumor_locrc
        45 srr27320657 normal_locrc
        46 srr27320658  tumor_locrc
        47 srr27320659 normal_locrc
        48 srr27320660  tumor_locrc
        49 srr27320661 normal_locrc
        50 srr27320662  tumor_locrc
        51 srr27320663 normal_locrc
        52 srr27320664  tumor_locrc
        53 srr27320665 normal_locrc
        54 srr27320666  tumor_locrc
        55 srr27320667 normal_locrc
        56 srr27320668  tumor_locrc
        57 srr27320669 normal_locrc
        58 srr27320670  tumor_locrc
        59 srr27320671 normal_locrc
        60 srr27320672  tumor_locrc
        61 srr27320673 normal_locrc
        62 srr27320674  tumor_locrc
        63 srr27320675 normal_locrc
        64 srr27320676  tumor_locrc
        65 srr27320677 normal_locrc
        66 srr27320678  tumor_locrc
        67 srr27320679 normal_locrc
        68 srr27320680  tumor_locrc
        69 srr27320681 normal_locrc
        70 srr27320682  tumor_locrc
        71 srr27320683 normal_locrc
        72 srr27320684  tumor_locrc
        73 srr27320685 normal_locrc
        74 srr27320686  tumor_locrc
        75 srr27320687 normal_locrc
        76 srr27320688  tumor_locrc
        77 srr27320689 normal_locrc
        78 srr27320690  tumor_locrc
        79 srr27320691 normal_locrc
        80 srr27320692  tumor_locrc
        81 srr27320693 normal_locrc
        82 srr27320694  tumor_locrc
        83 srr27320695 normal_locrc
        84 srr27320696  tumor_locrc
        85 srr27320697 normal_locrc
        86 srr27320698  tumor_locrc
        1. Create switchAnalyzeRlist...

          |                                                                            
          |                                                                      |   0%
          |                                                                            
          |==================                                                    |  25%
          |                                                                            
          |===================================                                   |  50%
          |                                                                            
          |====================================================                  |  75%
          |                                                                            
          |======================================================================| 100%

          |                                                                            
          |                                                                      |   0%
          |                                                                            
          |============                                                          |  17%
          |                                                                            
          |=======================                                               |  33%
          |                                                                            
          |===================================                                   |  50%
          |                                                                            
          |===============================================                       |  67%
          |                                                                            
          |==========================================================            |  83%
          |                                                                            
          |======================================================================| 100%
                            comparison estimated_genes_with_dtu
        1 normal_eocrc vs normal_locrc              1027 - 1712
        2  normal_eocrc vs tumor_eocrc                214 - 357
        3   tumor_eocrc vs tumor_locrc               858 - 1429
        View aSwitchList summary...
        This switchAnalyzeRlist list contains:
        398518 isoforms from 58088 genes
        6 comparison from 4 conditions (in total 86 samples)

        Feature analyzed:
        [1] "ORFs, ntSequence"
        2. Prefiltering...
        Prefiltering summary with geneExpressionCutoff = 1; isoformExpressionCutoff = 0; Isoform fraction = 0...
        This switchAnalyzeRlist list contains:
        119137 isoforms from 14067 genes
        6 comparison from 4 conditions (in total 86 samples)

        Feature analyzed:
        [1] "ORFs, ntSequence"

        [1] "SatuRn results with standard prefiltering...\n"
                          Comparison nrIsoforms nrSwitches nrGenes
        1 normal_eocrc vs tumor_eocrc         14         10      10
        2 normal_locrc vs tumor_locrc        133        122     104
        3                    Combined        140        128     109

          |                                                                            
          |                                                                      |   0%
          |                                                                            
          |                                                                      |   1%
          |                                                                            
          |=                                                                     |   1%
          |                                                                            
          |=                                                                     |   2%
          |                                                                            
          |==                                                                    |   2%
          |                                                                            
          |==                                                                    |   3%
          |                                                                            
          |===                                                                   |   4%
          |                                                                            
          |===                                                                   |   5%
          |                                                                            
          |====                                                                  |   5%
          |                                                                            
          |====                                                                  |   6%
          |                                                                            
          |=====                                                                 |   6%
          |                                                                            
          |=====                                                                 |   7%
          |                                                                            
          |=====                                                                 |   8%
          |                                                                            
          |======                                                                |   8%
          |                                                                            
          |======                                                                |   9%
          |                                                                            
          |=======                                                               |   9%
          |                                                                            
          |=======                                                               |  10%
          |                                                                            
          |=======                                                               |  11%
          |                                                                            
          |========                                                              |  11%
          |                                                                            
          |========                                                              |  12%
          |                                                                            
          |=========                                                             |  12%
          |                                                                            
          |=========                                                             |  13%
          |                                                                            
          |=========                                                             |  14%
          |                                                                            
          |==========                                                            |  14%
          |                                                                            
          |==========                                                            |  15%
          |                                                                            
          |===========                                                           |  15%
          |                                                                            
          |===========                                                           |  16%
          |                                                                            
          |============                                                          |  17%
          |                                                                            
          |============                                                          |  18%
          |                                                                            
          |=============                                                         |  18%
          |                                                                            
          |=============                                                         |  19%
          |                                                                            
          |==============                                                        |  19%
          |                                                                            
          |==============                                                        |  20%
          |                                                                            
          |==============                                                        |  21%
          |                                                                            
          |===============                                                       |  21%
          |                                                                            
          |===============                                                       |  22%
          |                                                                            
          |================                                                      |  22%
          |                                                                            
          |================                                                      |  23%
          |                                                                            
          |=================                                                     |  24%
          |                                                                            
          |=================                                                     |  25%
          |                                                                            
          |==================                                                    |  25%
          |                                                                            
          |==================                                                    |  26%
          |                                                                            
          |===================                                                   |  26%
          |                                                                            
          |===================                                                   |  27%
          |                                                                            
          |===================                                                   |  28%
          |                                                                            
          |====================                                                  |  28%
          |                                                                            
          |====================                                                  |  29%
          |                                                                            
          |=====================                                                 |  29%
          |                                                                            
          |=====================                                                 |  30%
          |                                                                            
          |=====================                                                 |  31%
          |                                                                            
          |======================                                                |  31%
          |                                                                            
          |======================                                                |  32%
          |                                                                            
          |=======================                                               |  32%
          |                                                                            
          |=======================                                               |  33%
          |                                                                            
          |=======================                                               |  34%
          |                                                                            
          |========================                                              |  34%
          |                                                                            
          |========================                                              |  35%
          |                                                                            
          |=========================                                             |  35%
          |                                                                            
          |=========================                                             |  36%
          |                                                                            
          |==========================                                            |  37%
          |                                                                            
          |==========================                                            |  38%
          |                                                                            
          |===========================                                           |  38%
          |                                                                            
          |===========================                                           |  39%
          |                                                                            
          |============================                                          |  39%
          |                                                                            
          |============================                                          |  40%
          |                                                                            
          |============================                                          |  41%
          |                                                                            
          |=============================                                         |  41%
          |                                                                            
          |=============================                                         |  42%
          |                                                                            
          |==============================                                        |  42%
          |                                                                            
          |==============================                                        |  43%
          |                                                                            
          |===============================                                       |  44%
          |                                                                            
          |===============================                                       |  45%
          |                                                                            
          |================================                                      |  45%
          |                                                                            
          |================================                                      |  46%
          |                                                                            
          |=================================                                     |  46%
          |                                                                            
          |=================================                                     |  47%
          |                                                                            
          |=================================                                     |  48%
          |                                                                            
          |==================================                                    |  48%
          |                                                                            
          |==================================                                    |  49%
          |                                                                            
          |===================================                                   |  49%
          |                                                                            
          |===================================                                   |  50%
          |                                                                            
          |===================================                                   |  51%
          |                                                                            
          |====================================                                  |  51%
          |                                                                            
          |====================================                                  |  52%
          |                                                                            
          |=====================================                                 |  52%
          |                                                                            
          |=====================================                                 |  53%
          |                                                                            
          |=====================================                                 |  54%
          |                                                                            
          |======================================                                |  54%
          |                                                                            
          |======================================                                |  55%
          |                                                                            
          |=======================================                               |  55%
          |                                                                            
          |=======================================                               |  56%
          |                                                                            
          |========================================                              |  57%
          |                                                                            
          |========================================                              |  58%
          |                                                                            
          |=========================================                             |  58%
          |                                                                            
          |=========================================                             |  59%
          |                                                                            
          |==========================================                            |  59%
          |                                                                            
          |==========================================                            |  60%
          |                                                                            
          |==========================================                            |  61%
          |                                                                            
          |===========================================                           |  61%
          |                                                                            
          |===========================================                           |  62%
          |                                                                            
          |============================================                          |  62%
          |                                                                            
          |============================================                          |  63%
          |                                                                            
          |=============================================                         |  64%
          |                                                                            
          |=============================================                         |  65%
          |                                                                            
          |==============================================                        |  65%
          |                                                                            
          |==============================================                        |  66%
          |                                                                            
          |===============================================                       |  66%
          |                                                                            
          |===============================================                       |  67%
          |                                                                            
          |===============================================                       |  68%
          |                                                                            
          |================================================                      |  68%
          |                                                                            
          |================================================                      |  69%
          |                                                                            
          |=================================================                     |  69%
          |                                                                            
          |=================================================                     |  70%
          |                                                                            
          |=================================================                     |  71%
          |                                                                            
          |==================================================                    |  71%
          |                                                                            
          |==================================================                    |  72%
          |                                                                            
          |===================================================                   |  72%
          |                                                                            
          |===================================================                   |  73%
          |                                                                            
          |===================================================                   |  74%
          |                                                                            
          |====================================================                  |  74%
          |                                                                            
          |====================================================                  |  75%
          |                                                                            
          |=====================================================                 |  75%
          |                                                                            
          |=====================================================                 |  76%
          |                                                                            
          |======================================================                |  77%
          |                                                                            
          |======================================================                |  78%
          |                                                                            
          |=======================================================               |  78%
          |                                                                            
          |=======================================================               |  79%
          |                                                                            
          |========================================================              |  79%
          |                                                                            
          |========================================================              |  80%
          |                                                                            
          |========================================================              |  81%
          |                                                                            
          |=========================================================             |  81%
          |                                                                            
          |=========================================================             |  82%
          |                                                                            
          |==========================================================            |  82%
          |                                                                            
          |==========================================================            |  83%
          |                                                                            
          |===========================================================           |  84%
          |                                                                            
          |===========================================================           |  85%
          |                                                                            
          |============================================================          |  85%
          |                                                                            
          |============================================================          |  86%
          |                                                                            
          |=============================================================         |  86%
          |                                                                            
          |=============================================================         |  87%
          |                                                                            
          |=============================================================         |  88%
          |                                                                            
          |==============================================================        |  88%
          |                                                                            
          |==============================================================        |  89%
          |                                                                            
          |===============================================================       |  89%
          |                                                                            
          |===============================================================       |  90%
          |                                                                            
          |===============================================================       |  91%
          |                                                                            
          |================================================================      |  91%
          |                                                                            
          |================================================================      |  92%
          |                                                                            
          |=================================================================     |  92%
          |                                                                            
          |=================================================================     |  93%
          |                                                                            
          |=================================================================     |  94%
          |                                                                            
          |==================================================================    |  94%
          |                                                                            
          |==================================================================    |  95%
          |                                                                            
          |===================================================================   |  95%
          |                                                                            
          |===================================================================   |  96%
          |                                                                            
          |====================================================================  |  97%
          |                                                                            
          |====================================================================  |  98%
          |                                                                            
          |===================================================================== |  98%
          |                                                                            
          |===================================================================== |  99%
          |                                                                            
          |======================================================================|  99%
          |                                                                            
          |======================================================================| 100%
                    gene_ref gene_id gene_name  condition_1 condition_2
        1  geneComp_00055095    TPM2      TPM2 normal_eocrc tumor_eocrc
        2  geneComp_00110879  SORBS2    SORBS2 normal_locrc tumor_locrc
        3  geneComp_00113199    TPM2      TPM2 normal_locrc tumor_locrc
        4  geneComp_00091701   FSIP1     FSIP1 normal_locrc tumor_locrc
        5  geneComp_00102515 OSBPL1A   OSBPL1A normal_locrc tumor_locrc
        6  geneComp_00098800 MAP3K20   MAP3K20 normal_locrc tumor_locrc
        7  geneComp_00061664    CD44      CD44 normal_locrc tumor_locrc
        8  geneComp_00063393  CXCL12    CXCL12 normal_locrc tumor_locrc
        9  geneComp_00101397     NLN       NLN normal_locrc tumor_locrc
        10 geneComp_00093642   HNF4A     HNF4A normal_locrc tumor_locrc
          gene_switch_q_value Rank
        1         0.0001116680    1
        2         0.0001544585    2
        3         0.0001544585    3
        4         0.0001622092    4
        5         0.0002382206    5
        6         0.0003502090    6
        7         0.0004922797    7
        8         0.0006191435    8
        9         0.0006191435    9
        10        0.0009308128   10

          |                                                                            
          |                                                                      |   0%
          |                                                                            
          |=                                                                     |   1%
          |                                                                            
          |=                                                                     |   2%
          |                                                                            
          |==                                                                    |   2%
          |                                                                            
          |==                                                                    |   3%
          |                                                                            
          |===                                                                   |   4%
          |                                                                            
          |===                                                                   |   5%
          |                                                                            
          |====                                                                  |   5%
          |                                                                            
          |====                                                                  |   6%
          |                                                                            
          |=====                                                                 |   7%
          |                                                                            
          |=====                                                                 |   8%
          |                                                                            
          |======                                                                |   9%
          |                                                                            
          |=======                                                               |   9%
          |                                                                            
          |=======                                                               |  10%
          |                                                                            
          |========                                                              |  11%
          |                                                                            
          |========                                                              |  12%
          |                                                                            
          |=========                                                             |  12%
          |                                                                            
          |=========                                                             |  13%
          |                                                                            
          |==========                                                            |  14%
          |                                                                            
          |==========                                                            |  15%
          |                                                                            
          |===========                                                           |  16%
          |                                                                            
          |============                                                          |  17%
          |                                                                            
          |=============                                                         |  18%
          |                                                                            
          |=============                                                         |  19%
          |                                                                            
          |==============                                                        |  20%
          |                                                                            
          |===============                                                       |  21%
          |                                                                            
          |===============                                                       |  22%
          |                                                                            
          |================                                                      |  23%
          |                                                                            
          |=================                                                     |  24%
          |                                                                            
          |==================                                                    |  25%
          |                                                                            
          |==================                                                    |  26%
          |                                                                            
          |===================                                                   |  27%
          |                                                                            
          |====================                                                  |  28%
          |                                                                            
          |====================                                                  |  29%
          |                                                                            
          |=====================                                                 |  30%
          |                                                                            
          |======================                                                |  31%
          |                                                                            
          |======================                                                |  32%
          |                                                                            
          |=======================                                               |  33%
          |                                                                            
          |========================                                              |  34%
          |                                                                            
          |=========================                                             |  35%
          |                                                                            
          |=========================                                             |  36%
          |                                                                            
          |==========================                                            |  37%
          |                                                                            
          |==========================                                            |  38%
          |                                                                            
          |===========================                                           |  38%
          |                                                                            
          |===========================                                           |  39%
          |                                                                            
          |============================                                          |  40%
          |                                                                            
          |============================                                          |  41%
          |                                                                            
          |=============================                                         |  41%
          |                                                                            
          |==============================                                        |  42%
          |                                                                            
          |==============================                                        |  43%
          |                                                                            
          |===============================                                       |  44%
          |                                                                            
          |===============================                                       |  45%
          |                                                                            
          |================================                                      |  45%
          |                                                                            
          |================================                                      |  46%
          |                                                                            
          |=================================                                     |  47%
          |                                                                            
          |=================================                                     |  48%
          |                                                                            
          |==================================                                    |  48%
          |                                                                            
          |==================================                                    |  49%
          |                                                                            
          |===================================                                   |  50%
          |                                                                            
          |====================================                                  |  51%
          |                                                                            
          |====================================                                  |  52%
          |                                                                            
          |=====================================                                 |  52%
          |                                                                            
          |=====================================                                 |  53%
          |                                                                            
          |======================================                                |  54%
          |                                                                            
          |======================================                                |  55%
          |                                                                            
          |=======================================                               |  55%
          |                                                                            
          |=======================================                               |  56%
          |                                                                            
          |========================================                              |  57%
          |                                                                            
          |========================================                              |  58%
          |                                                                            
          |=========================================                             |  59%
          |                                                                            
          |==========================================                            |  59%
          |                                                                            
          |==========================================                            |  60%
          |                                                                            
          |===========================================                           |  61%
          |                                                                            
          |===========================================                           |  62%
          |                                                                            
          |============================================                          |  62%
          |                                                                            
          |============================================                          |  63%
          |                                                                            
          |=============================================                         |  64%
          |                                                                            
          |=============================================                         |  65%
          |                                                                            
          |==============================================                        |  66%
          |                                                                            
          |===============================================                       |  67%
          |                                                                            
          |================================================                      |  68%
          |                                                                            
          |================================================                      |  69%
          |                                                                            
          |=================================================                     |  70%
          |                                                                            
          |==================================================                    |  71%
          |                                                                            
          |==================================================                    |  72%
          |                                                                            
          |===================================================                   |  73%
          |                                                                            
          |====================================================                  |  74%
          |                                                                            
          |====================================================                  |  75%
          |                                                                            
          |=====================================================                 |  76%
          |                                                                            
          |======================================================                |  77%
          |                                                                            
          |=======================================================               |  78%
          |                                                                            
          |=======================================================               |  79%
          |                                                                            
          |========================================================              |  80%
          |                                                                            
          |=========================================================             |  81%
          |                                                                            
          |=========================================================             |  82%
          |                                                                            
          |==========================================================            |  83%
          |                                                                            
          |===========================================================           |  84%
          |                                                                            
          |============================================================          |  85%
          |                                                                            
          |============================================================          |  86%
          |                                                                            
          |=============================================================         |  87%
          |                                                                            
          |=============================================================         |  88%
          |                                                                            
          |==============================================================        |  88%
          |                                                                            
          |==============================================================        |  89%
          |                                                                            
          |===============================================================       |  90%
          |                                                                            
          |===============================================================       |  91%
          |                                                                            
          |================================================================      |  91%
          |                                                                            
          |=================================================================     |  92%
          |                                                                            
          |=================================================================     |  93%
          |                                                                            
          |==================================================================    |  94%
          |                                                                            
          |==================================================================    |  95%
          |                                                                            
          |===================================================================   |  95%
          |                                                                            
          |===================================================================   |  96%
          |                                                                            
          |====================================================================  |  97%
          |                                                                            
          |====================================================================  |  98%
          |                                                                            
          |===================================================================== |  98%
          |                                                                            
          |===================================================================== |  99%
          |                                                                            
          |======================================================================| 100%
                          Comparison nrIsoforms nrSwitches nrGenes
        1 normal_eocrc vs tumor_eocrc         14         10      10
        2 normal_locrc vs tumor_locrc        133        122     104
        3                    Combined        140        128     109
                          Comparison nrIsoforms nrSwitches nrGenes
        1 normal_eocrc vs tumor_eocrc         14         10      10
        2 normal_locrc vs tumor_locrc        132        122     103
        3                    Combined        140        128     109
        ```

- [EOCRC and LOCRC samples](integrative-analysis-dge-dtu-rss-crc/reports/dtu-analysis/dtu-read-rds-isoforms_42_44.html)

### **5. RNA Secondary Structure Analysis (RSS)**
- [Common EOCRC and LOCRC isoforms](integrative-analysis-dge-dtu-rss-crc/reports/secondary-rna-structure-analysis/motifs_plots.html)

---
## Contributing
This is a thesis repository, but suggestions for improvements are welcome via [GitHub issues](https://github.com/sblaizerwize/master-bioinformatics/issues).