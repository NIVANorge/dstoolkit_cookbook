# "Cookbook" for the Data Science Toolkit

Useful scripts and notebooks for NIVA's Data Science Toolkit.

The easiest way to explore these examples is to **clone this repository to your JupyterHub** and **run the notebooks interactively**. (Note that GitHub is sometimes very slow to render notebooks online, so if you see a message saying `Something went wrong` after clicking a link below, you can either try refreshing until GitHub catches up or just clone the repository and run the notebook interactively).

## GIS/spatial data

 * **[Basic introduction to querying spatial data via the DSToolkit](./notebooks/postgis_example.ipynb)**. Connecting to the database and exploring available datasets
 
 * **[Create GIS data package](./notebooks/create_gis_package.ipynb)**. Extract a list of layers for your area of interest and create a single data package that you can download for use in e.g. desktop GIS
 
 * **[Work with catchment data](./notebooks/catchment_processing_example.ipynb)**. Query catchment boundaries from the Hub's PostGIS database and combine them with other vector and raster data sources

## Data in nivacloud (FerryBox etc.)

 * **[Accessing FerryBox data using pyniva](./notebooks/pyniva_example.ipynb)**. *Contributed by Zofia Rudjord*. Query and plot FerryBox data from **nivacloud** using the **pyniva** API. A more extensive example from Dag Hjermann is [here](https://github.com/NIVANorge/dstoolkit_cookbook/blob/master/notebooks/pyniva_download_ferrybox.ipynb)

## Statistics

 * **[Estimating riverine fluxes using different methods](./notebooks/estimating_river_fluxes.ipynb)**. NivaPy includes four methods for estimating riverine fluxes. This notebook uses a synthetic dataset to explore their properties
