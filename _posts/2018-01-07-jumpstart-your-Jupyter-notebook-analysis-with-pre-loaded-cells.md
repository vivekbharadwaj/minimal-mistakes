---
title: "Jump-start Jupyter Notebook With Pre-Loaded Cells"
excerpt: "Because Hello World posts are so cliche."
layout: single
header:
    overlay_image: /assets/images/jupyter-ecosystem-overlay.jpg
    overlay_filter: 0.2
categories:
  - data science
tags:
  - Jupyter notebook
  - data science tools
  - python
author: "Vivek"
date: "7 January 2018"
hidden: false
---

Since its inception in 2014, the [Jupyter ecosystem](http://jupyter.org) along with the Jupyter notebook, has become an integral part of several data scientists’ toolbox. If you’re a Python data scientist like me, the first couple of lines of code in your jupyter notebook is invariably importing all the packages, libraries and custom utilities that you may need for your analysis. When I think about it, "importing" a capability or scikit-learn model almost always makes me feel like Neo from The Matrix.

![Python flying xkcd]({{ site.url }}{{ site.baseurl }}/assets/images/python-flying-xkcd.png)

(image taken from: xkcd)

However, it becomes a chore when I need to Ctrl-C+Ctrl-P nearly twice a day, every day. This is exactly the kind of nitty-gritty stuff that data scientists go through, which somehow doesn't seem to get coverage in the hype machine.

Wouldn’t it be great if each time you initialise your jupyter notebook, it would automatically pre-load a couple of lines of admin and import code so that you can do your thing from the get-go?

There was an excellent conversation on [this github issue](https://github.com/jupyter/notebook/issues/1451) about incorporating this feature. Based on the conversation above, this post is a quick step-by-step guide to create a pre-load feature as a reproducible Jupyter notebook extension in a way that is reproducible from one computer to another.

1) If you're running virtual environments using conda or virtualenv (I use anaconda and strongly recommend this for future proofing your code. But more on this some other time.), activate your viritual environment. Otherwise, stick to your base python. 
2) Check if you have the [Jupyter notebook extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions) package  installed . If not, the most straightforward way to install extensions is to use pip: 
```
pip install jupyter_contrib_nbextensions
```
3) Find the path where notebook extensions are installed inside your virtual environment or base python:
```
jupyter --path
```
4) go to the data directory specific to your environment. If you're on a mac and are on base python, this will be in the {/Library/Jupyter} directory under your home directory. On windows machines, I'm given to understand that this will be under your home directory under {\AppData\Roaming\jupyter\}. If the nbextensions step went smoothly, you should see a directory called 'nbextensions' here
5) Create a directory for your custom notebook extension to preload import code inside the nbextensions directory:
```
mkdir preload_import_code
```
6) Create a new file called 'main.js' and copy this custom js code inside the 'preload\_import_code' directory:
```
define([
    'base/js/namespace'
], function(
    Jupyter
) {
    function load_ipython_extension() {
      if (Jupyter.notebook.get_cells().length===1){
   //change this piece of code to what you want
        Jupyter.notebook.insert_cell_above('code', 0).set_text("import os, sys; sys.path.append('/Users/Vivek/DataScience')\nimport matplotlib\n%matplotlib inline\n\nfrom ds_utils.jupyter_notebook_imports import *\nfrom ds_utils.blob_utilities import df_to_sqldb, df_to_blob,set_up_blob_connection, df_to_blob\nfrom ds_utils.sql_database_utilities import parse_sql_query_from_arbitrary_script, execute_sql_queries, source_raw_data_from_sql, execute_sql_script");
      }
    }
    return {
        load_ipython_extension: load_ipython_extension
    };
});
```
7) Once the main.js file has been created, your notebook extension is now ready to use. You'll also need to enable it, which tells the notebook interface to load it. To do this, use the jupyter subcommand:
    jupyter nbextension enable preload_import_code/main
```
jupyter nbextension enable preload_import_code/main
```
8) You're good to go! When you fire up a new Jupyter notebook instance, the notebook extension checks for the number of cells and adds the custom cell block initially. So this code block will not be added to existing Jupyter notebooks.

![Preload jupyter notebook cells]({{ site.url }}{{ site.baseurl }}/assets/images/preload-notebook-utilities.png)

In my case, I have all my python imports as well as scikit-learn and nltk methods declared inside the jupyter\_notebook\_imports custom utility. 

Hope this helped. Feel free to let me know if you face any issues with the set-up. Happy coding!


