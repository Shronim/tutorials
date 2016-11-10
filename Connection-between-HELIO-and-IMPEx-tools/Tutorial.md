#Connection of Helio Tools, AMDA/IMPEx & 3DView/IMPEx: CME impact on Venus and Earth


[Authors](#Authors)  
[Change Log](#Change Log)  
[Introduction](#Introduction)  
[Steps](#Steps)  
&ensp;&ensp;&ensp;&ensp;[First Step](#1)  
&ensp;&ensp;&ensp;&ensp;[Second Step](#2)  
&ensp;&ensp;&ensp;&ensp;[Third Step](#3)  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[Verification of CME impacts on Venus and Earth](#3a)  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[The Venus Impact](#3b)  
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[The Earth Impact](#3c)  
&ensp;&ensp;&ensp;&ensp;[Fourth Step](#4)  
[References](#5)




<h2 id="Authors">Authors</h2>
To be updated...


<h2 id="Change Log">Change Log</h2>

First converted by [Keyuan Yin](https://github.com/megadiesel705) on 10th, Nov. 2016 from Vespa tutorial site.

<h2 id="Introduction">Introduction</h2>
This tutorial gives an example of the interconnected use of HELIO Tools, AMDA/IMPEx functionality and 3DView/IMPEx functionality. The AMDA/IMPEx, as well as the 3DView/IMPEXpart show new features in AMDA, which were implemented within the IMPEx FP7 project, i.e. the possibility of plotting simulation runs for given spacecraft side by side with observational data.  

<h2 id="Steps">Steps</h2>
<h3 id='1'>First Step</h3>  

Searching for events in [Helio](http://hfe.helio-vo.eu/Helio/). Using *Search Events* button to open new search.   

![Search Event Button](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/1_Search_Button_Icon.png)  

Example(with picture attached):  *Time Range*:  
20120610Z00:00:00 - 2012-06-15Z00:00:00    *Event Catalogue*:  
SOHO/LASCO CME Event List / pa_width>=270→ 1 CME  

![Input Example for Step 1](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/1_Factor_Input_Illustration.png)

<h3 id='2'>Second Step</h3>  

Extraction of time range → use as input for the Helio CME Forward PM  
**Longitude: 1  Width: 45  Speed:  977  
SpeedError: +/50**  
CME hits Earth, Venus, Pluto, Voyager1, New Horizons, Rosetta (see screenshot)
![Input Screenshot for Step 2](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/2_Input_Example_for_the_Helio_CME_Forward_PM.png)  

<h3 id='3'>Third Step</h3>  

Plotting data in AMDA Comparison of model data with insitu data on [this site](http://amda.cdpp.eu/).  

<h4 id="3a">a)  Verification of CME impacts on Venus and Earth</h4>  

● Open the Plot Manager in AMDA:Use the time range as received via HELIO and extend it properly, i.e. the CMEimpacts at Venus and Earth should be visible (e.g. 2012/06/15 15:00:00 2012/06/17 05:00:00)  
● The following parameters may be selected (see screenshot below):  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ VEXMAG data: Remote Data  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*(Observations)/VexMag@Graz/VEX/Vex_mag/MAG_VSO/MAG_VEX_VSO]*  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ WINDMFI data: Local Data/WIND/MFI/mfi_high/b_gse  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ CLUSTER1FGM data: Local Data/fgm_5vps/b_gse  

● Plot the data (see screenshot below). One can zoom into different time intervalsto get a more detailed view on the data at Venus and Earth.  

Selected Parameters Illustration:  
![Parameter Input for AMDA Plot](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/3_Plotting_data_in_AMDA_Parameter_Input.png)  


Output Plot:  
![Parameter Output for AMDA Plot](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/3_Plotting_data_in_AMDA_Plot_Output.png)  

<h4 id="3b">b)  The Venus Impact</h4>

● Prepare another plot via the Plot Manager for the time interval of the CME impactat Venus (e.g. 2012/06/15 19:00:00 2012/06/16/ 13:00:00).  
● Compare observational data by VEX MAG with FMI HYB simulation run data (please be aware that the FMI HYB simulation runs are by now only for quiet solar wind conditions. The runs are within a range around Venus of x=[3,3],y=[4,4],z=[4,4]  Venus radii). Use the following data:  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ VEXMAG data: Remote Data&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(Observations)/VexMag@Graz/VEX/Vex_mag/MAG_VSO/MAG_VEX_VSO  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ Via Create/Modify parameter one can also create the absolute  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;value of the observed magnetic field (see screenshot below)  &emsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;runs for Venus under (Remote Data (Simulations))  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;○ VEXMAG ephemeris data: Remote Data(Observations)/VexMag@Graz/VEX/Vex_mag/MAG_VSO/SC_POS_VSO  
● Plot the data. One can now zoom into the region, where the FMI HYB simulation run is plotted (see screenshot below).    

Image illustration for creating the absolute value of the observed magnetic field:  
![Magnetic Field Creation](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/3_absolute_value_of_the_observed_magnetic_field.png)  


Image illustration for zooming into the region:  
![Zoom Into the Region](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/3_Venus_Impact_Zoom_Into_Region.png)  

<h4 id='3c'>c)  The Earth Case</h4>  

● The same can be performed for the Earth case within AMDA. One can use e.g. WIND data to obtain the CME outside the magnetoshpere and **e.g. CLUSTER1 within the magnetosphere**. CLUSTER1 data can then be compared with SINP paraboloid model for Earth. The SINP model performs the simularion “on fly” **i.e. the input paramters are parameters measured by the chosen spacecraft at the chosen time**.    
● Besides AMDA, one can also go to the 3D visualization tool 3DView and test theinterconnectivity of AMDA & 3DView (see example in fourth step).  

<h3 id='4'>Fourth Step - Visualization within 3DView: IMPEx functionality within 3DView TheCMEimpact at Earth (Cluster1 & Geotail)</h3>  

1. Download and open [3DView](http://3dview.cdpp.eu/)  2. File → New. Open File → Manage Scene within the new scene window and choosea. Time range: Start = 2012/06/16 00:00:00 & Stop = 2012/06/17 00:00:00b. Choose Cluster1 & Geotail and start scene3. Loada. Science → Models → Magnetopause models / Shue, andb. Science → Impex tree4. Within the Impex tree choosea. Model data → FMI → GUMICS_Earth:run_000001 → 3DCubes → MagneticField→ traj interpol Bx,By,Bz and “Add selected data to 3DScene” (make sure thatGeotail is the selected spacecraft)b. Observational data → AMDA → Geotail → MGF → mgf_preliminary → b_gsmand “Add selected data to 3DScene”c. One may additionally add Cluster1 data in the same way as described above5. The different parameters can be manipulated via Scientific Control Panels (see screenshot below). One can get to the control panels via Science → Science data controls. Additionally further spacecrafts can be added via File → Manage Scene. Further data can also be added in the same way as described above.
![4.5 Manipulating Different Parameters](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/4_Manipulate_different_Parameter.png)

6. Within the science control one can also add a 2DPlot by clicking on “2Dplot” on therespective Science Control Panel (see below screenshot)   
![2D Plot](https://raw.githubusercontent.com/megadiesel705/tutorials/master/Connection-between-HELIO-and-IMPEx-tools/img/4_2DPlot.png)

<h3 id="5">References</h3>

PDF File exported from VESPA tutorial site.
