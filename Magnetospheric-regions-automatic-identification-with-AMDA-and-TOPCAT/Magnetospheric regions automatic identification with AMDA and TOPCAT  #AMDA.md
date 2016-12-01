###Magnetospheric regions automatic identification with AMDA and TOPCAT	
#AMDA-TOPCAT use case##Magnetospheric regions automatic identification[Authors](#Authors)  
[Change Log](#Log)  
[Science Use Case](#Science Use Case)  
[Goals](#Goals)  
[Steps](#Steps)  
[References](#References)



<h2 id="Authors">Authors</h2>

V. Génot – October 2012 – V2  
His email:  vincent.genot@irap.omp.eu  

<h2 id="Log">Change Log</h2>

|Version|Name|Note|
|---|---|---|
|1|[Keyuan Yin](https://github.com/megadiesel705)|First converted from [this site](http://typhon.obspm.fr/VESPA-tutorials/docs/AMDA-TOPCAT_Magnetospheric_regions_automatic_identification.pdf)|

<h2 id="Science Use Case">Science Use Case</h2>

•  Based on Jelinek et al., JGR 2012 (paper1)  •  Uses AMDA for the analysis  •  Uses TOPCAT for visualisations  •  Uses IVOA SAMP to exchange data between AMDA and TOPCAT  

<h2 id="Goals">Goals</h2>

Goal :  
•  Reproduce two paper1’s results in a few steps  
–  Identify solar wind / magnetosheah / magnetosphere  
–  Identify bow shock and magnetopause  
•  Explore AMDA/TOPCAT enhanced functionalities  

–  AMDA conditional parameters  –  TOPCAT weighted density maps  
•  Propose new research perspectives  

<h2 id="Steps">Steps</h2>

**Magnetospheric region identification in Paper1**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/1_.png" width="500" alt="1">  

**THEMIS A magnetospheric sampling over ~3 years**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/2_.png" width="500" alt="2">  

Magnetospheric regions  only THEMIS A  In both cases, the bin/contour represents the number of events  
*Jelinek et al., JGR 2012*  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/3_.png" width="500" alt="3">  

**Magnetospheric Regions**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/4_.png" width="500" alt="4">  

**Bow shock and magnetopause identification**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/5_.png" width="500" alt="5">

In both case, each bin represents the probability (<1) for this location to be in the magnetosheath  In TOPCAT this is automatically computed from the flag_msh values  
*Jelinek et al., JGR 2012*  

**Step by step AMDA–TOPCAT analysis  Magnetospheric region identification**  

•  define rB and rn in AMDA (create new parameters, see slide for exact definition)  
&nbsp;&nbsp;•  time delay between ACE and THEMIS A is taken constant  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•  for instance : shift(param,4000) shifts ACE data from 4000s forward  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•  here : param=BACE or nACE  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•  a better approach would use (see plot) : T=|XACE-XTHEMIS_A|/VSW  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;•  a much better approach would use an iterative algorithm to compute T   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• forinstancesee http://cdpp-amda.cesr.fr/DDHTML/HELP/delay.html  •  launch TOPCAT ; it automatically opens a SAMP hub  •  in AMDA : click the « interoperability » and open a SAMP connection  •  download rB and rn on 2007/03/01 – 2009/10/01 at 60s resolution (all in one file) 
•  in AMDA : in the « Download Results » window choose « Send to TOPCAT »  •  the table is automatically loaded in TOPCAT  •  choose « density map » (2D histogram) : rB function of rn  •  adjust binning and plotting range as necessary (0-8 for rn, 0-22 for rB)  •  do not worry about NaN values !  

**Step by step AMDA–TOPCAT analysisBow shock and magnetopause identification**  
Use of AMDA conditional parameters  

•  define the solar wind ram pressure pSW shifted to THEMIS A  
&nbsp;&nbsp;•  time delay may be taken as 4000s as before   
&nbsp;&nbsp;• pSW=1.67e-6nACEVACE^2  •  produce a time table T1 when the pSW values are in a restricted band (ex: pSW<4)  
•  define a new (conditional) parameter : flag_msh&nbsp;&nbsp;&nbsp;&nbsp;•  flag_msh=1 if rB>4-rn and rB<10rn (see plot), else 0 (for solar wind and magnetosphere)  •  download XTHA, sqrt(YTHA^2+ZTHA^2), flag_msh at 3600 s resolution (all in one file) for the above T1 time table  

￼**Transfer via SAMP (same procedure as before)**  

•  the table is loaded into TOPCAT  •  choose « density map » (2D histogram) :  &nbsp;&nbsp;• sqrt(Y^2+Z^2) function of X weighted by flag_msh   
•  adjust binning as necessary  

**Parameter definition in AMDA**  
```
r_n = n_i_tha/shiftT_(sw(0),4000)  
```

```
r_b = bs_tha(3)/shiftT_(imf(3),4000)  
```

```
p_sw = shiftT_(sw(0)*sw(1)*sw(1),4000)*1.67e-6
```

```
flag_msh = (n_i_tha/shiftT_(sw(0),4000)+bs_tha(3)/shiftT_(imf(3),4000) > 4.) & (bs_tha(3)/shiftT_(imf(3),4000) - 10.*n_i_tha/shiftT_(sw(0),4000) <0.)
```

flag_msh value is either 1 (THEMIS A is in the magnetosheath) or 0  

**Time delay between ACE and THEMIS A**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/6_.png" width="500" alt="6">  

```
It is computed along the XGSE direction : T=|XACE-XTHEMIS_A|/VSW
```

**Time Dalay**  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/7_.png" width="500" alt="7">  

Here the delay T varies much more, a « banded » delay could be adopted (not implemented here) with conditional parameters :  

```bs_tha(3)/shiftT_(imf(3),2400)  
```or  

```bs_tha(3)/shiftT_(imf(3),3200)  
```
or  

```bs_tha(3)/shiftT_(imf(3),4000)  
```

*In AMDA a conditional parameter P is such that P=1 if P is trueEx: C=A\*(T<3600)+\*(T>3600) is equal to either A or B depending on the value of T*  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/8_.png" width="500" alt="8">  

**Perspectives**  • Refine analysis with smaller ram pressure domains  • Extend to larger time intervals, and other S/C (all THEMIS, CLUSTER, ...) • Extend to magnetosphere and solar wind region determinations   
• Use this procedure to deduce bow shock and magnetopause models  
**Tool enhancements**  • TOPCAT  &nbsp;&nbsp;&nbsp;&nbsp;• Bin value on mouse over  &nbsp;&nbsp;&nbsp;&nbsp;• Over plot of contours and user defined lines on density maps  • AMDA  &nbsp;&nbsp;&nbsp;&nbsp;• Delay procedure (continuous instead of constant or « banded »)  

Using the binning TOPCAT functionality for density map  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/9_.png" width="500" alt="9">  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/10_.png" width="500" alt="10">  

<img src="https://raw.githubusercontent.com/megadiesel705/tutorials/master/Magnetospheric-regions-automatic-identification-with-AMDA-and-TOPCAT/img/11_.png" width="500" alt="11">  

<h2 id="References">References</h2>

Please refer this tutorial to the [original version](http://typhon.obspm.fr/VESPA-tutorials/docs/AMDA-TOPCAT_Magnetospheric_regions_automatic_identification.pdf)






