---
layout: page
title: Setup
---
## Set-up Instructions:

### Prerequirisite software:
1. Anaconda or Micromamba
2. Python 3.x (<=3.10) 
3. Jupyter Lab

On **Windows**, this setup uses **Anaconda prompt** to install the prerequisites for the course. Experienced users may opt for other options such as **Git Bash** or **Windows Subsystem for Linux**

## Installing Python Using Anaconda

If you want to instal Micromamba instead, please skip this and go to Option 2 below.

[Python][python] is a popular language for scientific computing, and great for
general-purpose programming as well. Installing all of its scientific packages
individually can be a bit difficult, however, so we recommend the all-in-one
installer [Anaconda][anaconda].

Regardless of how you choose to install it, please make sure you install Python
version 3.x (e.g., 3.7 is fine). Also, please set up your python environment at
least a day in advance of the workshop.  If you encounter problems with the
installation procedure, ask your workshop organizers via e-mail for assistance so
you are ready to go as soon as the workshop begins.

### Windows - [Video tutorial][video-windows]

1. Open [https://www.anaconda.com/distribution/][anaconda-windows] with your web browser.

2. Download the Python 3 installer for Windows.

3. Double-click the executable and install Python 3 using the recommended settings. Make sure that **Register Anaconda
   as my default Python 3.x** option is checked - it should be in the latest version of Anaconda. We also recommend that you make sure "Add Anaconda to my PATH environment variable" is selected.

### Mac OS X - [Video tutorial][video-mac]

1. Visit [https://www.anaconda.com/distribution/][anaconda-mac] with your web browser.

2. Download the Python 3 installer for OS X. These instructions assume that you use the graphical installer `.pkg` file.

3. Follow the Python 3 installation instructions. Make sure that the install location is set to "Install only for me" so
   Anaconda will install its files locally, relative to your home directory. Installing the software for all users tends
   to create problems in the long run and should be avoided.


### Linux

Note that the following installation steps require you to work from the shell.
If you run into any difficulties, please request help before the workshop begins.

1.  Open [https://www.anaconda.com/distribution/][anaconda-linux] with your web browser.

2.  Download the Python 3 installer for Linux.

3.  Install Python 3 using all of the defaults for installation.

    a.  Open a terminal window.

    b.  Navigate to the folder where you downloaded the installer

    c.  Type

    ~~~
    $ bash Anaconda3-
    ~~~
    {: .bash}

    and press tab.  The name of the file you just downloaded should appear.

    d.  Press enter.

    e.  Follow the text-only prompts.  When the license agreement appears (a colon
        will be present at the bottom of the screen) press the space bar until you see the
        bottom of the text. Type `yes` and press enter to approve the license. Press
        enter again to approve the default location for the files. Type `yes` and
        press enter to prepend Anaconda to your `PATH` (this makes the Anaconda
        distribution your user's default Python).

## Option 1 Setting up the workshop environment with conda

If Anaconda was properly installed, you should have access to the `conda` command in your terminal/anaconda prompt.

1. Test that it works by running the `conda` command in the terminal. You should get an output that looks like this:

    ```bash
    $ conda
    usage: conda [-h] [-V] command ...

    ```

2. Create the environment using the `conda create` command. It's possible to paste the following
code on the terminal/anaconda prompt:

    ```bash
    conda create -n geospatial -c conda-forge -y \
      python=3.10 jupyterlab numpy matplotlib \
      xarray rasterio geopandas rioxarray earthpy descartes xarray-spatial pystac-client python-graphviz

    ```
    
3. ```bash
    conda activate geospatial
    ```

    If successful, the text `(base)` in your terminal prompt will now read `(geospatial)` indicating that you are now in
    the Anaconda virtual environment named `geospatial`. The command `which python` should confirm that we're using the
    Python installation in the `geospatial` virtual environment. For example:

    ```bash
    % which python
    > /Users/your-username/anaconda3/envs/geospatial/bin/python
                                          ^^^^^^^^^^
    ```
    
    > ## IMPORTANT
    > If you close the terminal, you will need to reactivate this environment with `conda activate geospatial` to use the Python libraries required for the lesson and to start JupyterLab, which is also installed in the `geospatial` environment.
    {: .callout}
    

## Option 2 Using Micromamba

1. Install micromamba with
    - Mac: `curl micro.mamba.pm/install.sh | zsh`
    - Linux: `curl micro.mamba.pm/install.sh | bash`
    - Windows: https://mamba.readthedocs.io/en/latest/installation.html#windows

2. Open a new terminal window and type
  ```micromamba create -n geospatial -c conda-forge -y \
     python=3.10 jupyterlab numpy matplotlib \
     xarray rasterio geopandas rioxarray earthpy descartes xarray-spatial pystac-client python-graphviz
   ```
3. ```bash
    micromamba activate geospatial
    ```

    If successful, the text `(base)` in your terminal prompt will now read `(geospatial)` indicating that you are now in
    the  virtual environment named `geospatial`.
    
    > ## IMPORTANT
    > If you close the terminal, you will need to reactivate this environment with `micromamba activate geospatial` to use the Python libraries required for the lesson and to start JupyterLab, which is also installed in the `geospatial` environment.
    {: .callout}
    

## Option 3 Using Binder

Don't install anything. Just go to [this binder link](https://mybinder.org/v2/gh/caltechlibrary/geospatial-python/HEAD?urlpath=lab) in your web browser.
  	
# Download files

We'll use some files on day two. Download them and move then to a location where you can find them

- [brpgewaspercelen_definitief_2020_small.gpkg](https://figshare.com/ndownloader/files/37729413)
- [brogmwvolledigeset.zip](https://figshare.com/ndownloader/files/37729416)
- [status_vaarweg.zip](https://figshare.com/ndownloader/files/37729419)


[anaconda]: https://www.anaconda.com/
[anaconda-mac]: https://www.anaconda.com/download/#macos
[anaconda-linux]: https://www.anaconda.com/download/#linux
[anaconda-windows]: https://www.anaconda.com/download/#windows
[gapminder]: https://en.wikipedia.org/wiki/Gapminder_Foundation
[jupyter]: http://jupyter.org/
[starting-jupyterlab]: https://swcarpentry.github.io/python-novice-gapminder/01-run-quit/#starting-jupyterlab
[python]: https://python.org
[video-mac]: https://www.youtube.com/watch?v=TcSAln46u9U
[video-windows]: https://www.youtube.com/watch?v=xxQ0mzZ8UvA

{% include links.md %}
