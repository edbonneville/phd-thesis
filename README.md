# PhD thesis: Statistical modelling of competing risks with incomplete data

This repository contains the sources files for my PhD thesis at Leiden University (defended on July 2nd, 2025), which was made using [Quarto](https://quarto.org/docs/books/) and [koma-script](https://ctan.org/pkg/koma-script). The pdf of the thesis is freely available at Leiden University Scholarly Publications ([online repository](https://scholarlypublications.universiteitleiden.nl/handle/1887/4252266)).

<img src="figures/thesis-cover.png" width="90%" align="center">

If you want to directly access the individual chapters (all were/are going to be published open access) + associated code, you can use the Table below:

| Chapter                                                      | Journal                                                      | DOI                                                          | Code repository                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Handling missing covariate data in clinical studies in haematology (Chapter 2) | *Best Practice & Research Clinical Haematology*              | [10.1016/j.beha.2023.101477](https://doi.org/10.1016/j.beha.2023.101477) | [https://github.com/survival-lumc/ReviewHaemaMissing](https://github.com/survival-lumc/ReviewHaemaMissing) |
| Multiple imputation for cause-specific Cox models: Assessing methods for estimation and prediction (Chapter 3) | *Statistical Methods in Medical Research*                    | [10.1177/09622802221102623](https://doi.org/10.1177/09622802221102623) | [https://github.com/survival-lumc/CauseSpecCovarMI](https://github.com/survival-lumc/CauseSpecCovarMI) |
| Impact of comorbidities and body mass index on the outcomes of allogeneic hematopoietic cell transplantation in myelofibrosis: A study on behalf of the Chronic Malignancies Working Party of EBMT (Chapter 4) | *American Journal of Hematology*                             | [10.1002/ajh.27262](https://doi.org/10.1002/ajh.27262)       | Not publicly available :(                                    |
| Multiple imputation of missing covariates when using the Fine–Gray model (Chapter 5) | *Statistics in Medicine*                                     | [10.1002/sim.70166](https://doi.org/10.1002/sim.70166) (to appear, for now use [preprint](https://arxiv.org/abs/2405.16602)) | [https://github.com/survival-lumc/FineGrayCovarMI](https://github.com/survival-lumc/FineGrayCovarMI) |
| Why you should avoid using multiple Fine–Gray models: insights from (attempts at) simulating proportional subdistribution hazards data (Chapter 6) | *Journal of the Royal Statistical Society, Series A (Statistics in Society)* | [10.1093/jrsssa/qnae056](https://doi.org/10.1093/jrsssa/qnae056) | [https://github.com/survival-lumc/FineGrayDGM](https://github.com/survival-lumc/FineGrayDGM) |
| Joint models quantify associations between immune cell kinetics and allo-immunological events after allogeneic stem cell transplantation and subsequent donor lymphocyte infusion (Chapter 7) | *Frontiers in Immunology*                                    | [10.3389/fimmu.2023.1208814](https://doi.org/10.3389/fimmu.2023.1208814) | [https://github.com/survival-lumc/ImmuneReconstJM](https://github.com/survival-lumc/ImmuneReconstJM) |



## Usage 

The thesis was rendered using

```r
quarto::quarto_render(output_format = "pdf")
```

..but most likely that will not work for you from the off as I have unfortunately done a fairly lackluster job of documenting the various R/LaTex/system dependencies here (oopsies).

Most of the heavy lifting for the formatting is done in [_quarto.yml](_quarto.yml), but the following non-standard stuff might be useful:

- [chapterthumb.sty](chapterthumb.sty) are the koma-script-based thumb indices for the chapters, with minor formatting edits also allowing for bleed correction when sending to the printers.
- [tex/preamble.tex](tex/preamble.tex) is the overall preamble, with some font settings + headings set-up.
- [tex/koma-chapter-titles.tex](tex/koma-chapter-titles.tex) is the koma-script-based emulation of the 'Lenny' chapter title style from fncychap, again with some minor edits.
- [tex/before-body.tex](tex/before-body.tex) is my set-up for the 'non-scientific' part of the thesis required by Leiden University, and used some pandoc variables.

## Credits

Credit to the following repositories and blog posts helping me put this thesis together:

- [https://cameronpatrick.com/post/2023/07/quarto-thesis-formatting/](https://cameronpatrick.com/post/2023/07/quarto-thesis-formatting/)
- [https://github.com/rekkasa/phd_thesis](https://github.com/rekkasa/phd_thesis)
- [https://github.com/bbartholdy/endgame](https://github.com/bbartholdy/endgame)
- [https://github.com/nmfs-opensci/quarto-thesis](https://github.com/nmfs-opensci/quarto-thesis)
- [https://github.com/alberto-guzman/quarto-dissertation](https://github.com/alberto-guzman/quarto-dissertation)

<!-- Finialise html with co-author yamls -->
