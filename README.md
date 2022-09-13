# NC Barrier Island Road Networks

Analysis of NC barrier island road networks.

This set of notebooks is based heavily on an existing repository: https://github.com/envidynxlab/Networks_Barriers

and the resulting (OA) paper in Earth's Future: https://doi.org/10.1029/2021EF002581

The goals of this repository are to further analyze NC barrier islands:
- go beyond bathub flooding and use flooding based on event forecasts (existing ADCIRC model runs)
- incorporate other metrics beyond elevation (i.e., distance to coastline, fronting dune height, etc.)
- test with real time traffic logs

To reproduce the analysis, follow these steps

### Step 0: set up the environment

```
> conda create -n roads

> conda activate roads

> conda install -c conda-forge fiona gdal networkx osmnx requests scipy urllib3 zipp shapely rasterio geopandas pandas numpy matplotlib notebook tqdm -y
```
### Step 1: run [`getNCBarriers.ipynb`](./src/getNCBarriers.ipynb) to get the barrier shapefiles

### Step 2: run [`getNCCUDEM.ipynb`](./src/getNCCUDEM.ipynb) to get the elevation data (CUDEM)

### Step 3: run [`getExceedence.ipynb`](./src/getExceedence.ipynb) to get the water level data (NOAA)

### Step 4: run [`getRoads.ipynb`](./src/getRoads.ipynb) to get the road data (OSM)