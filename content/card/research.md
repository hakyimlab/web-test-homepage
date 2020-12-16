+++
# An example of using the custom widget to create your own homepage section.
# To create more sections, duplicate this file and edit the values below as desired.

date = "2016-04-20T00:00:00"
draft = false

title = "Research"
subtitle = ""
widget = "custom"

# Order that this section will appear in.
weight = 15

+++

## Research

The overarching goal of our research program is to develop computationally efficient and statistically sound methods to sift through the vast amounts of genomic and other high dimensional data with the goal of making discoveries that can be translated to improve human health.

To achieve this goal, we build and maintain an analytic infrastructure, i.e. a dry lab. This includes statistical and computational methods, pipelines and workflows, streamlined access to big data, and a research software engineering, bioinformatic and analysis team. This infrastructure constitutes a powerful instrument that gives us a unique vantage point from which discoveries can be made.



Below, we highlight some of the methods we have developed and future directions of the lab. The full list of our publications can be found [here](https://scholar.google.com/citations?hl=en&user=1QD4sIcAAAAJ&view_op=list_works&sortby=pubdate)

### PrediXcan, a regulatory mechanism driven gene discovery tool

Although investments in genomic studies of complex diseases made possible the discovery of thousands of variants robustly associated with these traits, the translation of these discoveries into actionable targets has been hampered by the lack of a mechanistic understanding on how genome variation relates to phenotype. Moreover, it has been widely shown that a substantial portion of the genetic control of complex traits is exerted through the regulation of gene expression traits, but effective methods to fully harness this mechanism were not available. To address these challenges, we developed a gene-based test —PrediXcan— that directly tests this regulatory mechanism and substantially improves power relative to single variant tests and other gene-based tests. PrediXcan is inherently mechanistic and provides directionality, highlighting its potential utility in identifying novel targets for therapy. PrediXcan was the first of the class of methods known currently as TWAS (transcriptome-wide association studies). More details can be found [in this paper](https://uchicago.box.com/shared/static/ilqi3c12j5z8gu6puiiemumai0vgl6h2.pdf). The following figure shows a schematic description of the method.

|![](https://uchicago.box.com/shared/static/d3ab2xn2ivrj3yfo9tkkeo3qrfew4k4k.png)|
|:--:|
| *PrediXcan tests the mediating effect of a target gene on disease risk.* The left panel shows the components of the expression of a gene. PrediXcan tests the association between the genetically regulated component and the complex trait and is not affected by the reverse effects of the disease on the expression. The mechanistic model behind PrediXcan is shown on the right panel. The genetic profile of an individual determines a baseline gene expression level (genetically determined expression), which is further modified by environment and other factors. For deleterious causal genes this final level determines the liability to disease which can lead to disease if it surpasses certain threshold. |

### Scaling up PrediXcan to integrate large-scale data

Genetic studies have discovered many thousands of locations on chromosomes that are associated with health or disease, but the majority of these fall outside of protein-encoding regions, and so it is difficult to understand just how they exert their influences. PrediXcan leverages large scale DNA, observable trait, and gene expression datasets, as well as machine learning, to infer from these discoveries which genes are actually influenced and whether an up or downregulation of the gene is beneficial. Despite the appeal and success of this approach, which directly identifies candidate drug targets, accumulating experience revealed that data from over a million individuals would be required in many cases. We therefore developed an approach that bypasses the need to use individual level data and takes advantage of summary results, to vastly expand the applicability and power of the original PrediXcan method. The new approach, called S-PrediXcan, allows to find potential target genes for modulating thousands of traits across a broad set of human tissues. These results are now publicly available and have gathered users across the globe and led to funded collaborations. Most of the associations proved to be tissue-specific, suggesting context specificity of the trait etiology. Significant associations in unexpected tissues also underscored the need for an agnostic scanning of multiple contexts to improve the ability to detect causal regulatory mechanisms. Monogenic disease genes were enriched among significant associations for related traits, suggesting that smaller alterations of these genes may cause a spectrum of milder phenotypes. More details can be found [in this paper](https://www.nature.com/articles/s41467-018-03621-1)

### Genetic architecture of expression traits across tissues

We investigated the genetic architecture of gene expression traits, which are important intermediate processes to understand the mechanisms by which genetic variation affect complex diseases and traits. We found that in contrast to the polygenic nature of complex diseases, most of the variation of gene expression traits is driven by a small number of variants (eQTLs). In addition to providing insight into the biology of the transcriptome, this finding has practical implications for the best approaches to predict gene expression traits. More details can be found [in this paper](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1007586)

### Boosting the power to identify target genes by exploiting the tissue sharing of gene expression regulation

An unexpected finding from the GTEx consortium (large scale transcriptome study of 900 organ donors with whole body tissue sampled across 49 tissues) was the widespread sharing of genetic regulation of expression traits across tissues. We estimated that more than half of the eQTLs (variants associated with expression levels) are active across all tissues. One implication of this is that eQTL-based studies will have little specificity to narrow down the tissue where disease initiates. However, one can take advantage of this lack of specificity and consider the different tissue panels as independent experiments and aggregate the information across all of them. We developed MultiXcan to implement this idea and show its effectiveness. More details can be found [in this paper](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1007889)

### Application to childhood and adult onset asthma data in the UK Biobank

Regardless of how sophisticated they may be, analytical methods only matter if they can answer relevant scientific questions. We teamed up with Carole Ober and Dan Nicolae, experts in asthma genetics, to examine the shared and distinct genetic factors of childhood and adult onset asthma risk applying state of the art methods implemented in our lab’s analytical pipeline. For the first time, data on age of onset of asthma became available through the UK Biobank for a sufficiently large number of individuals. We seized the opportunity to identify novel genetic factors that are specific to childhood onset cases as well as those shared with adult onset cases. We found that genetic factors of adult onset asthma are a subset of childhood onset asthma with overall smaller effects suggesting a larger environmental component in adult cases. Tissue enrichment analysis suggested the role of allergy and epithelial barrier disfunction in childhood onset asthma and lung involvement in adult onset asthma. Both types shared immune components. More details can be found [in this paper](https://uchicago.box.com/shared/static/oxziuex5lpjzrg3oguobnpvk1amehhz0.pdf)

## Ongoing research

### Enhancing PrediXcan to improve power and specificity
PrediXcan method has proven to be successful and widely adopted. However there are several aspects that can be improved to increase detection and reduce false discoveries. A substantial portion of my effort will be devoted to developing methods to achieve this goal.

### Reducing spurious results due to LD contamination
Linkage disequilibrium (LD, correlation of genetic variation within proximal genomic regions) can lead to associated genes and phenotypes even when the underlying causal variants are distinct. This is a difficult problem given the widespread LD in the population. We are examining several approaches to mitigate this problem. One is by using fine-mapping methods, which seeks to increase the resolution of the association and narrow down the causal variant to a single variant. Another one is to use orthogonal approaches that seek to cancel out the confounding by averaging across multiple independent genes.

### Methods to quantify mediating role of molecular traits that are robust to LD contamination
The goal is to quantify the proportion of phenotypic variability that can be explained by the regulation of transcript levels or other molecular intermediate phenotypes. We call this concept regulability in analogy to the heritability concept. This quantity can be tissue dependent. Characterizing the relative importance of different tissues and brain regions will provide insight into the etiology of complex diseases. Moreover, this method can be applied to quantify the contribution of a gene set or pathway, which provides not only significance but also magnitude of the effect.

### Open sharing of software, methods, and public databases of resources and results
Users across the globe are using PrediXcan and related methods and resources. We will continue hosting the resources and providing support to users.

### Build a catalog of the function of every human gene (PhenomeXcan)
One of the important feature of PrediXcan is the ability to identify target genes. My team and We will apply state of the art methods from my lab to large scale data from UK Biobank and other public repositories such as dbGaP to build a catalog of the function of every human gene.

### Extend PrediXcan to imaging (ImageXcan)
Environmental perturbations have a large impact in phenotypes both in concert and independently of genetic factors. We will investigate the effect of environment and its interaction with genetic factors on complex phenotypes. Large scale biobanks, such as UK Biobank and the recently started All of Us, offer an unprecedented opportunity to study gene-environment interaction with high dimensional data on millions of individuals. We will start to extending the ideas of PrediXcan from the transcriptome to the “radiome”, the high dimensional data available in MRIs and other images of the human body. We expect this line of research to provide important insights into the gene and gene-environment contribution to complex diseases. It will be a focus of my R01 application anticipated to be submitted in October 2019.

### Multi-ethnic and multi-omic extension of PrediXcan
Until recently, large reference transcriptome datasets were composed of individuals of mostly European descent. In response to the need of multi-ethnic representation, The NHLBI Trans-omics for Precision Medicine (TOPMed) Program has selected samples from the Multi-Ethnic Study of Atherosclerosis (MESA) for the pilot phase of trans-omic data generation. This provides the opportunity to address the limitations of PrediXcan by training prediction models in multiple ethnic backgrounds. Therefore, We propose here to adapt my prediction pipelines for the multi-ethnic RNA-seq, methylomic, and proteomic data from MESA. These prediction models will allow propagation of molecular information from the subset of assayed individuals to the much larger set for which only genetic data are available. Leveraging these higher quality models, We anticipate achieving improved functional data interpretation and multi-ethnic performance.
