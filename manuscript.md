---
title: Manuscript Title
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-06-15'
author-meta:
- John Doe
- Jane Roe
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Manuscript Title" />
  <meta name="citation_title" content="Manuscript Title" />
  <meta property="og:title" content="Manuscript Title" />
  <meta property="twitter:title" content="Manuscript Title" />
  <meta name="dc.date" content="2022-06-15" />
  <meta name="citation_publication_date" content="2022-06-15" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="John Doe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="twitter:creator" content="@johndoe" />
  <meta name="citation_author" content="Jane Roe" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <link rel="canonical" href="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta property="og:url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta property="twitter:url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta name="citation_fulltext_html_url" content="https://taylorreiter.github.io/2022-paper-charcoal/" />
  <meta name="citation_pdf_url" content="https://taylorreiter.github.io/2022-paper-charcoal/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://taylorreiter.github.io/2022-paper-charcoal/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://taylorreiter.github.io/2022-paper-charcoal/v/91342b17509f5475b66a501b70ffa1f80da1abfc/" />
  <meta name="manubot_html_url_versioned" content="https://taylorreiter.github.io/2022-paper-charcoal/v/91342b17509f5475b66a501b70ffa1f80da1abfc/" />
  <meta name="manubot_pdf_url_versioned" content="https://taylorreiter.github.io/2022-paper-charcoal/v/91342b17509f5475b66a501b70ffa1f80da1abfc/manuscript.pdf" />
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
([permalink](https://taylorreiter.github.io/2022-paper-charcoal/v/91342b17509f5475b66a501b70ffa1f80da1abfc/))
was automatically generated
from [taylorreiter/2022-paper-charcoal@91342b1](https://github.com/taylorreiter/2022-paper-charcoal/tree/91342b17509f5475b66a501b70ffa1f80da1abfc)
on June 15, 2022.
</em></small>

## Authors



+ **John Doe**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [johndoe](https://github.com/johndoe)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [johndoe](https://twitter.com/johndoe)<br>
  <small>
     Department of Something, University of Whatever
     · Funded by Grant XXXXXXXX
  </small>

+ **Jane Roe**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [janeroe](https://github.com/janeroe)<br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
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

This manuscript is a template (aka "rootstock") for [Manubot](https://manubot.org/ "Manubot"), a tool for writing scholarly manuscripts.
Use this template as a starting point for your manuscript.

The rest of this document is a full list of formatting elements/features supported by Manubot.
Compare the input (`.md` files in the `/content` directory) to the output you see below.

## Basic formatting

**Bold** __text__

[Semi-bold text]{.semibold}

[Centered text]{.center}

[Right-aligned text]{.right}

*Italic* _text_

Combined *italics and __bold__*

~~Strikethrough~~

1. Ordered list item
2. Ordered list item
    a. Sub-item
    b. Sub-item
        i. Sub-sub-item
3. Ordered list item
    a. Sub-item

- List item
- List item
- List item

subscript: H~2~O is a liquid

superscript: 2^10^ is 1024.

[unicode superscripts](https://www.google.com/search?q=superscript+generator)⁰¹²³⁴⁵⁶⁷⁸⁹

[unicode subscripts](https://www.google.com/search?q=superscript+generator)₀₁₂₃₄₅₆₇₈₉

A long paragraph of text.
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Putting each sentence on its own line has numerous benefits with regard to [editing](https://asciidoctor.org/docs/asciidoc-recommended-practices/#one-sentence-per-line) and [version control](https://rhodesmill.org/brandon/2012/one-sentence-per-line/).

Line break without starting a new paragraph by putting  
two spaces at end of line.

## Document organization

Document section headings:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### A heading centered on its own printed page{.center .page_center}

<!-- an arbitrary comment. visible in input, but not visible in output. -->

Horizontal rule:

---

`Heading 1`'s are recommended to be reserved for the title of the manuscript.

`Heading 2`'s are recommended for broad sections such as *Abstract*, *Methods*, *Conclusion*, etc.

`Heading 3`'s and `Heading 4`'s are recommended for sub-sections.

## Links

Bare URL link: <https://manubot.org>

[Long link with lots of words and stuff and junk and bleep and blah and stuff and other stuff and more stuff yeah](https://manubot.org)

[Link with text](https://manubot.org)

[Link with hover text](https://manubot.org "Manubot Homepage")

[Link by reference][manubot homepage]

[Manubot Homepage]: https://manubot.org

## Citations

Citation by DOI [@doi:10.7554/eLife.32822].

Citation by PubMed Central ID [@pmc:PMC6103790].

Citation by PubMed ID [@pubmed:30718888].

Citation by Wikidata ID [@wikidata:Q56458321].

Citation by ISBN [@isbn:9780262517638].

Citation by URL [@{https://greenelab.github.io/meta-review/}].

Citation by alias [@deep-review].

Multiple citations can be put inside the same set of brackets [@doi:10.7554/eLife.32822; @deep-review; @isbn:9780262517638].
Manubot plugins provide easier, more convenient visualization of and navigation between citations [@doi:10.1371/journal.pcbi.1007128; @pubmed:30718888; @pmc:PMC6103790; @deep-review].

Citation tags (i.e. aliases) can be defined in their own paragraphs using Markdown's reference link syntax:

[@deep-review]: doi:10.1098/rsif.2017.0387

## Referencing figures, tables, equations

Figure @fig:square-image

Figure @fig:wide-image

Figure @fig:tall-image

Figure @fig:vector-image

Table @tbl:bowling-scores

Equation @eq:regular-equation

Equation @eq:long-equation

## Quotes and code

> Quoted text

> Quoted block of text
>
> Two roads diverged in a wood, and I—  
> I took the one less traveled by,  
> And that has made all the difference.

Code `in the middle` of normal text, aka `inline code`.

Code block with Python syntax highlighting:

```python
from manubot.cite.doi import expand_short_doi

def test_expand_short_doi():
    doi = expand_short_doi("10/c3bp")
    # a string too long to fit within page:
    assert doi == "10.25313/2524-2695-2018-3-vliyanie-enhansera-copia-i-insulyatora-gypsy-na-sintez-ernk-modifikatsii-hromatina-i-svyazyvanie-insulyatornyh-belkov-vtransfetsirovannyh-geneticheskih-konstruktsiyah"
```

Code block with no syntax highlighting:

```
Exporting HTML manuscript
Exporting DOCX manuscript
Exporting PDF manuscript
```

## Figures

![
**A square image at actual size and with a bottom caption.**
Loaded from the latest version of image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/square.png "Square image"){#fig:square-image}

![
**An image too wide to fit within page at full size.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/wide.png "Wide image"){#fig:wide-image}

![
**A tall image with a specified height.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/tall.png "Tall image"){#fig:tall-image height=3in}

![
**A vector `.svg` image loaded from GitHub.**
The parameter `sanitize=true` is necessary to properly load SVGs hosted via GitHub URLs.
White background specified to serve as a backdrop for transparent sections of the image.
](https://raw.githubusercontent.com/manubot/resources/main/test/vector.svg?sanitize=true "Vector image"){#fig:vector-image height=2.5in .white}

## Tables

| *Bowling Scores* | Jane          | John          | Alice         | Bob           |
|:-----------------|:-------------:|:-------------:|:-------------:|:-------------:|
| Game 1 | 150 | 187 | 210 | 105 |
| Game 2 |  98 | 202 | 197 | 102 |
| Game 3 | 123 | 180 | 238 | 134 |

Table: A table with a top caption and specified relative column widths.
{#tbl:bowling-scores}

|         | Digits 1-33                        | Digits 34-66                      | Digits 67-99                      | Ref.                                                        |
|:--------|:-----------------------------------|:----------------------------------|:----------------------------------|:------------------------------------------------------------|
| pi      | 3.14159265358979323846264338327950 | 288419716939937510582097494459230 | 781640628620899862803482534211706 | [`piday.org`](https://www.piday.org/million/)               |
| e       | 2.71828182845904523536028747135266 | 249775724709369995957496696762772 | 407663035354759457138217852516642 | [`nasa.gov`](https://apod.nasa.gov/htmltest/gifcity/e.2mil) |

Table: A table too wide to fit within page.
{#tbl:constant-digits}

|          | **Colors** <!-- $colspan="2" --> |                      |
|:--------:|:--------------------------------:|:--------------------:|
| **Size** | **Text Color**                   | **Background Color** |
| big      | blue                             | orange               |
| small    | black                            | white                |

Table: A table with merged cells using the `attributes` plugin.
{#tbl: merged-cells}

## Equations

A LaTeX equation:

$$\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}$$ {#eq:regular-equation}

An equation too long to fit within page:

$$x = a + b + c + d + e + f + g + h + i + j + k + l + m + n + o + p + q + r + s + t + u + v + w + x + y + z + 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9$$ {#eq:long-equation}

## Special

<i class="fas fa-exclamation-triangle"></i> [WARNING]{.semibold} _The following features are only supported and intended for `.html` and `.pdf` exports._
_Journals are not likely to support them, and they may not display correctly when converted to other formats such as `.docx`._

[Link styled as a button](https://manubot.org "Manubot Homepage"){.button}

Adding arbitrary HTML attributes to an element using Pandoc's attribute syntax:

::: {#some_id_1 .some_class style="background: #ad1457; color: white; margin-left: 40px;" title="a paragraph of text" data-color="white" disabled="true"}
Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
:::

Adding arbitrary HTML attributes to an element with the Manubot `attributes` plugin (more flexible than Pandoc's method in terms of which elements you can add attributes to):

Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
<!-- $id="element_id" class="some_class" $style="color: #ad1457; margin-left: 40px;" $disabled="true" $title="a paragraph of text" $data-color="red" -->

Available background colors for text, images, code, banners, etc:  

`white`{.white}
`lightgrey`{.lightgrey}
`grey`{.grey}
`darkgrey`{.darkgrey}
`black`{.black}
`lightred`{.lightred}
`lightyellow`{.lightyellow}
`lightgreen`{.lightgreen}
`lightblue`{.lightblue}
`lightpurple`{.lightpurple}
`red`{.red}
`orange`{.orange}
`yellow`{.yellow}
`green`{.green}
`blue`{.blue}
`purple`{.purple}

Using the [Font Awesome](https://fontawesome.com/) icon set:

<!-- include the Font Awesome library, per: https://fontawesome.com/start -->
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css">

<i class="fas fa-check"></i> <i class="fas fa-question"></i> <i class="fas fa-star"></i> <i class="fas fa-bell"></i> <i class="fas fa-times-circle"></i> <i class="fas fa-ellipsis-h"></i>

[
<i class="fas fa-scroll fa-lg"></i> **Light Grey Banner**<br>
useful for *general information* - [manubot.org](https://manubot.org/)
]{.banner .lightgrey}

[
<i class="fas fa-info-circle fa-lg"></i> **Blue Banner**<br>
useful for *important information* - [manubot.org](https://manubot.org/)
]{.banner .lightblue}

[
<i class="fas fa-ban fa-lg"></i> **Light Red Banner**<br>
useful for *warnings* - [manubot.org](https://manubot.org/)
]{.banner .lightred}


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
The results of this step are summarized to report the contaminating genomes, the number of contaminant contigs and basepairs at each level of taxonomy, and other metrics like the fraction of the genome that was identifiable and the fraction that was assignable to the majority lineage.
The outputs of the first stage of the pipeline can then be used in any of three additional reporting steps.
First, contamination can be verified by aligning the contaminant contigs against their identified matching reference genome, and the mappings can be visualized.
Second, an html document can be produced that gives an overview of the contamination in each genome.
Lastly, the contaminant contigs can be separated out from the non-contaminant contigs, writing two separate FASTA files per genome.
](images/charcoal_overview.png){#fig:overview}

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

### Datasets and benchmarking


# Results

**old results outline:**
+ charcoal estimates low contamination in non-representative GTDB genomes
+ charcoal assigns correct taxonomy to all non-representative GTDB genomes
+ charcoal vs. checkm
  + charcoal vs. checkm: mgnify, tara
  + checkm on charcoal clean
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
