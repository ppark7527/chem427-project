# 004: First Calibration Analysis/Results

- **Status:** done
- **Created:** 2026-11-22
- **Updated:** 2026-11-24
- **Due:** 2026-11-22 11:59pm

## Goal
Use code to visualize data on first calibration line for benzaldehyde on the 2.50 min gradient. Analyze and explain choices regarding what nm to use, blank subtraction, excluding series 1 level 075 or not, and explain the results; include reason for using linear regression, the slope, and the method (Beer-Lambert: area is proportional to concentration).

## Steps
1. Load the runs. Read the archive with tarfile and keep the 4 blanks and 8 benzaldehyde standards on the 2.50 min gradient. (cells 3–4)
2. Check the data on loading. Record the problems and what you did about each: UTF-16, the unnamed time column, the different run lengths, the negative absorbance below 208 nm, and the missing concentrations. (cells 5–8)
3. Plot one standard against its blank. Find the peak at 1.283 min and see how much the baseline drifts, from −0.2 to 19.7 mAU. This is the reason for blank subtraction. (cells 9–11)
4. Choose the wavelength. Plot the apex spectrum against the blank and compare 201 nm with 249 nm. Choose 249 nm because the blank there is 8.2 mAU, against 72.7 mAU at 201 nm. Check it against a literature UV spectrum of benzaldehyde. (cells 12–14)
5. Integrate the peaks. Subtract the blank, integrate apex ± 0.05 min, and compute the area per mM for all 8 standards. (cells 15–17)
6. Decide on series 1 level 075. Compare its area per mM (3459) with the others (294–310), and write your reason in cell 18. (cell 18)
7. Fit the calibration line. Fit with and without the excluded standard. Explain why linear regression fits: Beer–Lambert says area is proportional to concentration. Record the slope, intercept, R² and residual SD. (cells 19–20)
8. Check the residuals. Confirm there's no curve and no offset between series. (cells 21–23)
9. Record the result. Write the slope, 294.6 ± 2.5 mAU s/mM, in the Outcome, and state what comes next (task 006).

## Done when
The calibration line, its residual plot, and the reason for each choice (wavelength, blank, exclusion) are in the notebook, and the slope with its standard error is recorded.

## Progress log
2026-11-24 Wrote first calibration analysis entry directly into analysis.ipynb notebook in cell 26.

## Outcome
Written in analysis.ipynb also.

Ran a calibration for one analyte (benzealdehyde) on one gradient (2.50 min). Detection wavelength chosen where benzaldehyde absorbs strongly and blank is also low: 305.8 mAU at 249 nm, blank at 8.2 mAU. Strongest corrected absorbance of 480.9 mAU at 201 nm not chosen due to high blank at 72.7 mAU. Cells 10–12 show the benzaldehyde peak at 1.283 min, 305.8 mAU above the blank. The blank drifts from −0.2 to 19.7 mAU at 249 nm over the run, subtracted from standard at each time point. Series 1 level 075 standard excluded as large outlier with area per mM of 3459 vs ~300 for the other seven standards, and a peak height of 2443 mAU vs 228 mAU for series 2 lvl 075. Excluding standard makes slope well fit to calibration results: with, slope = 824.8 ± 1135.0 mAU s/mM and R² 0.08; without, slope = 294.6 ± 2.5 and R² 0.9996. Residuals of calibration line demonstrate random scatter near zero with no curve or offset, indicating a straight line fit with left over as random noise: residuals lie between −2.66 and +2.55 mAU s, under 1% of the largest area, no clear curve; the intercept of 2.2 ± 1.7 mAU s is within 1.3 standard errors of zero. 