# Forest-Health-Assessment-in-Sierra-Nevada-Mountains
Geographic object-based image analysis that investigates the change in forest health between the years 2018 and 2022

<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Software Used</h2>

- <b>ArcGIS Pro</b> 
- <b>Trimble eCognition</b>
- <b>Microsoft Excel</b> 

<h2>Analysis walk-through:</h2>

<p align="center">
Define study area: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Obtain multispectral NAIP imagery and LiDAR data for both timepoints:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open imagery and LiDAR data in Trimble eCognition, segment using quadtree and multi-resolution algorithm: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Determine land classes to include and generate interpretation key for each class to understand spectral and spatial properties NEED TO INCLUDE ALL CLASSES:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Define rules to classify each class based on their spectral and spatial properties :  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Break tree classification into 3 separate NDVI values: diseased, stressed, and healthy:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Determine percent change and perform accuracy assessment:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
