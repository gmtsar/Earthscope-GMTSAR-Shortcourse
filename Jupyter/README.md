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

## Example 2: How to Download Sentinel-1 data and prepare it for processing

This demo will take you through the steps of:

(1) Searching for and downloading Sentinel-1 SLC data from the Alaska Satellite Facility website

(2) Obtaining the proper supporting files for data processing (e.g. orbit files, DEM grids)

(3) Preparing to process your Sentinel-1 images

(4) Processing your images

(5) Viewing and interpreting the interferogram (after processing is complete)

This workflow can be applied to any specific study area. Additionally, we refer you to other prepared GMTSAR examples (https://topex.ucsd.edu/gmtsar/downloads/), that have undergone steps (1), (2), and (3) already, so you can explore both other examples of Sentinel-1 data, as well as other examples using data from other SAR satellite sources.

