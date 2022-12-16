# The Effect of Opportunity Zones on Employment: Early Results from the Longitudinal Employer-Household Dynamics Origin-Destination Employment Statistics
## Authors: Adelaide Currin & Jennah Gosciak, December 2022

This repository holds all code used in developing the fall semester empirical research project in NYU Wagner's Doctoral Research Methods course. Preliminary results can be viewed [here](https://docs.google.com/presentation/d/19Nqy_VqwDpl-Me1GjUJ6hwGkGivOs0sjsjoTvenWi_I/edit?usp=sharing).

- **Research Design:** DiD; Two way fixed effects
- **Intervention:** Opportunity Zones (OZs); A 2018 place-based policy that incentivizes investment in selected census tracts
- **Sample:**	Low-Income Community (LIC) tracts or tracts contiguous with LICs in top commuting zones
- **Outcome of interest:** Year-to-year percent change growth in jobs, disaggregated by wage, race, ethnicity, and commuting patterns
- **Key findings:** Few statistically significant or practically significant results


Folder structure:
- 0_data: local folder for storing data files, though most files were downloaded from through R packages.
- 1_input: variable lists and other documentation.
- 2_output: plots and table output.
- 3_programs: data cleaning and analysis code.
  - [0_Load Ozs and Census Data.Rmd](https://github.com/jennahgosciak/RMproject/blob/main/3_programs/0_Load%20Ozs%20and%20Census%20Data.Rmd): downloads raw data through `lehdr` and `tidycensus`. Processes OZ data file from HUD
  - [1_LODES Data Cleaning.Rmd](https://github.com/jennahgosciak/RMproject/blob/main/3_programs/1_LODES%20Data%20Cleaning.Rmd): appends yearly LODES data files together to create a single LODES file, extracts relevant outcome variables
  - [2_Create Analysis File.Rmd](https://github.com/jennahgosciak/RMproject/blob/main/3_programs/2_Create%20Analysis%20File.Rmd): merges and appends files together, creates key constructs
  - [3_Run Analysis.Rmd](https://github.com/jennahgosciak/RMproject/blob/main/3_programs/3_Run%20Analysis.Rmd): runs main specifications for the analysis
  - [4_Parallel Trends.Rmd](https://github.com/jennahgosciak/RMproject/blob/main/3_programs/3_Run%20Analysis.Rmd): tests the parallel trends assumption and runs baseline equivalence checks
