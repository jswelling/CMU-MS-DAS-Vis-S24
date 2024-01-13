## You May Need Multiple Python Virtual Environments For This Class ##

This class uses a lot of notebook-based visualization tools.  The
tools used in this course generally work well together, but they can
be finicky about which exact versions are used.

Some others libraries (like ipywidgets and plotly) will not work
properly in the presence of libraries used in this class to the best
of my knowledge.


This can happen with any set of Python packages, but it's more common with
packages that try to do clever things with the Jupyter Notebook screen
environment.  That means it may happen more in this Vis class than in your
other classes.

The solution is to be prepared to use multiple Python virtual environments.




## Some Things Fail In JupyterLab!

I've seen some things (like ipywidgets) work in *jupyter notebook* but
fail in *jupyter-lab*.  If I don't use JupyterLab for something, this may
well be the reason.  YMMV.



## How To Generate A Venv From Requirements

Different parts of the class use different versions of libraries.
We specify these with *requirements.txt* files.  I'll tell you which is
appropriate for any given task.  You'll see them in the GitHub repo.

Suppose we are using the requirements file for *someproject* .  We decide to
call this venv **someproject_env** .
```
$ conda create --name someproject_env python=3.8.1 pip
$ conda activate someproject_env
```


Now the new venv exists and is active.  Load the requirements into it:
```
$ pip install -r requirements_someproject.txt
```
and let Jupyter know that this environment can be run as a kernel:
```
$ python -m ipykernel install --user --name=someproject_env
```


Now you should be able to start up a Jupyter notebook.
```
$ jupyter notebook
```
Don't forget to use or switch to the kernel venv you just installed!