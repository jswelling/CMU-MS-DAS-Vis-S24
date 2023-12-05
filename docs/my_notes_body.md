# My Notes #

* Do all students have B2 accounts? How are they accessed?
 * They are out of B2 units- need to get more from Shawn?
* Do students run notebooks locally, or on B2/OpenAccess?
* Do students know javascript?
* Can students download and run something from git?


To Do:
* Add details on how to do git clone step. (fm last year)
* Add some force to the prereqs (fm last year)
* Add a 'Please Install' for Tableau


Class Calendar:

Class starts Tue Jan 16 and runs through April 25 with no break.
11AM - 12:20PM

* Jan 16, 18: Block 1
* Jan 23 (Tuesday): Block 1 colors, Block 2 contours and ggplot
* Jan 25 (Thursday): Block 2 seaborn 1
* Jan 30 (Tuesday): Block 2 seaborn 2
* Feb 1 (Thursday) Block 3 maps 1 ***needs geopy info*** ; please install GraphViz and Gephi
* Feb 6 (Tuesday): Block 3 maps 2, Block 4 web server
* Feb 8 (Thursday): Block 4 graphs (incl Brendan/Gephi)


Class Calendar 2:

* Feb 13 (Tuesday): Block 4 D3; please install Tableau
* Feb 15 (Thursday): Block 5 (Tableau); please install VisIt
* Feb 20 (Tuesday): Block 5 (Tableau) continued
* Feb 22 (Thursday): prev Block 6 (VisIt)
* Feb 27 (Tuesday): Block 6 (VisIt) continued
* Feb 29 (Thursday): ????


Maps assignment update using geopy

This was originally suggested by Charlie Chen in S22.  This
approach assigns counties to many more of the snowfall locs
than the current method.  This is Chen's regex-based method,
with minor mods.

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


<!-- .slide: data-background="#ff0000" -->
## Color Change Demo ##
This is just a demo of how to change slide color
Note:
This is a note.


