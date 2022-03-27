### Working With Maps

In this assignment we make a weather map and estimate
some travel distances.  This should all be done in one Jupyter
Notebook based on our 'generic' venv.



### Step 1: Imports and data

You will need:
```
import matplotlib.pyplot as plt
import pandas as pd
import geopandas as gpd
from pyproj import CRS
```



### Step 2: Datasets

You will need to read the following datasets in to Pandas DataFrames:
* snowstorm_PA.tsv
* PA_cities_counties.tsv
This will give you weather data for the snowstorm of Jan 16 2022.
Remember to use ```sep='\t'``` in your ```pd.read_csv``` commands.


You will need to read the following shapefile into a GeoPandas GeoDataFrame:
* tl_2021_us_county.shp
This one is available on Canvas, to avoid problems with large binary
files on github.



### Step 3: Copy in some utilities

Copy in the following functions from the *geopandas_experiments.ipynb*
notebook, for convenience:
* add_area_and_label_coords()
* plot_with_labels()
* calc_overall_centroid()



### Step 4: Set up an ortho projection for PA

Select the geometry for Pennsylvania from the GeoDataFrame.  The
FIPS code for PA is 42.

Set up an orthographic projection for PA, just as we did in
*geopandas_experiments.ipynb*.  Set the CRS for the GeoDataFrame.



### Step 5: Estimate some county-wide snowfall numbers

We are interested in the 'Expected Snowfall' values from the
snowfall dataset.  However, we only have that data for cities,
and we need to plot by counties.  You can get averages for
counties by:


* Merge the snowfall dataframe with the cities-and-counties dataframe,
using the city name as the merge key.  Note that there are many cities
for which we have no snowfall estimate, so there will be a lot of
missing snowfall data.
* Prune the resulting dataframe down to only the columns you need.


* Group the dataframe by county and take the mean.  This will handle
counties with more than one named city by averaging over their
snowfall estimates.

Now you should have a dataframe with county names and estimated
snowfall values.



### Step 6: Merge the snowfall data into the GeoDataFrame

Be careful to do the merge in such a way that counties with no
snowfall data stay in the GeoDataFrame, but with 'NaN' values
for 'Estimated Snowfall'.  We want to use those records to draw
the counties outside the snowstorm area.



### Step 7: Plot the map

The GeoPandas page for
[Mapping and Plotting](https://geopandas.org/en/stable/docs/user_guide/mapping.html)
describes how to handle missing data.  Use those features to make
sure the part of Pennsylvania the snowstorm missed appears in the
map!

Pick a color map and 'missing' color that looks reasonable to you.