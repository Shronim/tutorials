#Virtis / Venus Express demo

* [Authors](#Authors)  
* [Change Log](#Log)  
* [Steps](#Steps)  
* [Reference](#Reference)  


<h2 id="Authors">Authors</h2>


S. Erard, B. Cecconi, P. Le Sidaner, F. Henry, R. Savalle, C. Chauvin  


<h2 id="Log">Change Log</h2>


Firstly converted from PDF file provided by VESPA website by [Keyuan Yin](https://github.com/megadiesel705) 


<h2 id="Steps">Steps</h2>


Go to [VESPA web site](http://vespa.obspm.fr)  

- Click "Custom resource"  

- Enter Resource URL:  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/1_VESPA_Website.png" width="500" alt"1">  

- Click  
(You can also click "Advanced query form"

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/2_Service_results.png" width="500" alt="2">  

Result is a list of files matching the query  


<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/3_query_result.png" width="500" alt="3">  


- Launch VO tools either from buttons

TOPCAT: tables  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/4_query_result.png" width="500" alt="4">  

- Send all results to VO tools
TOPCAT will receive the

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/5_Send_result.png" width="500" alt="5">  


- In TOPCAT, double-click table name to open it  


<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/6_TOPCAT.png" width="500" alt="6">  

- Click Sky-plotting icon  
Select parameters c1min & c2min  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/7_Sky-plotting.png" width="500" alt="7">  

- Click plane-plotting icon  
Select parameters C1min & C2min => Cylindrical map  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/8_plane-plotting.png" width="500" alt="8">  

- continue: Click plane-plotting icon  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/9_plane-plotting_2.png" width="500" alt="9">  

- In plane plot, click SizeXY option  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/10_SizeXY_option.png" width="500" alt="10">  

**Future developments to be implemented:**  

**On-line visualization of spectral cubes (demo)**  

- Select a test file in input, click "Process"  
(and wait a bit)  
- corresponding spectrum will plot

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/11_visualization_of_spectral_cubes.png" width="500" alt="11">  

- continue
- (with VOtools launched) Click "Register to SAMP
- Click on a "Send… via SAMP" button  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/12_visualization_of_spectral_cubes_2.png" width="500" alt="12">  

**Spectral tools: TOPCAT**  

TOPCAT receives spectra from APERICubes, can overplot selections  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/13_Spectral_tools_TOPCAT.png" width="500" alt="13">  

****
**Spectral tools: Specview**  

Specview receives spectra from APERICubes  


<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/14_Spectral_tools_Specview.png" width="500" alt="14">  

- continue Click on "Line IDs" to query band line
pick uprelevant ones  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/15_Spectral_tools_Specview_2.png" width="500" alt="15">  

****
**Spectral tools: CASSIS**  

CASSIS receives spectra from APERICubes, can overplot a selection of spectra and manipulate them  

- Click the "Tools" tab to combine spectra

- Press "shift" to get info on mouse location

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/16_Spectral_tools_CASSIS.png" width="500" alt="16">  

****
**Spectral tools: VOSpec**  

VOSpec receives spectra from APERICubes, but does

- Select Wavelength in micron & Flux in W/m2/μm in input pannel  


<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/17_Spectral_tools_VOSpec.png" width="500" alt="17">  

- continue Click "Simple Line Access" button  
Select area of interest  

*Fitting functions available in "Operations" menu*  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/18_Spectral_tools_VOSpec.png" width="500" alt="18">  

****
**VESPA to APERICubes connection (demo)**  
During the test phase:  




- Go to VESPA page, select one VIRTIS file as previsouly

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/19.png" width="500" alt="19">  


****
**VO functions**  

- VESPA provides search functions to the PSA VVEx dataset

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/20_VO_functions.png" width="500" alt="20">  

**Search other datasets**   
VESPA sends queries to several data services in parallel. In the long term it will access:  


<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/21_Search_other_datasets.png" width="500" alt="21">  



**Possible extension to the Virtis VEx data service**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/EPN-TAP-services-Virtis-Venus-Express-demo/img/22_possible_extension.png" width="500" alt="22">  

****


<h2 id="Reference">Reference</h2>


Please refer this tutorial to PDF file uploaded on VESPA wiki and also the [website](http://vespa.obspm.fr)  
