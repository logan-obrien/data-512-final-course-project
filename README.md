# data-512-final-course-project
## Project Info:
### Project Goal:
The goal of my overall project was to study the impacts of smoke on my assigned city, Richland, WA. 

### Data Sources:
- **'USGS_Wildland_Fire_Combined_Dataset.json'**: This is the primary source of data for the project and contains wildfire data. I downloaded it from https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81 as part of the 'GeoJSON Files.zip' file. Citation: Welty, J.L., and Jeffries, M.I., 2021, Combined wildland fire datasets for the United States and certain territories, 1800s-Present: U.S. Geological Survey data release, https://doi.org/10.5066/P9ZXGFY3.I am not sure what the usage policy for this data is, but I am assuming it is safe to use since Dr. McDonald instructed us to use it.

### API Documentation:
- US Environmental Protection Agency (EPA) Air Quality Service (AQS) API:
    - This API is used in the project to retrieve some AQI estimates for relevant wildfires.
    - Documentation: https://aqs.epa.gov/aqsweb/documents/data_api.html
    - Additional Information: https://www.epa.gov/outdoor-air-quality-data/frequent-questions-about-airdata
    - I am not sure what the license terms for using the API and data are, but again I assume it is safe to use for class purposes.

### Data Files:
**Intermediary Data Files:**
- **'relevant_fires.json'**: This file contains the subset of wildfire data that is within about 1250 miles from Richland, WA, and between 1963 and 2023. The geometry data provided in 'USGS_Wildland_Fire_Combined_Dataset.json' has been dropped as it is no longer needed. Instead, a 'distance_to_richland' attribute has been added which stores the results of a geometric calculation performed in my first Jupyter Notebook.
- **'relevant_fires_and_smoke_est.csv'**: This file contains the data from 'relevant_fires.json' after it has been converted to a csv. Additionally, it also contains a new column with my smoke estimate data. It contains 32 columns, so I won't bother to list them here.
- **'Annual_AQI_Average.csv'**: This file contains the annual AQI estimates that I retrieved and aggregated in my second Jupyter notebook. It contains two columns: the first is the year and the 2nd the corresponding average AQI estimate. 

### Source Code Notes:
- Part 1:
    - My source code for this part of the project is contained within three Jupyter Notebooks. They are the following:
        - 'Project Part 1 - Common Analysis-s1-Load and Process Data.ipynb'
        - 'Project Part 1 - Common Analysis-s2-Get-Smoke-est-and-AQI.ipynb'
        - 'Project Part 1 - Common Analysis-s3-Comparison-and-Visualization.ipynb'
    - You should be able to reproduce the results of my analysis by running these files in this order, with one important note. Due to the size of some of the data files (both data sources and intermeadiate files) these data files are stored within a data folder that is not included in my Github repository. Thus, you will have to create a directory named 'data' within your clone of my project repo and ensure the data files are stored there in order to run my notebook files.


* note: this file originated in https://github.com/logan-obrien/data-512-course-project and was built upon and modified into its current state to incorporate work from the extension plan