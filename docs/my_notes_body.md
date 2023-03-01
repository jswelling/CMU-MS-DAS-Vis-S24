# My Notes #

* Do all students have B2 accounts? How are they accessed?
 * They are out of B2 units- need to get more from Shawn?
* Do students run notebooks locally, or on B2/OpenAccess?
* Do students know javascript?
* Can students download and run something from git?


<!-- .slide: data-background="#ff0000" -->
## Color Change Demo ##
This is just a demo of how to change slide color
Note:
This is a note.


To Do:

* Reorganize and insert the Tableau classes
* Update the syllabus to include some details on topics


To Do 2:
* From last year:
 * Add details on how to do git clone step.
 * Add some force to the prereqs
 * Add a 'Please Install' for GraphViz
 * Add geopy to requirements_generic.txt
 * Add a lecture component for geopy


Class Calendar:

* March 14, 16: Block 1
* March 21, 23: Block 2
* March 28, March 30, April 4: Block 3
* April 6, 11: Block 4
* April 13: no class- Spring Carnival
* April 18, 20: Block 5
* April 25, 27: Block 6


Maps assignment update using geopy

This was originally suggested by Charlie Chen in S22.  This
approach assigns counties to many more of the snowfall locs
than the current method.

```
from geopy.geocoders import Nominatim
geolocator=Nominatim(user_agent="joel_learns_geopy")
county = []
for i in snow_df['Location']:
    loc = geolocator.geocode(i + ' Pennsylvania US')
    a = r', (.*?) County'
    if len(re.findall(a, str(loc)))>0:
        county_str = re.findall(a, str(loc))[0].split(" ")[-1]
    else:
        # Try without the suffix
        loc = geolocator.geocode(i)
        if len(re.findall(a, str(loc)))>0:
            county_str = re.findall(a, str(loc))[0].split(" ")[-1]
        else:
            county_str = ""
    print(i,": ",county_str)
    county.append(county_str)
```


First class March 15, last class April 28

13 classes in all (due to Spring Carnival)


1. class intro, Data Lives On Manifolds
2. why vis, using color
3. Marching squares, The Grammar Of Graphics.
4. Statistical Data, seaborn
5. seaborn 2
6. Maps
7. Now we need a web server!
8. Graphs
9. D3: TreeMaps, Sankey diagrams, etc
10. Tableau 1
11. Tableau 2
12. VisIt 1
13. VisIt 2 - visualization algorithms


### Assignments
1. matplotlib assignment (class 1)
2. grammar of graphics, seaborn (class 4)
4. maps (class 6)
5. Flask exercise happens in class
6. GraphViz (class 8)
7. Tableau (class 10 or 11?)
8. VisIt (class 12)


# LaTeX Math Example

A sample of LaTeX math, so I remember how to do it later:

`$$ J(\theta_0,\theta_1) = \sum_{i=0} $$`
