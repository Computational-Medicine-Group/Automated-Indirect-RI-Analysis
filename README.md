# Indirect Estimation of Reference Intervals from Clinical "Big Data"

This repository contains the RMarkdown script (Handout.Rmd) for the analysis of indirect reference intervals (RIs) from clinical cohort data. The script provides a step-by-step instructions to perform the analysis and generate results.

## Introduction

Reference intervals play a crucial role in diagnostic medicine, helping physicians identify potentially pathological states in patient test results. By utilizing newer methodologies like refineR, we can estimate precise RIs directly from routine clinical data, making it especially valuable for patient groups with unique characteristics, such as pediatric or multimorbid populations.

## Requirements

To run the RMarkdown script and reproduce the analysis, you will need the following:

- R version 4.2.3 (2023-03-15) and RStudio (optional: 2023.6.0.421)
- Required R packages: "dplyr", "kableExtra", "ggplot2", "ggpubr", "broom", "purrr", "gridExtra", "referenceIntervals", "refineR"

## How to Run the Analysis

1. Clone this repository to your local machine using `git clone`.

2. Open RStudio and set the working directory to the location where you cloned the repository.

3. Open the RMarkdown script "analysis.Rmd" in RStudio.

4. Install the required R packages by running the *setup* chuck:

```R
# List of required packages
required_packages <- c("dplyr", "kableExtra", "ggplot2",
                       "ggpubr", "broom", "purrr", "gridExtra", 
                       "referenceIntervals", "refineR")

# Check if each package is installed, and install it if missing
for (pkg in required_packages) {
  if (!require(pkg, character.only = TRUE)) {
    install.packages(pkg)
  }
}
```

5. Click on the "Knit" button in RStudio to run the RMarkdown script. This will generate the output file "Handout.html" containing the full script. If you have a LaTex distribution installed, you can render the "Handout.pdf"

## Analysis Results

You can view the results of the analysis by opening the knitted HTML file "Handout.html" in your web browser. Alternatively, you can view the analysis output directly on GitHub by clicking the link below:

<iframe src="Handout.html" width="100%" height="500px"></iframe>

## Data

The analysis utilizes part of the [HCV](https://doi.org/10.24432/C5D612) data set, provided by the UC Irvine Machine Learning Repository (CC BY 4.0 license). The modified data set contains laboratory test results of 615 potential blood donors. For each patient, the person's age (in years), sex (f,m) and measurements of 6 laboratory analytes are recorded. 

## License

This project is licensed under [CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/deed.en_GB)

## Contact

If you have any questions or feedback, feel free to contact me at <tobias.blatter@extern.insel.ch>.