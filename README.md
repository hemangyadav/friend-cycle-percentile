# FRIEND Cycle VO2 Percentile Calculator

A single-page, browser-based calculator using the 2022 FRIEND cycle-ergometer peak VO2 reference standards for U.S. adults aged 20-89 years.

## What the calculator does

- Inputs: age, sex, peak VO2 in mL/kg/min, and peak RER.
- Uses the published 10-year age group and sex-specific cycle values from Table 3 of Kaminsky et al. (2022), using the RER >= 1.0 reference cohort.
- Returns an estimated numerical percentile between the published 10th and 90th percentile values by linear interpolation.
- Returns "below the 10th percentile" or "above the 90th percentile" outside the published range rather than extrapolating.
- Uses peak RER as an effort-quality flag. It does not switch reference tables at RER 1.10.
- Includes a copy-ready report sentence.
- Runs entirely in the browser and has no analytics, database, or server-side code.

## Publish with GitHub Pages

1. Create a new public GitHub repository, for example `friend-cycle-percentile`.
2. Upload `index.html` and this `README.md` to the root of the repository.
3. In the repository, open **Settings > Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch **main** and folder **/(root)**, then select **Save**.
6. After deployment finishes, use **Visit site** in the Pages settings.

The site address will normally be:

`https://YOUR-GITHUB-USERNAME.github.io/friend-cycle-percentile/`

## Validation examples

- Age 58, female, peak VO2 15.5, RER 1.15: approximately 33rd percentile.
- Age 43, male, peak VO2 27.0, RER 1.12: approximately 48th percentile.
- Age 65, female, peak VO2 21.1, RER 1.10: above the 90th percentile.

Before clinical use, validate every exact table knot and representative interpolated values against the source table.

## Reference

Kaminsky LA, Arena R, Myers J, et al. Updated Reference Standards for Cardiorespiratory Fitness Measured with Cardiopulmonary Exercise Testing: Data from the Fitness Registry and the Importance of Exercise National Database (FRIEND). Mayo Clinic Proceedings. 2022;97(2):285-293. doi:10.1016/j.mayocp.2021.08.020.

## Important limitations

This tool is a reference calculator, not a determination that a CPET was maximal and not a diagnosis. It uses published decade-based age groups and therefore retains discontinuities at age-group boundaries. The FRIEND cohort consisted of apparently healthy U.S. adults. The 80-89 cycle sample was small, particularly for women.

Do not enter patient identifiers.
