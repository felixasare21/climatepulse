# West African Rainfall Intelligence System

A Jupyter Notebook for exploring and visualising monthly rainfall over West Africa from 1901 to 2022, using the CRU TS gridded climate dataset. It produces static maps, anomaly maps, a regional time series, and animated and interactive rainfall maps.

## What the notebook does

1. **Loads the data.** Opens the CRU TS 4.07 monthly precipitation dataset with `xarray`.
2. **Subsets West Africa.** Selects latitude 4°N to 20°N and longitude 20°W to 20°E.
3. **Maps rainfall.** Plots a single-month precipitation map with coastlines and country borders (Cartopy).
4. **Computes climatology.** Calculates the long-term mean rainfall at every grid cell and maps it.
5. **Computes anomalies.** Subtracts the climatology from each month to show wetter and drier than average conditions, on a diverging red-blue scale.
6. **Plots regional mean rainfall.** Averages over the whole region to show the time series from 1901 to 2022.
7. **Builds an animation.** Creates a month-by-month rainfall animation with Matplotlib's `FuncAnimation`, rendered inline as HTML.
8. **Builds interactive maps.** Uses HoloViews, GeoViews and hvPlot to create maps with a time slider for both rainfall and anomalies.

## Data

This project uses the **CRU TS v4.07** monthly precipitation dataset from the Climatic Research Unit, University of East Anglia:

- File used: `cru_ts4.07.1901.2022.pre.dat.nc`
- Variable: `pre` (precipitation, mm per month)
- Coverage: global, 1901 to 2022, 0.5° resolution

The data file is **not included** in this repository because of its size. Download it from the [CEDA Archive](https://catalogue.ceda.ac.uk/uuid/e0b4e1e56c1c4460b796073a31366980) (search for "CRU TS 4.07") and place it in the same folder as the notebook.

## Requirements

- Python 3.9 or later
- xarray
- netCDF4
- numpy
- matplotlib
- cartopy
- plotly
- holoviews
- geoviews
- hvplot
- bokeh

Install everything with:

```bash
pip install xarray netCDF4 numpy matplotlib cartopy plotly holoviews geoviews hvplot bokeh
```

Cartopy and GeoViews can be easier to install with conda:

```bash
conda install -c conda-forge xarray netcdf4 numpy matplotlib cartopy plotly holoviews geoviews hvplot bokeh
```

## How to run

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
   cd YOUR-REPO
   ```
2. Download the CRU TS 4.07 precipitation file (see **Data**) into this folder.
3. Install the requirements.
4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook West_African_Rainfall_Intelligence_System.ipynb
   ```
5. Run the cells from top to bottom.

## Notes

- The animation and interactive map cells process all 1,464 months, so they can take a while to run and produce large outputs.
- The interactive HoloViews and hvPlot maps only work in a live Jupyter session. They will not display interactively when the notebook is viewed on GitHub.

## Data citation

Harris, I., Osborn, T.J., Jones, P., and Lister, D. (2020). Version 4 of the CRU TS monthly high-resolution gridded multivariate climate dataset. *Scientific Data*, 7, 109. https://doi.org/10.1038/s41597-020-0453-3

## Author

YOUR NAME

## License

Add a license of your choice, for example MIT. See [choosealicense.com](https://choosealicense.com/).
