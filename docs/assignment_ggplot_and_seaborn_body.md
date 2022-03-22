### Working with ggplot and seaborn

This assignment has two parts, one using plotnine to experiment with the Grammar of Graphics
and the other using seaborn to examine some statistical data.  It should be possible to do
both in separate jupyter notebooks running the *generic_requirements.txt* environment.  Hand in
both notebooks.



### Task 1: Reproduce the Charles Minard visualization of Napoleon's march to Moscow using plotnine


#### Step 1: Import the data

In the data directory for this class you should find *ggplot2_minard_gallery.zip*, a zip file containing
the necessary data for the plot.  *README.ggplot2_minard_gallery* contains some additional hints.  Unzip
the data file and read in the individual text files.  This will give you several data arrays.


#### Step 2: Use plotnine to reproduce the plot.

Use "%matplotlib qt" if you can, so your plots go into separate windows and you can arrange them on your
display.


Hints:
* Hadley Wickham's paper *A Layered Grammar Of Graphics* (referenced in the lecture notes) contains almost
step-by-step instructions for how to do the graphs.
* You will need to do two separate graphs, one for the upper half and one for the lower half.  Once you have
them both set up, putting them next to each other reproduces the original graph reasonably well.


#### Step 3: There will be some fine tuning needed.

You don't have to exactly reproduce my results, but:
* I set the text size for the city names explicitly.
* I changed the 'breaks' for the 'survivors' aesthetic to get a better match to Minard's range of bar widths.
* I explicitly set the width of the temperatures plot based on the limits of the cities/troops plot.
* I stretched the display windows around so that they had about the same aspect ratios as in Minard's original.



### Task 2: Produce an informative scatterplot using seaborn.

There are two files in the class data directory, *california_counties.tsv* and
*covid_surge_offsets.tsv*.  The first contains information about the counties in California,
including their area and population.  The second contains the date offsets of the four COVID
wave peaks we saw earlier in the *covidcases_test.csv* dataset.


#### Step 1: Read in and merge the data.

Read in the county information and the surge offset information.  Use a Pandas "merge" operation
to merge the two datasets, matching the key "area" in the *covid_surge_offsets* dataset with
the key "name" in the *california_counties* dataset.


#### Step 2: Add a population density column.

Just divide the population of each county by its area in square miles.


#### Step 3: Create a scatterplot with seaborn.

Try plotting surge_offset_4 against the population density.  It's informative to
use different symbols for the counties that based on their "general_law_or_charter"
characteristic.

Use a log scale in the population_density direction to make the correlation clearer.