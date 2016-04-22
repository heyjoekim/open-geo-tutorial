Open Source Geoprocessing Tutorial
==================================

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title"></a>

Tutorial of basic remote sensing and GIS methodologies using open source software (GDAL in Python). Tutorial covers workflow to perform image classification using machine learning classifiers:

0. Introduction [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_0_introduction.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_0_introduction.html)]
1. The GDAL datatypes and objects [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_1_GDALDataset.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_1_GDAL.html)]
2. Your first vegetation index [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_2_indices.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_2_indices.html)]
3. Visualizing data [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_3_visualization.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_3_visualization.html)]
4. Vector data - the OGR library [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_4_vector.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_4_vector.html)]
5. Land cover classification [[Python](http://ceholden.github.io/open-geo-tutorial/python/chapter_5_classification.html)] [[R](http://ceholden.github.io/open-geo-tutorial/R/chapter_5_classification.html)]

# R Installation

The following R libraries will be needed for this tutorial:

- `raster`
- `rgdal`
- `sp`
- `randomForest`

Install them from within R as follows:

``` r
install.packages(c('raster', 'rgdal', 'sp', 'randomForest'))
```

# Python Installation

To run the Jupyter Notebooks (formerly known as IPython Notebooks) and complete the tutorial, you will need to install Python and the libraries used in the tutorials. This installation can be accomplished in many ways, but I will list the two most common approaches:

### conda

I recommend using the [Anaconda](http://conda.pydata.org/docs/) Python distribution to make installation of the tutorial dependencies less complicated. After [installing Anaconda or "miniconda" by following their instructions](http://conda.pydata.org/docs/install/quick.html), you can install the dependencies as follows:

``` bash
conda env create -f environment.yaml
source activate open-geo-tutorial
```

### pip

Assuming you already have Python installed, you could use the the Python package manager, [pip](https://en.wikipedia.org/wiki/Pip_(package_manager)), to install the dependencies.

Following "pip" convention, you can find all package requirements in the `requirements.txt` file. I would also recommend installing these packages into a virtual environment to avoid conflicts with existing versions of the required Python packages. To isolate these dependencies from the rest of your system, use [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html):

``` bash
# Create virtual environment to isolate dependencies
virtualenv venv
# Activate virtual environment
source venv/bin/activate
# Install dependencies
pip install -r requirements.txt
```

You will need to have GDAL installed for Python to build the drivers against. You may have the Python bindings already built as part of GDAL's installation process.
