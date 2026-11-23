# 006: Series 1 Level 075 Outlier: Solution or Injection?

- **Status:** active
- **Created:** 2026-11-22
- **Updated:** 2026-11-23
- **Due:** 2026-12-01 11:59pm

## Goal
Compute the area per mM of series 1 level 075 on all five gradients and compare it with series 2 and with the other levels.

## Steps
1. Find out from Haas et al. (2023) or the MOCCA documentation whether series 1 and 2 injected the same vials or separately prepared solutions, and record which.
2. Look at the raw chromatogram of series 1 level 075 at 249 nm beside series 2 level 075: retention time, peak shape, any extra peaks, and whether the 2443 mAU apex is above the detector's linear range.
3. Compare the spectrum at its apex with the series 2 level 075 apex spectrum, to check it is benzaldehyde and not another compound or a mislabeled vial.
4. Integrate benzaldehyde (249 nm, ±0.05 min, same blank method) for all 4 levels × 2 series on all 5 gradients, and compute the area per mM of each.
5. Make a table and a figure of area per mM against gradient length, with one marker per series and level, so that series 1 level 075 can be compared with the other 7 standards on every gradient.
6. Check the run timestamps for what was injected just before series 1 level 075, in case of carryover.
7. Decide: high on every gradient points to the solution; high on the 2.50 min gradient only points to one injection. Set `EXCLUDED_STANDARDS` to match, and write the reason in cell 18.

## Done when
Recorded whether it's high on every gradient or only on the 2.50 min gradient, and EXCLUDED_STANDARDS follows from that, with a reason written in cell 18.

## Progress log

## Outcome