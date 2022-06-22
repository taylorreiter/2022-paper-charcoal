---
title: 'Charcoal: filtering contamination in metagenome-assembled genome bins and other genomes'
keywords:
- contamination
- genome
- k-mer
lang: en-US
date-meta: '2022-06-22'
author-meta:
- Taylor E. Reiter
- N. Tessa Pierce-Ward
- Luiz Irber
- Erich M. Schwarz
- C. Titus Brown
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Charcoal: filtering contamination in metagenome-assembled genome bins and other genomes" />
  <meta name="citation_title" content="Charcoal: filtering contamination in metagenome-assembled genome bins and other genomes" />
  <meta property="og:title" content="Charcoal: filtering contamination in metagenome-assembled genome bins and other genomes" />
  <meta property="twitter:title" content="Charcoal: filtering contamination in metagenome-assembled genome bins and other genomes" />
  <meta name="dc.date" content="2022-06-22" />
  <meta name="citation_publication_date" content="2022-06-22" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Taylor E. Reiter" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0002-7388-421X" />
  <meta name="twitter:creator" content="@ReiterTaylor" />
  <meta name="citation_author" content="N. Tessa Pierce-Ward" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0002-2942-5331" />
  <meta name="twitter:creator" content="@saltyscientist" />
  <meta name="citation_author" content="Luiz Irber" />
  <meta name="citation_author_institution" content="Graduate Group in Computer Science, UC Davis" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0003-4371-9659" />
  <meta name="twitter:creator" content="@luizirber" />
  <meta name="citation_author" content="Erich M. Schwarz" />
  <meta name="citation_author_institution" content="Department of Molecular Biology and Genetics, Cornell University" />
  <meta name="citation_author_orcid" content="0000-0003-3151-4381" />
  <meta name="citation_author" content="C. Titus Brown" />
  <meta name="citation_author_institution" content="Department of Population Health and Reproduction, University of California, Davis" />
  <meta name="citation_author_orcid" content="0000-0001-6001-2677" />
  <link rel="canonical" href="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta property="og:url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta property="twitter:url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta name="citation_fulltext_html_url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta name="citation_pdf_url" content="https://taylorreiter.github.io/2022-paper-charcoal/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://taylorreiter.github.io/2022-paper-charcoal/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://taylorreiter.github.io/2022-paper-charcoal/v/e8621d1a084e76f8b148e969e9fe98cdd730b2c8/" />
  <meta name="manubot_html_url_versioned" content="https://taylorreiter.github.io/2022-paper-charcoal/v/e8621d1a084e76f8b148e969e9fe98cdd730b2c8/" />
  <meta name="manubot_pdf_url_versioned" content="https://taylorreiter.github.io/2022-paper-charcoal/v/e8621d1a084e76f8b148e969e9fe98cdd730b2c8/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://taylorreiter.github.io/2022-paper-charcoal/v/e8621d1a084e76f8b148e969e9fe98cdd730b2c8/))
was automatically generated
from [taylorreiter/2022-paper-charcoal@e8621d1](https://github.com/taylorreiter/2022-paper-charcoal/tree/e8621d1a084e76f8b148e969e9fe98cdd730b2c8)
on June 22, 2022.
</em></small>

## Authors



+ **Taylor E. Reiter**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-7388-421X](https://orcid.org/0000-0002-7388-421X)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [taylorreiter](https://github.com/taylorreiter)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [ReiterTaylor](https://twitter.com/ReiterTaylor)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
  </small>

+ **N. Tessa Pierce-Ward**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-2942-5331](https://orcid.org/0000-0002-2942-5331)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [bluegenes](https://github.com/bluegenes)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [saltyscientist](https://twitter.com/saltyscientist)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
     · Funded by NSF 1711984
  </small>

+ **Luiz Irber**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-4371-9659](https://orcid.org/0000-0003-4371-9659)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [luizirber](https://github.com/luizirber)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [luizirber](https://twitter.com/luizirber)<br>
  <small>
     Graduate Group in Computer Science, UC Davis; Department of Population Health and Reproduction, University of California, Davis
  </small>

+ **Erich M. Schwarz**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-3151-4381](https://orcid.org/0000-0003-3151-4381)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [SchwarzEM](https://github.com/SchwarzEM)<br>
  <small>
     Department of Molecular Biology and Genetics, Cornell University
  </small>

+ **C. Titus Brown**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-6001-2677](https://orcid.org/0000-0001-6001-2677)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [ctb](https://github.com/ctb)<br>
  <small>
     Department of Population Health and Reproduction, University of California, Davis
  </small>



## Abstract {.page_break_before}

Metagenomics has expanded our knowledge of microbial diversity, but contaminant sequences are frequently accidentally included in metagenome-assembled genomes. 
Genome contamination is often estimated by the presence of marker genes that are biased against detecting contaminants lacking these sequences. 
Further, most contamination detection tools do not remove contamination. 
We present charcoal, a tool that rapidly identifies and removes contamination in metagenome-assembled genomes using k-mer based methods.
K-mers are nucleotide sequences of length k. 
Sufficiently long k-mers are usually specific to a taxonomic lineage. 
Taking advantage of this property of k-mers, charcoal identifies majority and minority lineages for each contiguous sequence in a genome and removes contiguous sequences belonging to minority lineages when those lineages occur below a taxonomic threshold (by default, order). 
Applying charcoal to the Genome Taxonomy Database rs207, we found approximately XX% of genomes in GTDB were contaminated, with contamination broadly distributed across species and occurring in representative and RefSeq genomes. 
Genomes with longer contiguous sequences were less likely to be contaminated.
Our results show concordance with CheckM on detecting the presence of contamination in a genome. 
Charcoal is a snakemake workflow developed around the tool sourmash. 
It is available at github.com/dib-lab/charcoal, and is pip installable.

# Introduction

Metagenomic sequencing has expanded our knowledge of microbial communities and their diversity [@doi:10.1038/nmicrobiol.2016.48; @doi:10.1038/s41587-020-0718-6; @doi:10.1038/s41564-021-00928-6].
*De novo* metagenome analysis has generated thousands of draft genomes, termed metagenome-assembled genomes (MAGs), from organisms from diverse environments [@doi:10.1038/nature02340; @doi:10.1016/j.cell.2019.01.001; @doi:10.1038/s41587-020-0603-3; @doi:10.1038/s41587-020-0718-6].
Recently, large-scale re-analysis efforts have led to a rapid expansion in draft genomes in public repositories like the European Nucleotide Archive [@doi:10.1038/s41587-020-0603-3] and the Joint Genome Institute IMG/M [@doi:10.1038/s41587-020-0718-6].
Increased observation of draft genomes across the tree of life better enables researchers to contextualize new sequencing data and the roles that microorganisms play in diverse metabolic processes [@doi:10.1038/s41564-017-0012-7; @doi:10.1093/nar/gkz1002].

MAG inference relies on assembly and binning of metagenomic sequencing data.
Assembly produces long contiguous sequences by identifying overlaps between short sequencing reads, while binning groups assembled sequences into MAGs using read coverage and tetramernucleotide frequency.
Both processes are subject to biases that can reduce the completeness of or increase the contamination in a MAG: low sequencing coverage or high genomic variation causes short read assemblers to break contiguous sequences into shorter pieces (CITE), which decreases the signal for and accuracy of binning (CITE).
Commonly, the completeness and purity of MAGs is estimated through the presence and sequence composition of single-copy marker genes [@doi:10.1101/gr.186072.114] [@doi:10.1093/bioinformatics/btv351], with MAGs that reach >90% completeness and <5% contamination considered high quality [@doi:10.1101/gr.186072.114].
Single-copy marker genes are sets of genes that are present once in a genome of almost all members of a taxonomic group [@doi:10.1101/gr.186072.114; @doi:10.7717/peerj.243].
Using these genes to estimate contamination leads to two important biases.
First, given the assumption that marker genes are universally present in genomes, if a marker gene resides on a contaminant sequence but no other sequence for that marker gene is present in the genome, it will not be detected as contamination [@doi:10.1101/gr.186072.114; @doi:10.3389/fmicb.2017.02264].
When a MAG is substantially complete, this may lead to a small underestimation in contamination (~3% [@doi:10.1101/gr.186072.114]), but as completeness decreases, contamination may be substantially underestimated [@doi:10.3389/fmicb.2017.02264].
Second, contiguous sequences which do not contain marker sequences are not included among contamination estimates [@doi:10.1101/gr.186072.114] (note checkm called out plasmids and phages for this bias specifically).

Given these biases, methods that do not rely solely on marker genes may be better suited for contamination estimation.
Many tools have recently been developed that rely on different strategies for detecting contamination [@doi:10.1186/s13059-022-02619-9].
GUNC expands beyond marker genes and uses the full complement of genes in a genome to identify contiguous sequences that fall outside of the predicted lineage [@doi:10.1186/s13059-021-02393-0].
It estimates the distribution of taxonomic assignments within and across contiguous sequences to identify contaminants even among sequences that are poorly taxonomically labelled [@doi:10.1186/s13059-021-02393-0].
Conterminator detects cross-kingdom contamination using all-vs-all alignment and is geared toward contamination detection in large collections of genomes (e.g. databases) [@doi:10.1186/s13059-020-02023-1].
Sequences are considered contaminants when at least 100 nucleotides and no more than 20 kb share a sequence identity of at least 90% in genomes that originate from different kingdoms [@doi:10.1186/s13059-020-02023-1].
In addition, conterminator finds contamination in protein sequences by identifying protein clusters that contain sequences from cross-kingdom members [@doi:10.1186/s13059-020-02023-1].
 
Removing contamination is a separate problem from estimating its extent.
Tools like RefineM [@doi:10.1038/s41564-017-0012-7], MAGPpurify [@doi:10.1038/s41586-019-1058-x], and BlobTools [@doi:10.12688/f1000research.12232.1] rely on a combination of GC content, tetramernucleotide frequency, read coverage, phylogenetic or clade markers, conspecific sequences, and known contaminants to flag contaminant contiguous sequences for removal.
The inclusion of read coverage profiles necessitates the use of the original sequencing reads to produce coverage profiles in BAM format for the genomes.
Given that sequencing data and BAM files are usually orders of magnitude larger than genome sequences, this requirement limits the utility of such approaches, especially for large-scale genome databases. 
Tools like GUNC are poised for contamination removal without relying on read coverage profiles, but as of yet such approaches are unimplemented [@doi:10.1186/s13059-021-02393-0].

Long k-mers capture relatedness between organisms, where a k=31 captures species-level similarity [@doi:10.1128/mSystems.00020-16].
K-mers offer an alternative metric to identify contamination, especially in sequences lacking marker genes. 
Here we describe Charcoal, an automated method for filtering contaminant contiguous sequences from MAGs. 
We show...
We show...
We envisage that charcoal will complement marker gene-based approaches for contamination estimation, removing problematic sequences before they are further analyzed or propagated in public databases. 


# Methods

## Overview

![**Summary of steps used to decontaminate genomes with charcoal.**
In the first stage of the pipeline, contamination detection occurs by comparing the taxonomic assignment of each contig in a genome against all other contigs. 
Contigs with inconsistent taxonomy are flagged as contaminants, by default if they differ at the order level or above.
The results of this step are summarized to report the contaminating genomes, the number of contaminant contigs and base pairs at each level of taxonomy, and other metrics like the fraction of the genome that was identifiable and the fraction that was assignable to the majority lineage.
The outputs of the first stage of the pipeline can then be used in any of three additional reporting steps.
First, contamination can be verified by aligning the contaminant contigs against their identified matching reference genome, and the mappings can be visualized.
Second, an html document can be produced that gives an overview of the contamination in each genome.
Lastly, the contaminant contigs can be separated out from the non-contaminant contigs, writing two separate FASTA files per genome.
](images/charcoal_overview.png){#fig:overview}

Charcoal provides an automated method to detect, visualize, and remove bacterial and archaeal contamination in genomes (**Figure @fig:overview**).
To identify contamination, charcoal first creates a FracMinHash sketch for each contiguous sequence ("contig") in an input genome. 
Charcoal then identifies all genomes in a database ("reference genomes") that share sequence overlap with the input genome using sourmash `prefetch`.
Subsequent operations subset the original database to include only the genomes identified by `prefetch`, reducing search volumes. 
Using these matches, charcoal uses sourmash `gather` to identify the minimum set of genomes that cover (or contain) the k-mers in each contig [@doi:10.1101/2022.01.11.475838].
Charcoal then determines the taxonomic lineage of each contig using a lineage spreadsheet that records the taxonomy of each reference genome in the database; the taxonomic assignment occurs at the lowest common ancestor of all taxonomic assignments given to a contig.
If there is an exact match between the input genome and a genome in the database, this match is removed to allow decontamination to continue.

Charcoal compares the taxonomic lineage of each contig against the lineage of the input genome. 
If the contig has a different lineage before or at the configured taxonomic rank (order by default) than that of the majority lineage, the contig is considered a contaminant. 
For each contig, charcoal reports the fraction of identified hashes (total and to each major and minor lineage), an estimate of contaminated base pairs (at each taxonomic rank match), as well as the fraction of contigs and base pairs unable to be identified.

The input genome lineage can be user-provided, or it can be determined by charcoal via majority vote of all lineages assigned to all contigs. 
If the lineage is determined by charcoal, by default a minimum 10% of the input genome must have been assigned a taxonomic lineage, and 20% of assigned sequences must match to the majority lineage.
If these specifications are not met, charcoal will not decontaminate the input genome unless the user specifies a lineage. 
The user can optionally specify a lineage (e.g. d__Eukaryota), and charcoal will remove contigs that have a lineage different from the user-specified one. 
This allows charcoal to remove contigs from an input genome when some contigs from that genome occur in the database and when the input genome is not related to anything in a database. 
Charcoal reports whether the provided lineage agrees with k-mer classification at or above the genus level.

After the initial stage of contaminant detection, charcoal can perform additional tasks to verify, summarize, or remove the contaminant sequences. 
Contaminant verification downloads the reference genome sequence for any genome that was detected among the input genome contigs and aligns the contigs against those genomes using mashmap [@doi:10.1093/bioinformatics/bty597]. 
Contaminant removal separates "clean" from "dirty" contigs and outputs each set into a FASTA file. 
Importantly, charcoal will not remove a contig if it is unidentifiable, whether it is too short to be sketched or does not contain sequences in the reference database. 
While these contigs could still be contaminants, charcoal assumes contigs are clean for which it has no information. 
Therefore, charcoal will fail to detect contamination for very short contigs which contain no selected k-mers, as well as contigs with novel DNA content. 
Lastly, charcoal has a report feature that summarizes and visualizes the taxonomic lineages detected in each input genome as well as the alignments between the input genome and reference genomes.

Sourmash `prefetch` is the most compute intensive step in the decontamination process. 
When using the GTDB rs207 representative database, this step does not exceed 8GB of RAM.

+ statement that charcoal is database dependent (probably can go in last paragraph with RAM/CPU considerations)

## Availability and dependencies

Charcoal is written in python3 and can be installed via pip as charcoal-bio.
The core algorithms (contaminant detection and removal) depend on sourmash and snakemake. 
Contaminant verification depends on lxml and mashmap [@doi:10.1093/bioinformatics/bty597].
Reporting depends on mummer, papermill, notebook, and plotly [@doi:10.1002/0471250953.bi1003s00].
The source code is available at github.com/dib-lab/charcoal.
ZENODO DOI.

## Datasets and benchmarking

We first use charcoal to decontaminate GTDB rs207.

# Results

## Charcoal detected and removed contamination from roughly one quarter of GTDB genomes

![**Charcoal identified contamination in approximately one quarter of GTDB rs207 genomes, distributed generally across different types of genomes.**
**A)** Bar plot depicting the number of genomes in GTDB contaminated at the order level.
**B)** Bar plot separating genomes in GTDB by their inclusion in NCBI's RefSeq. Both GenBank and RefSeq genomes are contaminated.
**C)** Bar plot separating representative genomes in GTDB from non-representative genomes. While some representative genomes are contaminated, non-representative genomes are more likely to be contaminated.
**D)** Violin plots depicting the mean contig length within genomes in GTDB, separated by contamination profile. Genomes with longer contigs are less likely to be contaminated. On average, the contigs in contaminated genomes were 380,504 base pairs shorter than contigs in non-contaminated genomes.
**E)** Bar plot that separates genomes by NCBI category which specifies where source material was derived from.
**F)** Bar plot depicting the number of genomes in each order, colored by contamination status. Genomes are grouped by taxonomic lineage up to the order level.
](images/charcoal_gtdb.png){#fig:charcoal_gtdb}

Using charcoal to detect and remove contamination, approximately 26% of GTDB rs207 genomes were contaminated at the order level or above (**Figure @fig:charcoal_gtdb A**).
Contamination was distributed across GenBank and RefSeq genomes (**Figure @fig:charcoal_gtdb B**), GTDB representative and non-representative genomes (**Figure @fig:charcoal_gtdb C**), isolate, single cell, and metagenome-derived genomes (**Figure @fig:charcoal_gtdb E**), and taxonomic orders (**Figure @fig:charcoal_gtdb F**).
However, contamination was more likely to be identified in genomes with shorter contigs (**Figure @fig:charcoal_gtdb D**) and in non-representative GTDB genomes (**Figure @fig:charcoal_gtdb C**). 

+ TODO: run prodigal/bakta on dirty contigs, comment on number of genes/average functional potential added to contaminated genomes by contamination.

## Charcoal and CheckM identify the same set of not contaminated genomes

Charcoal is more conservative than CheckM contamination estimation at the order level.
whereas 80.2% of genomes are estimated to have some contamination using CheckM.
    + Both tools agree on the majority of genomes with no contamination

At the family level, charcoal identified contamination in XX% of genomes, suggesting that adjusting taxonomy may improve agreement with checkm.

Do plot -- at what % checkm contam best overlaps with order level charcoal?

+ run checkm on clean

## Databases

+ gtdb rs207 reps vs gtdb rs202 reps
+ gtdb rs202 reps vs gtdb rs202 full (replace evnetually with rs207)
    + short contigs missed
    + ram considerations
    + future development: species-level database

**old results outline:**

+ charcoal vs. checkm
  + charcoal vs. checkm: mgnify, tara
  + prokka on charcoal dirty
+ charcoal vs. refineM and magpurify
+ verification of contamination/contam case studies
  + case studies
  + user-provided lineages
  + cDBG/spacegraphcats?
  + user-specified lineages


# Discussion

## Benefits and drawbacks of charcoal. 

Commonly, the completeness and contamination of MAGs is estimated through the presence and sequence composition of single-copy marker genes [@doi:10.1101/gr.186072.114; @doi:10.1093/bioinformatics/btv351], with MAGs that reach >90% completeness and <5% contamination considered high quality [@doi:10.1101/gr.186072.114]. 
Using these genes to estimate contamination leads to two important biases. 
First, given the assumption that marker genes are universally present in genomes, if a marker gene resides on a contaminant sequence but no other sequence for that marker gene is present in the genome, it will not be detected as contamination [@doi:10.1101/gr.186072.114; @doi:10.3389/fmicb.2017.02264]. 
When a MAG is substantially complete, this may lead to a small underestimation in contamination (~3% [@doi:10.1101/gr.186072.114]), but as completeness decreases, contamination may be substantially underestimated [@doi:10.3389/fmicb.2017.02264]. 
Second, contiguous sequences which do not contain marker sequences are not included among contamination estimates [@doi:10.1101/gr.186072.114]. 
Charcoal avoids these pitfalls by using k-mers, which are sampled evenly across the genome [@doi:10.1101/2022.01.11.475838]. 
We envisage charcoal acting as a complementary analysis tool to CheckM.
  
While charcoal avoids the above biases, it is itself biased against detecting contamination in very short contigs. 
By default, a minimum of three k-mers must be taxonomically annotated on a contig for a contig to be removed; because contigs are first sketched, many short contigs will not contain three k-mers.

## Future work

+ strain heterogeneity estimation or strain insertion in newick tree using prefetch & clean results
+ completeness estimation, potentially via comparison to conspecifics via genome size
+ database with eukaryotic sequences
+ estimation via protein sequences for divergent organisms not well represented in databases

## Notes

+ fastani is an accepted way to do average nucleotide identity calculate, and it relies on k-mers.
+ from checkm paper:
> Bias in genome quality estimates: Quality estimates based on individual marker genes or collocated marker sets exhibit a bias resulting in completeness being overestimated and contamination being underestimated. This bias is the result of marker genes residing on foreign DNA that are otherwise absent in a genome being mistakenly interpreted as an indication of increased completeness as opposed to contamination. 
+ we don't deal with strain heterogeneity, as this occurs below the species-level aggregation in the LCA


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
