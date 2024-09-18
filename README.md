# Forest-Health-Assessment-in-Sierra-Nevada-Mountains
Geographic object-based image analysis that investigates the change in forest health between the years 2018 and 2022

<h2>Description</h2>

<br />


<h2>Software Used</h2>

- <b>ArcGIS Pro</b> 
- <b>Trimble eCognition</b>
- <b>Microsoft Excel</b> 

<h2>Analysis walk-through:</h2>

<p align="center">
Define study area: <br/>
<img src="https://i.imgur.com/wy1fHoF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Obtain multispectral NAIP imagery and LiDAR data for both timepoints:  <br/>
<img src="https://i.imgur.com/DoMJ50G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2setWfD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Clip NAIP and LiDAR to study area, generate nDSM in ArcGIS Pro, and project to same coordinate system: <br/>
<img src="https://i.imgur.com/SlKp2Og.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open imagery and LiDAR data in Trimble eCognition, define rulesets for segmentation and classification of each land class: <br/>
 
 - Buildings
   
 - Bare earth
   
 - Water
   
 - Pavement
   
 - Trees
<img src="https://i.imgur.com/kV01Uuu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Generate interpretation key for each class to understand spectral and spatial properties:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Define rules to classify each class based on their spectral and spatial properties :  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Break tree classification into 3 separate NDVI values: diseased, stressed, and healthy:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Determine percent change and perform accuracy assessment:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
