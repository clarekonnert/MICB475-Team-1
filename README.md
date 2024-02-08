# MICB475-Team-1 Meeting Minutes and Agenda

## Feb 8, 2024
Paper and Metadata selected
MICB 475 Project Paper

### Research Question Options
- oral contraception 
- use of NSAIDs on microbiome diversity and its implication on MS
- 2 medication groups → otc vs NSAIDs, otc vs. prescription
- eczema & correlation with MS
- Topical steroid cream for eczema 
- How eczema changes the microbiome on healthy and MS patients and whether steroid creams health → improved microbiome 
- Impact of biological sex on various variables and implication on MS 
- Lots of paired end sequences. Running analysis will take a long time. Review QIIME2 documentation. Detached overnight.

### Action Items
- Create read me file (to keep track of minutes, agenda, and project), folder with QIIME2 and folder for R. Output folder for each
- How to make a folder: <Name of folder> / → Create empty file 
- Github desktop/jupyter
- R Studio Github attachment

Data wrangling:
1. Use R to create new metadata →  healthy eczema & non-eczema vs. MS eczema & non-eczema
    - New column for prescribed meds → yes or no
    - N/A for missing data → do not delete
    - Identify confounding variables in all the other categories. FIlter everything else out but keep things that you might want to explore later. Ensure that it doesn’t reduce the sample size, otherwise keep the confounding variable and mention it as a limitation.
    - Potentially control for smoking
    - Potentially control for cohort
    - Good practice to do it in R
    - Do the same for the manifest file 
3. QIIME2 processing
4. Alpha/Beta diversity analysis, recommended to do on both QIIME2 and R (whole data set - 4 groups, and separated? - R filter, look at drug vs non-drugged. This process will depend on what our data shows/significance)
5. Examining profiles - indicator taxa analysis → predicted profile of someone who takes drugs vs not, eczema etc…
6. Core microbiome
