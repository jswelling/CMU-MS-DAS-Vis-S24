### Working with ggplot

In this assignment you will use plotnine to experiment with the
Grammar of Graphics.  It should be possible to do the assignment in a
jupyter notebook running the *generic_requirements.txt* environment.
It is also possible to do this in **R** of course, and please do so if
you would prefer.  When complete, hand in the notebook and an screen
capture image of your two graphs via Canvas.


The goal is to reproduce the Charles Minard visualization of Napoleon's march to Moscow using plotnine.



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

* Set the text size for the city names explicitly.
* Change the 'breaks' for the 'survivors' aesthetic to get a better
  match to Minard's range of bar widths.
* Explicitly set the width of the temperatures plot based on the
  limits of the cities/troops plot.  This is necessary so that the
  framing looks right when you line the two plots up.



#### Step 4: Make a screen capture including the two graphs

Stretch the display windows around so that they have about the same
aspect ratios as in Minard's original.  Do a screen grab to capture an
image of your two graphs lined up, and include that when you hand in
the assignment.
