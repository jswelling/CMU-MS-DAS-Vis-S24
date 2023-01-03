## A Slice Viewer Using imshow

This assignment involves modifying the *widgets_and_brains.ipynb*
notebook to display the colin27 dataset using the matplotlib 'imshow'
operation instead of contours.  The goal is to produce a better version of the final "application" that shows 3 sliders and 3 views.

You need to create a modified notebook that does the things described
below, and submit that notebook in the usual way.


### Step 1: Use imshow instead of contour

matplotlib.pyplot provides the imshow function, which displays an
image as an image rather than a contour plot.  It's much more natural
for this task than using contours was.  Google the function, and also
google 'imshow animation'.  You probably want to use the
*im.set_data()* method rather than any of the other image animation
methods that people describe.


### Step 2: Add Color Map Control

colormaps can be specified by name in the imshow() call, and there is an *im.set_cmap()* method as well.  Add an ipywidgets.Dropdown or other selection method, and provide three or more valid color map names.  For full credit on this bit you need to make the images redraw when the color map changes.

Colormap names can be found on the [matplotlib colormap
reference](https://matplotlib.org/stable/gallery/color/colormap_reference.html)
page.  Example name: 'viridis'.


### Step 3: Orient the images

Make whatever changes are necessary so that the top of the head is up,
the nose is horizontal, and the 'marker' bar we added to the dataset
appears on the left (the patient's right).


### Step 4: Right-handed or left-handed?

For each of the three views, consider the coordinate system you've
implemented.  The X direction is left-to-right in the image and the Y
direction is bottom-to-top.  The Z direction increases as you move the
slider toward higher slice numbers.

For each view, is the coordinate system left-handed or right-handed?
Write your answers in a markdown block at the end of your notebook.
