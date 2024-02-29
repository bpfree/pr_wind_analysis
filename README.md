# Puerto Rico
This GitHub repository hosts recreated wind speed data (160 meters) for Puerto Rico. Associated code obtains wind data for Puerto Rico from NREL's [Wind Integration National Dataset (WIND) Toolkit](https://www.nrel.gov/grid/wind-toolkit.html) to recreate the 20-year mean wind speed dataset contained in the [Puerto Rico 100 report](https://www.nrel.gov/docs/fy24osti/88615.pdf). For more information about the PR100 study, this the official [website](https://pr100.gov/).

#### Good resources for how to obtain and manipulate the NSRDB data are contained in NREL's [Github repository](https://github.com/NREL/hsds-examples) for HSDS:
* [Notebook examples](https://github.com/NREL/hsds-examples/tree/master/notebooks)
    *  https://github.com/NREL/hsds-examples/blob/master/notebooks/01_WTK_introduction.ipynb
    *  https://github.com/NREL/hsds-examples/blob/master/datasets/WINDToolkit.md

#### For information regarding the hy5pyd package, this is the [Github repository](https://github.com/HDFGroup/h5pyd)

#### Data
* NREL hosts wind data for Puerto Rico within its Wind Toolkit ([website](https://www.nrel.gov/grid/wind-toolkit.html), [GitHub](https://github.com/NREL/hsds-examples/blob/master/datasets/WINDToolkit.md)). These data exist at 5 minute increments across a year between 2001 and 2020.

#### Access
Data can get obtained through NREL's API. For information specific to the PR100 5-minute dataset, visit this [page](https://developer.nrel.gov/docs/wind/wind-toolkit/wtk-pr100-5min-download/).

#### Notes
Be aware that the raw data, due to their sizes, are not hosted on GitHub. They are approximately 8GB in size. The associated code provides the template for how to download any data hosted by NREL. See available datasets [here](https://github.com/NREL/hsds-examples/blob/master/datasets/WINDToolkit.md). This [documentation](https://www.nrel.gov/hpc/eagle-wind-dataset.html) provides context on the data.

#### Methodology
Basic framework of the methods are as follows:
(1) Connect to NREL server
(2) Inspect the files (.h5) in the server
(3) Open the files from the server (using h5pyd package)
(4) Inspect metadata and attributes (specifically the scale factor)
(5) Pull the wind speed data (160 m) for each year (2001 - 2020) and divide by the scale factor (i.e., 100)
(6) 
