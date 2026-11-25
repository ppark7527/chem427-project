# Judgment log: Princess Park

## How I used AI in this project
I had Claude read the data from knoevenagel.tar.bz2 to create the initial analysis.ipynb based on project list's description (which came out similar to previous session's activity.ipynb(s)); that includes code sections, such as parameters and analysis, leaving analytical decisions to me. Claude wrote codes, peak integrations, calibration fits, residuals, and explanatory markdowns comparable to previous sessions.
(Final submission only.)

## Entries
### 2026-11-24 Benzaldehyde detection wavelength at 249 nm.
Ran a calibration for one analyte (benzaldehyde) on one gradient (2.50 min). Detection wavelength chosen where benzaldehyde absorbs strongly and blank is also low: 305.8 mAU at 249 nm, blank at 8.2 mAU. Strongest corrected absorbance of 480.9 mAU at 201 nm not chosen due to high blank at 72.7 mAU. Cells 10–12 show the benzaldehyde peak at 1.283 min, 305.8 mAU above the blank. The blank drifts from −0.2 to 19.7 mAU at 249 nm over the run, subtracted from standard at each time point.
- **What the assistant suggested:** Assistant suggested checking 249 nm band for first-calibration standard against a literature UV spectrum of benzaldehyde.
- **What I did:** I checked online and according to technical guides, benzaldehyde does show a π → π* transition at ~248 nm in water (https://pdf.benchchem.com/3430/A_Technical_Guide_to_the_Spectroscopic_Identification_of_Benzaldehyde.pdf, accessed 2026-11-24).
- **Why, from my data:** So, dissolving benzaldehyde in a suitable solvent should obtain a well‑defined absorbance peak close to lit. value of ~248 nm. This validates me choosing detection wavelength at 249 nm. Shows that the band really is benzaldehyde and the data loaded correctly for first calibration run. 249 nm will be used as a choice for comparing gradients.

Note: 259 nm only checked for 2.50 min gradient (2026-11-24).

### 2026-11-24 Series 1 level 075 first calibration outlier
Series 1 level 075 standard excluded as large outlier with area per mM of 3459 vs ~300 for the other seven standards, and a peak height of 2443 mAU vs 228 mAU for series 2 lvl 075. Excluding standard makes slope well fit to calibration results: with, slope = 824.8 ± 1135.0 mAU s/mM and R² 0.08; without, slope = 294.6 ± 2.5 and R² 0.9996.

- **What the assistant suggested:** Assistant suggested checking if solution or injection is source of outlier.
- **What I did:** Series 1 level 075 first calibration run is currently left as an exclusion.
- **Why, from my data:** Presumed to be an outlier for just the single injection, series 1 level 075 standard for benzaldehyde (area per mM of 3459 vs ~300 for the other seven standards, and a peak height of 2443 mAU vs 228 mAU for series 2 lvl 075). Left it as an exclusion on this one run and will keep level 075 on other gradients. Excluding standard makes slope well fit to calibration results: with, slope = 824.8 ± 1135.0 mAU s/mM and R² 0.08; without, slope = 294.6 ± 2.5 and R² 0.9996.

Note: If the issue is the solution then the vial itself was wrong and series 1 level 075 is wrong on all gradients and should be excluded from every series 1 calibration. This relates to project question of whether noise comes from the instruments or the solutions.
