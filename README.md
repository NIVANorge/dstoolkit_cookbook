# "Cookbook" for the Data Science Toolkit

Useful scripts and notebooks for NIVA's Data Science Toolkit.

The easiest way to explore these examples is to **clone this repository to your JupyterHub** and **run the notebooks interactively**.

## GIS/spatial data

 * **[Basic introduction to querying spatial data via the DSToolkit](./notebooks/postgis_example.ipynb)**. Connecting to the database and exploring available datasets
 
 * **[Create GIS data package](./notebooks/create_gis_package.ipynb)**. Extract a list of layers for your area of interest and create a single data package that you can download for use in e.g. desktop GIS
 
 * **[Work with catchment data](./notebooks/catchment_processing_example.ipynb)**. Query catchment boundaries from the Hub's PostGIS database and combine them with other vector and raster data sources

## Data in nivacloud (FerryBox etc.)

 * **[Accessing FerryBox data using pyniva](./notebooks/pyniva_example.ipynb)**. *Contributed by Zofia Rudjord*. Query and plot FerryBox data from **nivacloud** using the **pyniva** API
