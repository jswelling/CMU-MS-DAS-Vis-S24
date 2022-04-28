# Some Thoughts On Dashboards


What's a *dashboard*?  In the context of visualization, it's a summary.  It's described
as something the boss reads regularly to get an overview of how things are going.
I've never written anything like that.


Instead, let's use it to mean the summary you bring to your research group when new data
becomes available.
* It has a standard form.
* It describes some new experiment in the context of previous experiments.
* It tells the group what they need to know to decide on the next steps.

I've written *that* kind of dashboard several times.


An important rule of thumb:
* You are the only person who sees 90% of the vis you do.
* Of the remaining 10%, 90% is for your group.
* 1% of the time, the visualization will be shown to the world in a paper or at a conference.

The 'dashboard' is for the ~10% that is shown to your group.


So what should that sort of dashboard or summary be like?



Let's discuss in the context of a specific example- a fMRI brain imaging experiment.  A new group
of subjects have been scanned and analyzed.  What do we need to present, and what can be omitted?



### Guiding questions
The research group needs to know how the overall project is proceeding, and if anything unexpected
happened with this most recent set of subjects.


How do these subjects fit in to the larger group?
* Are they 'typical', or do they differ somehow?
* What fraction of the total subjects do they represent?
This suggests a scatter plot, or just a summary table.


How does the data look?
* What fraction had to be discarded, and (briefly) why?
* Were these experiments atypical in any way?
Sometimes the scanner doesn't work properly, sometimes the subjects fall asleep.
Probably bar charts here?


* What do the in-group results look like?

* How do they fit with the overall results?

For this fMRI experiment, this might be activation maps or charts of activation by brain area.



### What Not To Show

Some data should not appear at the top level.  People will want to *drill down* to see the details
in some cases.

An fMRI example: curves of head motion tracking.  Uncorrected head motion makes leads to bad data,
so people want to see the curves- but not at the top level.


Fancy controls and interface elements should probably not be used.
* They take up space.
* They are great to look at the first few times, but by the 10th or 20th meeting they are annoying.


If your group has a logo, show it but keep it small.



### In Summary...

What you show to your group (every week for maybe years!) should be:
* Informative but not distracting
* Uncluttered
* Built out of parts that obey the visualization principles we've learned.



Here is Rebecca Barber's presentation on dashboards.  She speaks in the context of the boss rather
than the research group, but the principles are the same.

[Becky Barber on dashboards](https://www.youtube.com/watch?v=gCChe_ACBio)