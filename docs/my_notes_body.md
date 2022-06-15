# My Notes #

* Do all students have B2 accounts? How are they accessed?
 * They are out of B2 units- need to get more from Shawn?
* Do students run notebooks locally, or on B2/OpenAccess?
* Can I find my copy of Tufte?


From last year:

* Add details on how to do git clone step.
* Add some force to the prereqs
* Add a 'Please Install' for GraphViz
* Add geopy to requirements_generic.txt
* Add a lecture component for geopy


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
3. ipywidgets, marching squares
4. The Grammar Of Graphics.
5. Statistical Data, seaborn
6. seaborn 2
7. Maps
8. The Awful Exercise?
9. Graphs
10. D3: TreeMaps, Sankey diagrams, etc 
11. VisIt 1
12. VisIt 2
13. Guest lecture? Storytelling and dashboards?


### Assignments
1. matplotlib assignment (class 1)
2. ipywidgets assignment (class 3)
2. grammar of graphics
3. seaborn
4. maps
5. The Awful Exercise
6. VisIt


# LaTeX Math Example

A sample of LaTeX math, so I remember how to do it later:

`$$ J(\theta_0,\theta_1) = \sum_{i=0} $$`
