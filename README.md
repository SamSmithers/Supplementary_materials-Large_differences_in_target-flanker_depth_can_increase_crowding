# Supplementary material: Effect of depth on crowding investigated with a multi-depth plane display (Pre-print/under review)
### Supplementary information for: *Effect of depth on crowding investigated with a multi-depth plane display.* Samuel P. Smithers, Yulong Shao, James Altham, and Peter J. Bex. 

## Repository contents
- Raw date from Experiments 1-5 (files ending "*_rawData.csv*").
- ```Cal_CircSD.m```: Matlab code used to accumulate the raw data from each experiment and calculate perceptual error. Outputs processed data as "*_accumulatedPerErr.csv*" or "*_accumulatedPerErr_TargetInsideRing.csv*".
- Accumulated perceptual error data for Experiments 1-5 generated by ```Cal_CircSD.m``` (files ending "*_accumulatedPerErr.csv*").
- Accumulated perceptual error data for Experiments 1-4 based only on trials in which the subject reported seeing the target inside the flanker ring generated by ```Cal_CircSD.m``` (files ending "*_accumulatedPerErr_TargetInsideRing.csv*").
- ```Perceptual error data analysis.R```: R code used to generate the figures for, and perform the statistical analysis on, the perceptual error data reported in the main manuscript and supplementary material.
- ```Perceived target position data analysis.R```: R code used to generate the figures for, and perform the statistical analysis on, the data for the perceived position of the target relative to the flanker ring that was reported by observers in Experiments 1-4. 

## Calculating perceptual error (i.e. circular standard deviation) & accumulating raw data (MATLAB)
### Requirements & dependencies
- MATLAB R2022a (other versions should work but this one is tested)
- [MATLAB Circular Statistics Toolbox](https://www.mathworks.com/matlabcentral/fileexchange/10676-circular-statistics-toolbox-directional-statistics)

#### Running instructions
1. Manually download ```Cal_CircSD.m``` and raw data files from this repository. The raw data from each experiment should be kept in separate folders for the script to work. Alternatively, you can clone this repository ([instructions here for MATLAB](https://www.mathworks.com/help/simulink/ug/clone-git-repository.html)). 
2. Install any uninstalled dependencies, above.
3. Open ```Cal_CircSD.m``` and follow instructions within the script. 

## Statistical analysis & plotting (R)
### Requirements & dependencies
- R version >= 4
- The following packages must be installed: 
  - ggplot2
  - ggh4x
  - lme4
  - Matrix
  - DHARMa
  - svglite (optional to save plots)
  - gridExtra (optional to arrange/combine plots for saving)
  - bannerCommenter (optional)

#### Running instructions
1. Manually download ```Perceptual error data analysis.R``` and ```Perceived target position data analysis.R``` from this repository. You will also need to download the "*_accumulatedPerErr.csv*" and "*_accumulatedPerErr_TargetInsideRing.csv*" data files (required by both R scripts) along with the raw data files (required for ```Perceived target position data analysis.R``` only). The raw data from each experiment should be kept in separate folders for the script to work. Alternatively, you can clone this repository ([instructions for Rstudio here](https://datacarpentry.org/rr-version-control/03-git-in-rstudio/index.html)). 
2. Install any uninstalled dependencies, above.
3. Open ```Perceptual error data analysis.R``` and/or ```Perceived target position data analysis.R``` and follow instructions within the script.
