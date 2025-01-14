## Cassini T117 Titan Fly by

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

V. Genot et al.

## Change log

| Version       | Author        | Notes                                                                |
| ------------- |:-------------:| --------------------------------------------------------------------:|
| 1             | Gangloff      | Initial version modified to handle the latest version of VESPA portal|

## Requirements and dependencies
 Not applicable

## Use case
Search and display data around a Titan fly-by with VESPA

## Keywords
* 3DView
* TopCat

## Summary
For this use case, we use 3DView and another tool called TopCat to display data searched by 3DView among VESPA services.
We want to search for data provided by VESPA around a Titan flyby by the CASSINI spacecraft

## Introduction

The Titan fly by is described below (source PDS):

<img src="./img/T117atPDS.png" alt="T117atPDS">

## Steps

### First step
Start 3Dview : goto http://3dview.cdpp.eu and click on the **Launch 3DView** button, save the file as launch3dview.jnlp and run the application

<img src="./img/3DviewLaunchPage.png" alt="3DviewLaunchPage">

### Next step
In the desktop bar, select File/New to open a new 3D scene

<img src="./img/open3Dscene.png" alt="open3Dscene">

### Next step
With the File/Manage scene menu,create a scene with Titan as central body, CASSINI as spacecraft and TIIS as coordinate system
from 2016-02-16T21:00:00 to 2016-02-17T03:00:00

<img src="./img/manageScene.png" alt="manageScene">

### Next step
Select the VESPA option in the Science Menu

<img src="./img/sciencemenu.png" alt="sciencemenu">


This opens the VESPA pop-up window,with Target,StartTime and StopTime already selected from the scene.

<img src="./img/EPNTAPWindow.png" alt="EPNTAPWindow">

### Next step
Launch the animation and stop it at about 23:16,and click on the Select Region button to add a new search keyword.


<img src="./img/launchAnimation.png" alt="launchAnimation">

<img src="./img/time.png" alt="time">

## Next step
click on the Select Region button to add a new search keyword. The following pop-up window is opened.

<img src="./img/selectRegion1.png" alt="selectRegion1">

## Next step
Then select a region 

<img src="./img/selectRegion2.png" alt="selectRegion2">

## Next step
To increase the number of possible responses, change the start date to
2010-02-16T21:00:00  and click on Search

The list of services is displayed in the left part of the window. The name of each service is displayed with the corresponding
number of results.

<img src="./img/ListOfServices.png" alt="ListOfServices">

## Next step
Click on titan to display the results of this database.

<img src="./img/titanResults.png" alt="titanResults">

## Next step
Launch TopCat. This will automatically start the SAMP HUB hosted by TopCat.Right click on a raw displays several options
depending on the data format.Select send via SAMP to TopCat.
This option is available for data of mime type equal to application/x-votable+xml only.

<img src="./img/sendToTopCat.png" alt="sendToTopCat">

## Next step

The table is loaded by TopCat, and visible in the Table List after a few seconds. Open the plane plotting window to display the contents of the table.

<img src="./img/topcatView.png" alt="topcatView">

## Next step

In the plane plot window, Select temperature on X-axis and altitude on Y-axis.

<img src="./img/planePlotting.png" alt="planePlotting">


