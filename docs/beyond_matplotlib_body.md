## The world is full of graphics packages.

We are trying to impose some order on visualization beyond
"Here is a gallery of idioms. Plug in your data!"


One thread of ideas on this is the _grammar of graphics_.  It's been
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



plotnine and seaborn are both built on matplotlib

You can use matplotlib routines to modify their output.  This is often
necessary for fine tuning.

