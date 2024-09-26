# Analysis and Extraction of Socio-economic Indices from the Standard Demographic and Health Surveys

## Overview
In this project, we developed a data pipeline to analyze and extract socioeconomic indices that characterize the living standards of families in Egypt, utilizing the 2014 raw data from the Standard Demographic and Health Surveys (DHS) by [the DHS Program](https://www.dhsprogram.com/). The pipeline begins by collecting raw survey data, narrowing the scope of target variables, and converting the data into a CSV format for analysis. We then preprocess the data, transforming it into a format suitable for multivariate analysis. This involves Exploratory Data Analysis (EDA) to identify and remove irregular data, such as outliers and highly skewed variables. <br>
Subsequently, we apply advanced statistical techniques, including Principal Component Analysis (PCA), Factor Analysis, and cluster analysis, to reduce dimensionality and extract meaningful socioeconomic indices. These indices provide a comprehensive view of household living standards and help summarize complex data patterns effectively. <br>
The complete description of the project can be found [Here](https://medium.com/@omarhokudai/analysis-and-extraction-of-socio-economic-indices-from-the-standard-demographic-and-health-surveys-b1cca755377a)

## Prerequisites
### Standard Demographic and Health Surveys (DHS)
In this investigation, we utilize the 2014 Standard Demographic and Health Surveys (DHS) data from the DHS Program, with Egypt as the target country. Access to the data requires permission, and end users are advised to visit [the DHS Program website](https://www.dhsprogram.com/) to apply for the necessary permissions. Once approved, users can place the zipped folder of survey data in the `./user_input` directory, where it will be processed by the current data pipeline.

### Jupyter Notebook
In this project, we used Jupyter Notebook to develop and execute the analytical pipeline. End users are advised to refer to the [Installing Jupyter](https://jupyter.org/install#jupyterlab) guide to properly install and set up Jupyter Notebook for their environment.
### Python Libraries
In this project, we utilize the following third-party libraries to implement the analytical pipeline:
- **pandas** and **numpy:** For data manipulation and preprocessing.
- **seaborn** and **matplotlib:** For data visualization.
- **scipy**, **scikit-learn**, and **factor_analyzer:** To implement advanced statistical techniques, including Principal Component Analysis (PCA), Factor Analysis, and cluster analysis.

### Setup:

1. **Create Project Home Directory:**
   Create a directory to act as the working directory for the project:
   ```bash
   $ mkdir my_project
   $ cd my_project
   ```

2. **Clone the Repository:**
   Clone the current project repository:
   ```bash
   $ git clone <repository-url>
   ```

3. **Repository Structure:**
   The structure of the cloned repository is as follows:
   ```bash
   my_project
   ├── main                # Directory for the Jupyter notebooks used in the pipeline
   ├── resources           # Directory created by the program to store input/output data
   ├── user_input
   │   ├── xx.zip          # Zipped folder containing the survey data
   │   ├── EG_selected_variables_id.csv  # File with selected variables (columns) for analysis
   ├── requirements.txt    # File listing required Python third-party libraries
   ├── README.md           # This README file
   ```
## Using the Notebooks
The project is organized into the following Jupyter notebooks:

- **`main/01_collect_data.ipynb`**: Collect and extract input data from the raw survey data files.
- **`main/02_preprocess_data.ipynb`**: Cleanse and transform input data into a format suitable for subsequent analysis.
- **`main/03_preliminary_analysis.ipynb`**: Perform exploratory data analysis (EDA), including standardization and the removal of irregular data, such as outliers and highly skewed variables.
- **`main/04_multivariable_analysis.ipynb`**: Apply advanced statistical techniques, such as Principal Component Analysis (PCA), Factor Analysis, and cluster analysis, to reduce dimensionality and extract meaningful socioeconomic indices.