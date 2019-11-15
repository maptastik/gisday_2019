# Drops of Jupyter

This repo contains notebooks and data from my presentation at Raleigh's GIS Day 2019.

You can run the notebooks on Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/maptastik/gisday_2019/master)

## For Windows users (If running locally)

If you get the error `RuntimeError: b'no arguments in initialization list'` when using `.to_crs()` then you may need to apply some fixes behind the scenes. Apparently there is an improper reference to the location of the projection definitions for PROJ/pyproj. 

Go to `C:<path to>\Continuum\Miniconda3\envs\<your environment>\Lib\site-packages\pyproj` and open `datadir.py`. If the last two parts of the path are `share\proj`, replace them with `Library\share`. You'll need to restart your environment after that. Some other suggestions are in this [Stack Overflow thread](https://stackoverflow.com/questions/55390492/runtimeerror-bno-arguments-in-initialization-list).