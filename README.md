# PSMA PET SUVmax: reproducible analysis

Reproducible analysis code for:

**PSMA PET SUVmax Adds Information Beyond Conventional Risk Indices in Localized Prostate Cancer: A Prospective Lesion-Level Radiopathologic Study.** Motchoffo Simo et al. Submitted to *The Prostate*. Parent trial: ClinicalTrials.gov NCT04461509.

## What is here

- **PSMA_PET_analysis.Rmd** is an R Markdown file that recomputes every number reported in the manuscript and supplement: the cohort table, all SUVmax correlates, the adjusted models, the digital-pathology concordance, and the supplemental analyses. Its final section re-asserts each published value, so a failed check is the signal that the text and the data no longer agree.

## Data

The source data are not stored in this repository. They are provided as a supplement to the article: a de-identified, lesion-level workbook with sheets `analytic_foci`, `qupath_slides`, and a `data_dictionary`. To run the analysis, download that file from the article, name it `PSMA_PET_source_data.xlsx`, and place it in the same folder as the Rmd, or edit the `SOURCE_FILE` line at the top of the Rmd to match your filename.

## How to run

1. Install R (4.3 or later) and the packages `readxl`, `dplyr`, and `irr`.
2. Place the source-data workbook (`PSMA_PET_source_data.xlsx`) in the same folder as the Rmd, as described above.
3. Knit in RStudio, or run: `Rscript -e "rmarkdown::render('PSMA_PET_analysis.Rmd')"`
4. The final chunk prints "N of N assertions passed." A failure names the value that no longer matches the data.

## Citation

Please cite the manuscript above. Contact: Camille Motchoffo Simo. Corresponding author: Adam B. Weiner, MD.
