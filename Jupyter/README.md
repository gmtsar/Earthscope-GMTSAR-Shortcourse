## GMTSAR Jupyter Notebooks

## Example 1: Creating and Unwrapping an RADARSAT-2 Satelllite Interferogram

This demo will walk you through how to prepare, calculate, unwrap, and view an interferogram. We will be looking at volcanic activity in the Kilauea Caldera on the 
island of Hawaii, through the lens of the RADARSAT-2 satellite. The commands in this notebook follow the workflow present in the universal `p2p_processing.csh` script.

### Prerequisites

(1) Python, and specifically Jupyter notebooks, installed

(2) Most recent version of GMT (GMT v6.4) installed (see https://github.com/GenericMappingTools/gmt/blob/master/INSTALL.md )

(3) Most recent version of GMTSAR (GMTSAR v6.2) installed (see https://github.com/gmtsar/gmtsar/wiki/GMTSAR-Wiki-Page )

### Set Up 

#### RADARSAT-2 Dataset
To obtain the data for this notebook, visit and download: http://topex.ucsd.edu/gmtsar/tar/RS2_SLC_Hawaii.tar.gz .
Unzip this directory to access the data and supporting files. 

Note the `topo` directory already contains a file `dem.grd` that is needed for removal of the topographic phase.  There is a  web site http://topex.ucsd.edu/gmtsar that will generate a dem.grd file for a selected area based on the best available data (SRTM or ASTER).

#### Directory structure
To ensure that all commands in this notebook work properly, download and place the Jupyter notebook file `gmtsar_rs2_demo.ipynb` within the downloaded dataset directory (`RS2_SLC_Hawaii`).

### Note

If you find you are missing a python library (e.g. NetCDF4) when you run the first cells of this notebook, recall you can use

``` pip install NetCDF4 ```

to install the missing library.

