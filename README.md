This repository contains 3 data files:

**1) Copies_mL Calc Table.xlsx**
   - This datasheet shows the Cq and copies/mL value for each sample that was run through a qPCR assay. NTC Cq values are included on an additional tab. 
   - Sample Processing
      - Samples were collected in polyprpylene bottlesand filtered onto 0.4um filters and volume was recorded
      - Filters were stored at -20 until extraction
      - Extracts (up to 100uL) were kept at -20C until use
  - Calculations
      - To get copies/mL values, the following variables were used:
      - Volume Filtered: Volume of water sample collected on filter during processing
      - Cq: Cycle number in qPCR reaction where the flurescence crosses a pre-determined threshhold 
      - log10(SQ): Log10(Starting Quanity). This value is determined using the equation of a line from running a standard curve that is specific to the qPCR target
      - SQ: The starting quanity of the target in the sample (equal to copies/uL in this case)
      - Dilution Factor: If extract needed to be diluted prior to runnung qPCR . For example, if there was a high inhibition prevlalance. If the samples was diluted 1:10, the dilution factor would be 10
      - Concentration Factor: Used to standardize different filtration volumes. 100mL = 1, 50mL = 2, 30mL = 3.33 (100/filter volume)
      - Copies/mL = SQ*Concentration Factor * Dilution Factor 
  - Notes
      - Any sample that was below the limit of detection was assigned a value of 50% limit of detection. As it could still be present despite low quantity, and therefore may not be a false positive
      - Because of this, samples that were below the LOD (as SQ) may have varying copies/mL calculastions depdning on the concentration factor (i.e. volume filtered)
      - Samples that had no detection have a value of NA
      - V. cholerae assay at Blind Oso had 5 replicates due to high variability

**2) Monthly Water Quality Data.xlsx**
   - This datasheet contains water quality information (nutrients, salinity, temperature) taken monthly (2022) at each site barring January for all sites, and February for the Gulf site.

**3) tx_master_Daily_REPS (1).csv**
   - This master datasheet contains:
      - Water quality (Nutrients, Dissolved Oxygen, Temperature, pH, Salinity, Chlorphyll-a, TSS), qPCR (Total Bacteria, Total Vibrio, V. vulnificus, V. parahaemolyticus,  V. cholerae, V. alginolyticus, Bacteroides (HF183), Culture (Yellow/Green colony forming units (CFU)), dust (AOD, and AOD_24h_Lag). 
