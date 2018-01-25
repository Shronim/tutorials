## Visualizing Pangaea-X-2017 data in Aladin

* [Authors](#authors)
* [Change log](#change-log)
* [Requirements](#requirements-and-dependencies)
* [Use case](#use-case)
* [Keywords](#keywords)
* [Summary](#summary)
* [Introduction](#introduction)
* [Steps](#steps)
* [References](#references)
* [Links](#links)

## Authors:

M. Minin

## Change log

| Version       | Author        | Notes  |
| ------------- |:-------------:| -----: |
| 0             | name          | test   |

* * *

## Requirements and dependencies
 Not applicable

* * *

## Use case
exoplanets TBA

## Keywords
* term 1
* term 2 

## Summary
TBA

## Introduction

## Steps
[comment]: <> (Please document steps, including some description, not only screenshots.)

### First step - Load basemap
1. Open Aladin
2. In the available data panel, unfold "Collections" > "Solar system" > "Earth" 
3. Double click on "Blue Marble Next Generation w/ Topography and Bathymetry"
4. Zoom out with mouse wheel
![1](https://raw.githubusercontent.com/epn-vespa/tutorials/master/Aladin-Earth-Analog/img/1_Aladin_Earth_Analog_small.png)

### Second step - send ADQL query to EPN1


(<img src="https://raw.githubusercontent.com/epn-vespa/tutorials/master/APIS-Tutorial/img/1_planetary_uv_observations.png " width="500" alt="Planetary UV Observations">  )


<img src="https://raw.githubusercontent.com/epn-vespa/tutorials/master/APIS-Tutorial/img/1_planetary_uv_observations.png " width="500" alt="Planetary UV Observations">  


![1](https://raw.githubusercontent.com/aprossi/vespa-test-tutorial/master/IMG/1.png)

* In the available data panel, unfold "Others" > "Table (by TAP)" > jacobsuni
* Right-click on any table, click "Load"
* Change the query to "SELECT TOP 10 * FROM pangaea_x_2017.epn_core", click "submit"
* Double click on the table to open it in the data explorer panel
* Hover over to view the footprint
* Click on "FoV" button in the s_region column to display footprint permanently
* Click on a button in the access_url column to open coverage
* Open properties, create new projection (under Astronometrical reduction)
* Open "by WCS header" and change values CRVAL1 to c1min, CRVAL2 to c2min.
Measure distance across the footprint, divide it by diagonal of xy: 
Pixel ang. size = distance/(sqrt(x^2+y^2))
I'm getting 0.30356, then convert it to decimal degrees and divide this value by 2.
I'm getting 4.2*10^-8.
Enter this value in CD2_2 and negative of this value into CD1_1 (CDx_x are elements of the transformation matrix). 
Now the pixture should fit the circle precisely.


* step description
![1](https://raw.githubusercontent.com/aprossi/vespa-test-tutorial/master/IMG/1.png)

### First step with sized image
<img src="https://raw.githubusercontent.com/aprossi/vespa-test-tutorial/master/IMG/1.png" width="200">

### Second step
* step description
* step description
![7](https://raw.githubusercontent.com/aprossi/vespa-test-tutorial/master/IMG/7.png)

[http://exoplanet.eu](http://exoplanet.eu)


## References

TBA + URL


## Links
e.g. to working mybinder version where relevant, repos, jupyter notebooks, desktop tools/plugins or alike.