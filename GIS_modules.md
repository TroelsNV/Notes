## Installing various GIS modules and their subsequent use
Much of this documentation is built on the documentation made avaliable by [aleaf](https://github.com/aleaf). Thanks for sharing it  Andy!

First before installing any of the GIS packages below i recommend installing [Anaconda](https://www.continuum.io/). Anaconda can be installed for both python 2.7 and 3.6 (currently). It holds most of the python modules needed for scientfic computing.

Here it will be documented how various packages for managing, reading and writing GIS data can be downloaded and installed. Doing this directly for each module can be rather difficult because of external dependencies. But thanks to Christoph Gohlke's Unofficial Windows Binaries site (http://www.lfd.uci.edu/~gohlke/pythonlibs/) this has become much easier. Christoph has packed the python modules together with their library dependencies into binary ("wheel") files that can be installed using Python's pip package management system. This will be further detailed below.

First the various modules are described, their functionality and links to the documentation.

|  Module  |  Purpose  |  Dependencies  |  Unofficial binary  |  Documentation  |
|:---: |-----------|----------------|---------------------|-----------------|
| *gdal*   | python bindings for GDAL library | numpy | http://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal | https://pypi.python.org/pypi/GDAL and http://www.gdal.org/ | 
| *fiona*  | reads and writes shapefiles | gdal, six, cligj | http://www.lfd.uci.edu/~gohlke/pythonlibs/#fiona | http://toblerity.org/fiona/ |
| *rasterio* | manipulates rasters | gdal, affine, cligj (and click), enum34, numpy | http://www.lfd.uci.edu/~gohlke/pythonlibs/#rasterio | https://mapbox.github.io/rasterio/ |
| *shapely*| provides containers and operations for manipulating vector data (points, lines and polygons)|  |  	http://www.lfd.uci.edu/~gohlke/pythonlibs/#shapely | https://pypi.python.org/pypi/Shapely |
| *rasterstats* | summarizes raster data (e.g. zonal statistics) | gdal, rasterio, fiona, shapely and numpy | install using 'pip' | http://pythonhosted.org/rasterstats/ |
| *rtree* | spatial indexing to speed up large intersection operations |  | http://www.lfd.uci.edu/~gohlke/pythonlibs/#rtree | http://toblerity.org/rtree/ |
| *pyproj* | cartographic transformations | | http://www.lfd.uci.edu/~gohlke/pythonlibs/#pyproj | https://github.com/jswhit/pyproj |
| *descartes* | plotting functionality  |    |  instal lusing 'pip'  |  https://bitbucket.org/sgillies/descartes/  |  |
| *geopandas* | Integrates [pandas](http://pandas.pydata.org/) to allow spatial operations on geometric types | numpy, pandas, shapely, fiona, six, pyproj | install using 'pip' (http://geopandas.org/install.html) | http://geopandas.org/index.html |
| *pyshp* | pure python for reading and writing shape files | | install using 'pip' | https://pypi.python.org/pypi/pyshp | 

Most of the packages above can be installed using wheel files downloaded at the provided links. Once downloaded they can be installed using pip (provided with anaconda). using the following command:

>pip install <name of wheel file e.g. **GDAL‑1.11.3‑cp27‑none‑win_amd64.whl** for the GDAL 64bit package>

Note: GDAL must be installed prior to installing fiona and rasterio, and gdal, rasterio, fiona and shapely must be installed prior to installing rasterstats. After these other packages are installed, rasterstats can simply be installed from PyPl using pip.
