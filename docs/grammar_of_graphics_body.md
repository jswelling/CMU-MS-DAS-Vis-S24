## The Grammar Of Graphics

... is an attempt to impose some structure on visualization, to make it
more than just a collection of subroutine calls and idioms.  It's been
through a few iterations, beginning with
[Graph-Theoretic Scagnostics](https://www.semanticscholar.org/paper/Graph-theoretic-scagnostics-Wilkinson-Anand/8bc9868fe6c936614f7f94b01757723e9ffaaa43)
by Wilkinson, Anand, and Grossman in 2005.

This led to a famous book, **The Grammar of Graphics**, by Leland Wilkinson.


This led to
[A Layered Grammar of Graphics](http://vita.had.co.nz/papers/layered-grammar.pdf)
by Hadley Wickham 
([reference](http://vita.had.co.nz/papers/layered-grammar.html)).  This is
basically a restructuring of Wilkinson's grammar.

There is a full book version:
[ggplot2: Elegant Graphics for Data Analysis](https://books.google.com/books/about/Ggplot2.html?id=bes-AAAAQBAJ&source=kp_book_description)


These were implemented in **R**, the programming language.  As a result,
this formalism isn't very Pythonic.  To translate to Python, one must
choose between Pythonic design and pure preservation of the grammar.


# ggplot2 is part of the [Tidyverse](https://ggplot2.tidyverse.org/)

"system for declaratively creating graphics, based on The Grammar of Graphics. You provide the data, tell ggplot2 how to map variables to aesthetics, what graphical primitives to use, and it takes care of the details"


ggplot2 embodies an important attempt to impose order and structure on
data visualization.  Its rigorous grammar makes it more predictable than
ad hoc visualization tools.

In practice, you don't have to engage in the theory explicitly to take
advantage of its flexibility and simplicity.


ggplot is over 10 years old and has over 100 registered
[extensions](https://exts.ggplot2.tidyverse.org/gallery/).  This
modularity is a great strength!


# ggplot2: Practical Strengths

* **multivariate data visualization**: <span class=smalltext>easily swap variables and visualize using color, shape, facet grid, line style, and so on (without changing the data itself)</span>
* **themes**: <span class=smalltext>change overall plot appearance (font, background color, labels, legends, etc) by selecting different themes</span>
* **summary statistics**: <span class=smalltext>including regression, curve fitting, rolling averages... </span>
* very readable plotting code <span class=smalltext>(if you think R is readable)</span>



*plotnine* is a Python implementation of ggplot2.  Compare with *seaborn*,
which is similar conceptually but more pythonic.  (More on seaborn later).



# Never Get Involved In A Land War In Asia


By
[Charles Minard  (1781-1870) (Public Domain)](https://en.wikipedia.org/wiki/Charles_Joseph_Minard)
[![Russia campaign of 1812](images/Minard.png)](https://en.wikipedia.org/wiki/Charles_Joseph_Minard#/media/File:Minard.png)


This graphic has become iconic, and the ability to reproduce it is often taken
as a test of a visualization tool.

See [Re-Visions of Minard](https://www.datavis.ca/gallery/re-minard.php)
for many examples.

There is a copy of the necessary data in our data directory.



Attempting Minard's Graphic Using *plotnine*<br>
![Minard's graphic reproduced using plotnine](images/minard_with_plotnine.png)



plotnine and seaborn are both built on matplotlib

You can use matplotlib routines to modify their output.  This is often
necessary for fine tuning.

