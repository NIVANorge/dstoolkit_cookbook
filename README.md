# "Cookbook" for the Data Science Toolkit

Useful scripts and notebooks for NIVA's Data Science Toolkit.

The easiest way to explore these examples is to **clone this repository to your JupyterHub** and **run the notebooks interactively**. 

## Accessing NIVA datasets (Nivadatabasen/Aquamonitor, data in nivacloud etc.)

 * **[Aquamonitor-Python](https://nbviewer.org/github/NIVANorge/Aquamonitor-Python/blob/main/examples/query_chem.ipynb)**. Query project-specific water chemistry data directly to Pandas dataframes using the Aquamonitor API
 
 * **[Aquamonitor-Python Excel download](https://github.com/NIVANorge/niva_datasci_toolkit/blob/master/dstoolkit_examples/tutorials/11_Download_Excel_file_from_AquaMonitor.ipynb)**. *Contributed by Roar Branden*. Aquamonitor-Python also provides options for downloading data in Excel format. 
 
 * **[AquamonitR](https://nbviewer.jupyter.org/github/NIVANorge/aquamonitR/blob/main/examples/query_chem.ipynb)**. Query project-specific water chemistry data directly to R dataframes using the Aquamonitor API (an R equivalent of the Aquamonitor-Python package) 
 
 * **[Direct access to Oracle using nivapy](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/oracle_example.ipynb)**. Create a direct connection to Nivabasen (NIVA's Oracle database instance) and execute your own queries. More flexible than Aquamonitor-Python or AquamonitR, but also more complicated
 
 * **[Direct access to databases using R](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/r_db_connections.ipynb)**. A rough notebook providing hints for setting up direct connections to Hub databases from R
 
 * **[Accessing FerryBox data using pyniva](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/pyniva_example.ipynb)**. *Contributed by Zofia Rudjord*. Query and plot FerryBox data from **nivacloud** using the **pyniva** API. A more extensive example from Dag Hjermann is [also available](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/pyniva_download_ferrybox.ipynb)
 
## External data sources

 * **[Accessing data in Vannmiljø](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/vannmiljo_api.ipynb)**. How to use functions in `nivapy` to query data directly from Vannmiljø.

 * See **Tutorial 4 (`04_Accessing_Data.ipynb`)** in the `dstoolkit_examples/tutorials` folder on the Hub itself for details of how to access data via Met.no's [Frost API](https://frost.met.no/index.html) and [Thredds server](https://thredds.met.no/thredds/catalog.html), as well as European data hosted by [Copernicus](https://cds.climate.copernicus.eu/cdsapp#!/search?type=dataset) (via the [cdsapi](https://cds.climate.copernicus.eu/api-how-to)).

 * **[Using NVE's Hydrological API](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/nve_hydapi_example.ipynb)**. Create an API key and query NVE data directly from the JupyterHub
 
 * **[Using NVE's Grid Time Series API](https://nbviewer.org/github/NIVANorge/catchment_processing_workflows/blob/main/notebooks/nve_gts_api_example.ipynb)**. The [Grid Time Series (GTS) API](http://api.nve.no/doc/gridtimeseries-data-gts/) provides the most up-to-date gridded weather and hydrology data available for **Norway**. It's part of [seNorge 2018](https://essd.copernicus.org/articles/11/1531/2019/) and offers daily data from 1957 to present with 1 km x 1 km spatial resolution. The GTS API includes a wide range of weather and hydrology variables and it's probably the best gridded historic data currently available *if your region of interest is entirely within Norway*
 
 * **[Using Met.no's Nordic Gridded Climate Dataset](https://nbviewer.org/github/NIVANorge/catchment_processing_workflows/blob/main/notebooks/met_ngcd_thredds_example.ipynb)**. Gridded precipitation and temperature (min, mean and max) data for **Norway, Sweden and Finland** are available from [Met.no's Thredds server](https://thredds.met.no/thredds/catalog/ngcd/catalog.html). The data have a daily time step (1971 to present) and a spatial resolution of 1 km x 1 km. Two variants are available: `Type1` (based on a residual kriging) and `Type2` (based on Bayesian spatial interpolation), which are part of seNorge v1 and seNorge v2, respectively. This means they are slightly older than the datasets availble via the GTS API (above), which is part of seNorge 2018 (see [here](https://github.com/metno/seNorge_docs/wiki) for more information)
 
 * **[Accessing ERA5-Land via Copernicus](https://nbviewer.org/github/NIVANorge/catchment_processing_workflows/blob/main/notebooks/era5land_cds_api_example.ipynb)**. [ERA5-Land](https://www.ecmwf.int/en/era5-land) is a **global** reanalysis dataset providing a consistent view of the evolution of land variables over several decades at an enhanced resolution compared to ERA5. The dataset has a resolution of 0.1 by 0.1 degrees and is available from the [Copernicus Climate Data Store (CDS)](https://cds.climate.copernicus.eu/#!/home) as either [hourly](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-land?tab=overview) data or aggregated using [monthly](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-land-monthly-means?tab=overview) averages. See the links for further details.
 
## GIS/spatial data

 * See **Tutorial 3 (`03_Basic_Spatial_Analysis.ipynb`)** in the `dstoolkit_examples/tutorials` folder on the Hub itself for a basic overview of spatial data analysis and visualisation
 
 * See **Tutorial 10 (`10_Working_With_netCDFs.ipynb`)** in the `dstoolkit_examples/tutorials` folder on the Hub itself for an introduction to netCDF processing

 * **[Introduction to querying spatial data via the DSToolkit](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/postgis_example.ipynb)**. Connecting to the JupyterHub's PostGIS database and exploring available datasets
 
 * **[Create GIS data package](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/create_gis_package.ipynb)**. Extract a list of layers for your area of interest and create a single data package that you can download for use in e.g. desktop GIS

 * **[Catchment delineation](https://nbviewer.org/github/NIVANorge/catchment_processing_workflows/blob/main/notebooks/catchment_delineation/04_catchment_delineation.ipynb)**. Delineate watersheds for outflow points in Norway based on Kartverket's national 10 m resolution DTM. Reduced resolution versions (20 m and 40 m) are also available for faster processing and will be suitable for many applications
 
 * **[Catchment processing](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/catchment_processing_example.ipynb)**. Query catchment boundaries from the Hub's PostGIS database and combine them with other vector and raster data sources
 
 * **[DEM processing](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/dem_processing.ipynb)**. Calculate hillshade, slope and aspect maps using GDAL. Explore terrain properties and extract data based on masks

## Statistics

 * See **Tutorial 2 (`02_Water_Quality_Time_Series.ipynb`)** in the `dstoolkit_examples/tutorials` folder on the Hub itself for examples of simple **non-parametric tests for trends** (Sen's slope and Mann-Kendall) using NivaPy

 * **[Estimating riverine fluxes using different methods](https://nbviewer.jupyter.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/estimating_river_fluxes.ipynb)**. NivaPy includes four methods for estimating riverine fluxes. This notebook uses a synthetic dataset to explore their properties
 
  * **[Simple linear regression](https://nbviewer.org/github/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/simple_linear_regression.ipynb)**. OLS and Sen's slope

## Miscellaneous

 * **[Authentication using GitHub](https://github.com/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/github_auth.md)**. Configure Git to access private GitHub repositories
 
 * **[Debugging in JupyterLab](https://github.com/jupyterlab/debugger/blob/master/examples/index.ipynb)**. A basic overview of the debugging console
 
 * **[Using the Python Language Server Protocol (LSP)](https://github.com/jupyter-lsp/jupyterlab-lsp/blob/master/examples/Python.ipynb)**. The LSP provides many useful features, including syntax highlighting and linting, auto-completion, tools for refactoring, documentation links etc. This notebook provides an overview of what's available 
 
 * **[Configure pylint](https://github.com/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/configure_pylint.md)**. Filter and control warning messages generated by pylint
