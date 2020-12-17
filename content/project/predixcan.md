---
title: 'PrediXcan'
date: ''
weight: 1
---

### PrediXcan, a regulatory mechanism driven gene discovery tool

Although investments in genomic studies of complex diseases made possible the discovery of thousands of variants robustly associated with these traits, the translation of these discoveries into actionable targets has been hampered by the lack of a mechanistic understanding on how genome variation relates to phenotype. Moreover, it has been widely shown that a substantial portion of the genetic control of complex traits is exerted through the regulation of gene expression traits, but effective methods to fully harness this mechanism were not available. To address these challenges, we developed a gene-based test —PrediXcan— that directly tests this regulatory mechanism and substantially improves power relative to single variant tests and other gene-based tests. PrediXcan is inherently mechanistic and provides directionality, highlighting its potential utility in identifying novel targets for therapy. PrediXcan was the first of the class of methods known currently as TWAS (transcriptome-wide association studies). More details can be found [in this paper](https://uchicago.box.com/shared/static/ilqi3c12j5z8gu6puiiemumai0vgl6h2.pdf). The following figure shows a schematic description of the method.

|![](https://uchicago.box.com/shared/static/d3ab2xn2ivrj3yfo9tkkeo3qrfew4k4k.png)|
|:--:|
| *PrediXcan tests the mediating effect of a target gene on disease risk.* The left panel shows the components of the expression of a gene. PrediXcan tests the association between the genetically regulated component and the complex trait and is not affected by the reverse effects of the disease on the expression. The mechanistic model behind PrediXcan is shown on the right panel. The genetic profile of an individual determines a baseline gene expression level (genetically determined expression), which is further modified by environment and other factors. For deleterious causal genes this final level determines the liability to disease which can lead to disease if it surpasses certain threshold. |
