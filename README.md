# MICB475-Team-1 Meeting Minutes and Agenda

## Apr 8, 2024
Completed Deliverables: 
- presentation slides
  
Discussion: 
- Slideshow editing
- Reference list not necessary

Action Items:
- fix slides
- Guideline of how to coach team
    - Important statements for them to say etc
  
## Apr 4, 2024
Completed Deliverables: 
- figures as stated from last meeting

Discussion:
- move alpha diversity graphs to supplemental
    - S1: Alpha for Disease Status
    - S2: Alpha for OTC drugs
- Figure 1: Effect of MS only visible in individuals without Eczema
    - Beta Diversity - PCA, 2 panels: 1 for Jaccard and 1 for Bray-Curtis, significance by PERMANOVA p values mentioned in figure legends
    - Subset out all prescription ppl, run on OTC
    - Subset out all OTC ppl, run on prescription ppl
- Figure 2 (4 panels):
    - MS no prescription (Bray and Jaccard)
    - MS no OTC (Bray and Jaccard)
    - Indicate that prescription has no effect
- Figure 3:
    - Only want MS patients with eczema not taking prescription looking at the effects of OTC
    - Results from coding during the meeting: People with no eczema had a significant change in diversity when taking OTC vs people with eczema
    
- Ensure graphs are properly filtered and subsetted
    - Correcting for the confounding variable demonstrates a significant effect such that ppl with eczema appeared to be a bit more responsive to OTC drugs?
    - If not significant, the story just changes such that OTC drugs don’t seem to have an effect regardless if you have eczema or not
      
Action Items: 
- clarify story & create powerpoint slides

## Mar 28, 2024
Completed Deliverables: 
- alpha & beta analyses for only MS patients
- Indicator + core microbiome analyses
  
Discussion:
- ditch MS prescription angle, or do brief description in manuscript
- Limiting factor → small sample size
    - 9 ppl with MS, eczema & taking OTC
- figures + tables
    - figure 1
        - Beta diversity MS vs. eczema
            - 2 panels (2 PCoAs) for Jaccard + Bray Curtis
    - figure 2
        - Alpha diversity OTC Drugs
            - Shannon and Observed (OTC and prescribed) - show OTC prescription is not significant
            - 4 panels
    - figure 3
        - Alpha diversity
            - MS patients with eczema
            - MS patients without eczema
    - table 1
        - top table: OTC indicators
        - bottom table: eczema indicators
        - put common ones in gray, look at UJEMI for formatting
    - table 2
        - core microbiome, 2 panels → look at effect of OTC
            - MS, eczema & OTC
            - MS, no eczema & no OTC   
    - Supplemental
        - Alpha Diversity MS vs. eczema → showing no significance (Average diversity of the community - the 4 figures)
        - Frequency Table: Create frequency table separating eczema patients with MS and how many of them are taking OTC/prescription drugs

Potential next steps: 
- create figures


## Mar 21, 2024
Completed Deliverables: 
- alpha & beta diversity results for MS vs eczema & OTC vs prescription

Discussion:
- beta diversity
    - significance for MS vs eczema
        - MS has effect on non-eczema patients but not ppl with eczema
    - significance for OTC vs prescription medicine
        - Prescription medication has impact on patients (does not matter if  you’re taking OTC drugs or not)
- alpha diversity
    - no significance for MS vs eczema
    - significance for OTC vs prescription medicine
        - Taking OTC drugs makes ppl susceptible to microbiome changes caused by prescription medication
          
Potential next steps: 
- Subset for ONLY MS patients to compare effect of medication type
    - effect of eczema
- Indicator species + core microbiome analysis
    - Look at effect of MS on eczema/non-eczema patients
    - Set 1
        - Look at MS patients who take prescription medication
            - Find indicators in OTC/non-OTC
        - MS patients not taking prescription medication
            - Find indicators in OTC/non-OTC
    - Set 2
        - Look at people taking OTC
            - Find indicators in prescription/non-prescription
        - People not taking OTC
            - Find indicators in prescription/non-prescription 

## Mar 14, 2024
Completed Deliverables: Analyzed the different components discussed last meeting

Discussion:
- Eczema showed a mediating effect (because of significant difference between groups without eczema, but no effects seen when patients all had eczema)
- Patients more susceptible to changes of the microbiome induced by over the counter medication

Potential next steps
- Compare OTC and RX medication effect on the diversity in the gut, and investigate the indicator species
- Use a barplot or PCoA plot to look at whether there is general clustering and difference
- alpha diversity through bar plots
- beta diversity through PCoA and PERMANOVA
- Look at indicator taxa and core microbiome analysis for specific groups that show most promise

## Mar 7, 2024
Completed deliverables:
Alpha diversity for MS type, sex, and eczema --> only MS type, and eczema showed a level of distinction

Discussion:
- Using a statistical test to compare to see if there is a significant difference between the visual differences we are seeing
- There is not much statistical difference
- Control for age, sex, and BMI
- There is a large difference between individuals in the same exprimental group

## Feb 29, 2024
Completed deliverables:
Alpha and beta diversity anysis: Completed upload to QIIME2 and data processing and trimming, alpha and beta diversity metrics showed no significant differences

Discussion:
Paper found significance in sex, age, and bmi
Potentially could control for vitamin D supplementation as well

Action Items:
Filter for vitamin D supplementation (i.e 0)
Further seggregation of experimental groups based on age, sex, and BMI

## Feb 15, 2024
Completed deliverables: 
Data wrangling: Controlled for for Cohort 2 and non smokers, isolated for unique samples in the metadata, created an rx_meds column that is true and false

Action Items:
Create a new column combining the disease state annd eczema state (ex MS, eczema)
Import dataset to QIIME2
Complete alpha and beta diversity analysis

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

### Data wrangling
- kept only non-smokers and cohort 2
