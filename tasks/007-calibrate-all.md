# 007: Calibrating Every Gradient and Analyte

- **Status:** active
- **Created:** 2026-11-22
- **Updated:** 2026-11-23
- **Due:** 2026-12-01 11:59pm

## Goal
Peak areas and calibration slopes for 3 analytes × 5 gradients.

## Steps
1. Choose a detection wavelength for `ome` and `nme2` from each standard's apex spectrum minus the blank, where the analyte absorbs strongly and the blank is low, and check each against a literature UV spectrum.
2. For each gradient, find each analyte's retention time and its width at half height, and check that ±0.05 min still covers the whole peak on the 0.50 min gradient. If it does not, set the window by gradient in Parameters, with the reason.
3. Check the blanks for peaks near each analyte's retention time on every gradient, and check the standards for co-eluting peaks.
4. Change the loading cell to read all 120 standards and 20 blanks, keeping only `time_min` and the detection wavelengths, so memory stays small.
5. Integrate every standard with the same blank subtraction and window, and make a table of area and area per mM, flagging any standard far from the others with the rule decided in task 006.
6. Fit a line of area against concentration for each analyte and gradient, and record the slope ± standard error, intercept, R², and residual SD.
7. Plot the residuals of each fit, to check for curvature or an offset between series.
8. Check that the slopes make chemical sense: at constant flow rate, the area per mM should change little with gradient length, so a large change needs an explanation.

## Done when
There's a table of 15 slopes with standard errors.

## Decisions to record
A detection wavelength for ome and nme2, checked on their spectra the way you did for 249 nm; whether ±0.05 min still fits the peaks on the 0.50 min gradient; and any co-elution.

## Progress log

## Outcome