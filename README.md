# Using Linear Statistical Modelling to Predict New York Taxi Prices

# Dependencies
- Language: Python 3.8.3
- Packages / Libraries: pandas, sklearn, statsmodels, folium, numpy, fiona, matplotlib.pyplot, seaborn, geopandas, shapely, pylab, scipy

# Datasets
- NYC TLC: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page. The Download notebook in the code folder downloads the first 6 months data from 2018 and 2019 for both green and yellow taxis.
- Crash dataset: Downloaded from NYC OpenData - https://data.cityofnewyork.us/api/views/h9gi-nx95/rows.csv?accessType=DOWNLOAD
- Weather dataset: Downloaded from the National Centers for Environmental Information. The data is provided in the raw data folder. It can be requested from https://www.ncdc.noaa.gov/cdo-web/datasets/LCD/stations/WBAN:14732/detail


# Directory
- `raw_data`: Contains the raw weather data files and TLC taxi zones. The car crash dataset and taxi datasets are to be added here.
- `preprocessed_data`: Contains the TLC taxi zones with their geometry changed to have latitude and longitude.
- `plots`: Contains plots output by the notebooks
- `code`: Notebooks for preprocessing the data, joining all the data together, creating plots and statistical models
- `deprecated`: Old code

# How To Run
- Firstly, run the download notebook and manually download the car crash data. The weather data is already in the raw_data folder
- Then, run the preprocessing notebookes to clean the raw_data, pickles will be output to the preprocessed_data folder. The fix_zones notebook can be run, but the output is already in the preprocessed_data folder
- Run the data_joining notebook to merge the data together, a pickle will be output for both 2018 and 2019 data with all relevant features
- The statistical_modelling and geospatial_mapping_and_plotting notebooks can then be run, using the pickles created in the previous step to load in the data.
- The final report is the file 'NYC_taxi_report'
