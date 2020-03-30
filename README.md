# Jupyter-RISE with an R kernel available

Jupyter-RISE+R: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/fomightez/Jupyter-RISE-R/master?filepath=index.ipynb)

RStudio: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/fomightez/Jupyter-RISE-R/master?urlpath=rstudio)

RShiny: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/fomightez/Jupyter-RISE-R/master?urlpath=shiny/bus-dashboard/)

Click a `launch binder` badge anywhere on this page to begin.

-----

Note this builds on the [Binder example for the RISE plugin for presentations](https://github.com/binder-examples/jupyter-rise) to add the R kernel as well. **No installation needed**. 


----

## How to use

This repo is designed as a guide for making repositories where both Jupyter-RISE and an R kernel work. Copy it as a template using the `Use this template` button and add in your own content. Don't forget to edit the code for the badges to point at your repository.

The default **notebook cells not optimized for a slideshow presentation at this time**. Specifically, the current visuals are not formatted to fit the slide. This is just a strarting point for now. 

-----



## About Jupyter-RISE

RISE allows you to quickly generate a live, interactive presentation from a
Jupyter Notebook that is connected to the underlying Kernel of the notebook.
Using a new feature for automatically launching
the RISE plugin when a notebook is opened, RISE can be used to share interactive
presentations that run in the cloud with Binder.
This repository demonstrates how to accomplish this.

To make your RISE presentation automatically-launch with it is open,
add an `autolaunch=true` configuration
parameter to a notebook's `livereveal` section in the
metadata. E.g.:

```
...
"livereveal": {
        "autolaunch": true
        }
...
```

When the notebook is launched, your
presentation will automatically begin.

See the [RISE Documentation](https://damianavila.github.io/RISE/)
for more information.

If you don't need the hide_code extension enabled along with Jupyter-RISE, you may be more interested in the [Binder example for the RISE plugin for presentations](https://github.com/binder-examples/jupyter-rise)


-----
## R and RStudio use

Binder supports using R and RStudio, with libraries pinned to a specific 
snapshot on [MRAN](https://mran.microsoft.com/documents/rro/reproducibility).

You need to have a `runtime.txt` file that is formatted like:

```
r-<YYYY>-<MM>-<DD>
```

where YYYY-MM-DD is a snapshot at MRAN that will be used for installing 
libraries. In this line, you can request a [specific 
version of R](https://github.com/jupyter/repo2docker/pull/772#issue-313426641). To do this list the version between the 'r' 
and the year, as in `r-3.6-2019-09-24`. Right now the default version of R is 3.6.

You also need a Python notebook file such as [this one](https://github.com/binder-examples/r/blob/master/index.ipynb).

You can also have an `install.R` file that will be executed during build, and can be used to install libraries.

Both [RStudio](https://www.rstudio.com/) and [IRKernel](https://irkernel.github.io/)
are installed by default, so you can use either the Jupyter notebook interface or
the RStudio interface.

This repository also contains an example of a Shiny app.

Last, note that if your Binder URL points to a folder, as in 

http://mybinder.org/v2/gh/binder-examples/r/master?urlpath=shiny/bus-dashboard/,

you will need (1) to put in the final slash in the URL, and (2) to avoid converted 
spaces-'%20'-in the URL, instead placing a hyphen.

**Note:** An alternative is to use the excellent [holepunch package for R](https://karthik.github.io/holepunch/articles/getting_started.html).


----

## Technical notes:

Jupyter-RISE works via BINDER as can be seen via [the OFFICIAL Binder example for the RISE plugin for presentations](https://github.com/binder-examples/jupyter-rise). This repo was made by combining that with the [R Binder examples repository](https://github.com/binder-examples/r) to add the R kernel as well. 

-----

Jupyter-RISE+R: [![Binder](http://mybinder.org/badge_logo.svg)](http://mybinder.org/v2/gh/fomightez/Jupyter-RISE-R/master?filepath=index.ipynb)
