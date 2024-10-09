# crash-severity-model

## Project Overview
This project applies multiple regression methods to analyze pedestrian crash data in Massachusetts, focusing on predicting crash severity based on various explanatory variables such as pavement friction, ambient lighting, and driver behavior. The goal is to determine which factors are most significant in predicting crash severity and whether a categorical or ordinal classification method yields better predictive accuracy.

## Objectives
- **Categorization:** Compare different methods of categorizing crash severity.
- **Prediction:** Identify key factors contributing to pedestrian crash severity.
- **Modeling:** Use regression analysis to evaluate which variables significantly impact crash severity.

## Data
The data used in this project is **Massachusetts pedestrian crash data** from 2017-2019. It includes fields such as:
- Crash number (`crash_numb`)
- Maximum injury severity (`max_injr_svrty_cl`)
- Driver contributing circumstance (`drvr_cntrb_circ_cl`)
- Road surface conditions (`road_surf_cond_descr`)
- Road contributing circumstances (`road_cntrb_descr`)
- Traffic control devices (`traf_cntrl_devc_type_descr`)
- Ambient lighting conditions (`ambnt_light_descr`)

## Methodology
- **Model Type:** Ordinary Least Squares (OLS) regression was applied to model pedestrian injury severity.
- **Hypotheses Tested:**
  1. An ordinal scale for crash severity improves model accuracy compared to using a dummy variable.
  2. Driver behavior and external road conditions are more predictive of crash severity than crash characteristics.
- **Feature Selection:** Backwards elimination and statistical significance tests were applied to select the best-fitting variables.
- **Model Performance:** Regression diagnostics, including R-squared values, AIC/BIC, and residual analysis, were used to assess model performance.

## Results
- **Key Findings:** Variables such as pavement friction, ambient lighting, and traffic control devices had the most significant impact on injury severity. An ordinal scale for crash severity was found to be a better fit than a dummy variable.
- **Statistical Significance:** Most driver behavior variables were found to be less statistically significant compared to crash characteristics and environmental factors.

## Conclusion
The study suggests that ordinal categorization of injury severity provides better modeling outcomes. However, certain predictive variables like driver behavior do not contribute as strongly as expected, indicating a need for further refinement in future models. While multiple significant variables were found, the model could not fully capture the complexity of pedestrian injury outcomes.

## Dependencies
This project was written in R. The following libraries are used in this project:
- `gglm`
- `tidyverse`
- `dplyr`
- `ggplot2`
- `rmarkdown`
- `leaflet`
- `ggthemes`
- `DAAG`
- `stats`
- `stargazer`
- `readr`
- `magrittr`

## How to Run
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/pedestrian-crash-severity-modeling.git
    ```
2. Install required dependencies:
    ```bash
    ```r
    install.packages(c("gglm", "tidyverse", "dplyr", "ggplot2", "rmarkdown", "leaflet", "ggthemes", "DAAG", "stats", "stargazer", "readr", "magrittr"))
    ```
3. Run the main script to perform the regression analysis:
    ```bash
    pedestrian_severity_model.rmd
    ```
## Repository Structure
- `data/` : Contains the processed pedestrian crash data (note: original data should be accessed via MassDOT).
- `scripts/` :  R Markdown files used for exploratory data analysis and model development.
- `results/` A corresponding poster summarizing the project.

## References
1. Yannis, George, et al. "Vulnerable Road Users: Cross-Cultural Perspectives on Performance and Attitudes." ScienceDirect, 2020.
2. Crash Data Visualization Tool: [MassDOT IMPACT Portal](https://apps.impact.dot.state.ma.us/cdp/home)
