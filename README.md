# Forest-Health-Assessment-in-Sierra-Nevada-Mountains
Geographic object-based image analysis that investigates the change in forest health between the years 2018 and 2022. 

<h2>Description</h2>
The results of this analysis address the research question of how forest health has changed from 2018 to 2022 by quantifying the drastic decrease in forest health over the course of 4 years. Specifically, the quantification indicates that there was a significant decrease in forest health which included a 36 percent increase in diseased trees, a 38 percent increase in stressed trees, and a 100 percent decrease in healthy trees. These results are further reinforced by high user’s and producer’s accuracy for the tree class that, for both 2018 and 2022 imagery, were calculated to be 80% and higher. In addition to this, these accuracy results indicate that the segmentation and classification ruleset developed in Trimble eCognition is robust in terms of the forest class. 
<br />
<br />
On the other end of the spectrum were several problems would have been addressed if more time was available. The first problem is that the segmentation was geared towards the spectral, spatial, and textural features of trees, not other land classes. This is further supported by the high user’s and producer’s accuracy for trees and lower accuracy for other classes. The quadtree and multiresolution algorithms are designed with this mindset and therefore result in problems with other classifications that aren’t trees. This is also evident due to the significant class bleed of classes such as houses, pavement, and bare earth. If I had to do this all over again, I would have added another segmentation algorithm and spent more time fine tuning the parameters of the current algorithms that were incorporated into the ruleset. 
One aspect of this classification that may have led to misleading results is the time at which the multispectral imagery was collected. The 2018 imagery, which was collected in September, coincides with a time of the year that experiences more rainfall and temperatures begin to decrease which equates to healthier trees. The 2022 imagery was collected during July. This month experiences higher temperatures and is relatively dry which can result in significantly lower NDVI values.
<br />


<h2>Software Used</h2>

- <b>ArcGIS Pro</b> 
- <b>Trimble eCognition</b>
- <b>Microsoft Excel</b> 

<h2>Analysis walk-through:</h2>

<p align="center">
Define study area: <br/>
<img src="https://i.imgur.com/wy1fHoF.png" height="80%" width="80%" />
<br />
<br />
Obtain multispectral NAIP imagery and LiDAR data for both timepoints:  <br/>
<img src="https://i.imgur.com/hDGsmBb.png" height="80%" width="80%" />
<img src="https://i.imgur.com/vwzBte0.png" height="80%" width="80%" />
<br />
<br />
Clip NAIP and LiDAR to study area, generate nDSM in ArcGIS Pro, and project to same coordinate system: <br/>
<img src="https://i.imgur.com/SlKp2Og.png" height="80%" width="80%" />
<br />
<br />
Open imagery and LiDAR data in Trimble eCognition and define segmentation ruleset <br/>
 <img src="https://i.imgur.com/1j5gsbH.png" height="80%" width="80%" />
<br />
<br />
Once segmented, generate interpretation key for each class to understand spectral and spatial properties:  <br/>
- Classes: buildings, bare earth, water, pavement, trees
<img src="https://i.imgur.com/jliaM1W.png" height="80%" width="80%" />
<br />
<br />
Leverage interpretation key to define classification rulesets for each class based on their spectral and spatial properties :  <br/>
<img src="https://i.imgur.com/Mb6Vaza.png" height="80%" width="80%" />
<br />
<br />
Break tree classification into 3 separate NDVI values: diseased, stressed, and healthy: <br/>
<img src="https://i.imgur.com/kVZytGS.png" height="80%" width="80%" />
<br />
<br />
Export classified map to ArcGIS and create thematic maps<br/>
<img src="https://i.imgur.com/Qt8kImO.png" height="80%" width="80%" />
<img src="https://i.imgur.com/fpaWrsv.jpeg" height="80%" width="80%" />
<br />
<br />
Calculate total acreage for each class in both timepoints to determine percent change and perform accuracy assessment:  <br/>
<img src="https://i.imgur.com/rOG3mAK.png" height="80%" width="80%" />
<img src="https://i.imgur.com/1vW1WYu.png" height="80%" width="80%" />
<img src="https://i.imgur.com/J62yjW5.png" height="80%" width="80%" />
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
