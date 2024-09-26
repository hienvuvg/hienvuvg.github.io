---
layout: temp
title: "MmCows"
permalink: /mmcows/
author_profile: false
redirect_from:
  - /mmcows
---

<!--<p style="font-size: 25px; text-align: center;"><strong>MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</strong></p>-->

<div style="background-color: #f0f0f0; padding: 30px;">
  <p style="font-size: 33px; text-align: center;"><strong>MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</strong></p>
  
  <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-top: 30px;">
  	
  	<a href="https://github.com/neis-lab/mmcows" target="_blank" style="text-decoration: none;">
  	<button style="padding: 6px 10px; background-color:  #e44220 ; color: white; border: none; cursor: pointer; font-size: 18px;">Download Data and Code</button>
	</a>
    
    <a href="#sensors" style="text-decoration: none;">
    <button style="padding: 6px 10px; background-color: #008CBA; color: white; border: none; cursor: pointer; font-size: 18px;">The Sensors</button>
    </a>
    
    <a href="#ground_truth" style="text-decoration: none;">
    <button style="padding: 6px 10px; background-color: #008CBA; color: white; border: none; cursor: pointer; font-size: 18px;">Ground Truth</button>
    </a>
    
    <a href="#processing" style="text-decoration: none;">
    <button style="padding: 6px 10px; background-color: #008CBA; color: white; border: none; cursor: pointer; font-size: 18px;">Data Processing</button>
    </a>
    
    <a href="#usage" style="text-decoration: none;">
    <button style="padding: 6px 10px; background-color: #4CAF50; color: white; border: none; cursor: pointer; font-size: 18px;">Citation and Usage</button>
    </a>
  </div>
</div>


<!-- OVERVIEW #################################################-->
<!--<hr style="border: 1px; border-top: none; margin-bottom: 5px;">-->
<p style="font-size: 25px; text-align: center; margin-top: 20px;"><strong>Overview</strong></p>

MmCows is a large-scale multimodal dataset for behavior monitoring, health management, and dietary management of dairy cattle.

The dataset consists of data from 16 dairy cows collected during a 14-day real-world deployment, divided into two modality groups.
The primary group includes 3D UWB location, cows' neck IMMU acceleration, air pressure, cows' CBT, ankle acceleration, multi-view RGB images, indoor THI, outdoor weather, and milk yield. 
The secondary group contains measured UWB distances, cows' head direction, lying behavior, and health records.

MmCows also contains 20,000 isometric-view images from multiple camera views in one day that are annotated with cows' ID and their behavior as the ground truth.
The annotated cow IDs from multi-views are used to derive their 3D body location ground truth.

<!--<p align="center">
  <a href="https://github.com/neis-lab/mmcows">Download Data and Code</a>
</p>-->


<div align="center">
<video width="100%" controls autoplay loop>
  <source src="https://hienvuvg.github.io/files/media/mmcows_vision_demo.mp4" type="video/mp4">
</video>
<div><a href="https://github.com/neis-lab/mmcows/tree/main/visualization">Visualization of MmCows using an interactive 3D map and multiple views</a></div>
</div>

<br />

<a id="sensors"></a>
<!-- SENSORS #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<!--<p style="font-size: 25px; text-align: center;"><strong>Data Acquisition</strong></p>-->

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top:5px; margin-bottom:0px;">The Sensors</p>
    <img src="https://hienvuvg.github.io/files/media/cow_w_sensors.png" style="max-width:100%; width:90%; height:auto; vertical-align: middle; margin-bottom:15px;" />
</div>

The sensor suite consists of a neck-mounted collar tag, a vaginal temperature logger, and an ankle accelerometer for each of 10 cows, as well as four stationary cameras and six environmental sensors.
The neck tag records distances from the cow to eight stationary UWB anchors, the acceleration and magnetic field, and the ambient air pressure.
The temperature logger measures the core body temperature, while the ankle accelerometer records the leg direction of the cow.

The cameras provide visual data for identification, localization, and ground truth labeling of all 16 cows, while the environmental sensors measure indoor ambient conditions.
Additional data such as outdoor weather is recorded by a nearby weather station, and milk weight is logged by the barn staff.
All sensors are synchronized to the internet time.

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top: 5px; margin-bottom:0px;">The Barn Setup</p>
    <img src="https://hienvuvg.github.io/files/media/topview_pen_map.png" style="width:90%; height:auto; max-width:100%; vertical-align: middle; margin-bottom:15px;" />
</div>

The cows are housed in a 20x12m pen where they only leave for milking twice daily for approximately 30 min each time.
Eight stationary UWB anchors are installed around the pen that work with the neck tags to provide 3D locations of the cows.
Four high-resolution cameras are mounted at four corners of the pen to capture isometric-view images of the cows.


<br />

<a id="ground_truth"></a>
<!-- GROUND TRUTH #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Ground Truth</strong></p>

The ground truth of MmCows comprises visual cow IDs and behavior labels.
Out of 4.8M image frames, 20k UWB-synced frames from all four cameras in one day are selected for cow ID annotation.
We defined and annotated seven behaviors of all 16 cows at the granularity of one second during the chosen day.
Details of the annotation rules can be found [here](https://docs.google.com/document/d/1NAfwlkVOnybEZPSC2KwAE4i7GHH12huKUijDDizSxiI/edit?usp=sharing).

<div align="center">
<img src="https://hienvuvg.github.io/files/media/behavior_examples.jpg" style="width:85%; height:auto; max-width:100%; margin-bottom:15px;" />
</div>

<br />

<a id="processing"></a>
<!-- DATA PROCESSING #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Data Processing Flow</strong></p>

<div align="center">
<img src="https://hienvuvg.github.io/files/media/processing_pipeline.jpg" style="width:65%; height:auto; max-width:100%; margin-bottom:15px;" />
</div>

Some of the measured parameters are processed to derive more meaningful data that indicates the behaviors of the cows.
The heading direction related to feeding and drinking behaviors is obtained from the ```immu```.
The lying behavior is classified from the ankle acceleration. 
The 3D neck location ```uwb``` is calculated from UWB distances, while the 3D body location ground truth is derived from the ID-annotated labels.

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">
    <div style="text-align: center;">
        <video width="480" controls autoplay loop>
            <source src="https://hienvuvg.github.io/files/media/uwb_loc_vid.mp4" type="video/mp4">
        </video>
        <div><a href="https://github.com/neis-lab/mmcows/tree/main/visualization">UWB localization for one cow</a></div>
    </div>
    <div style="text-align: center;">
        <video width="480" controls autoplay loop>
            <source src="https://hienvuvg.github.io/files/media/visual_loc_vid.mp4" type="video/mp4">
        </video>
        <div><a href="https://github.com/neis-lab/mmcows/tree/main/visualization">Visual localization for multiple cows</a></div>
    </div>
</div>


<br />

<a id="usage"></a>
<!-- USAGE #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Citation and Usage</strong></p>

### Citation
Hien Vu, Omkar Prabhune, Unmesh Raskar, Dimuth Panditharatne, Hanwook Chung, Christopher Choi, and Younghyun Kim, "MmCows: A Multimodal Dataset for Dairy Cattle Monitoring", Advances in Neural Information Processing Systems (NeurIPS) Track on Datasets and Benchmarks, 2024. URL: [https://github.com/neis-lab/mmcows](https://github.com/neis-lab/mmcows)

Manuscripts: [Publisher](https://neurips.cc/virtual/2024/poster/97651), [Main Paper](https://www.dropbox.com/scl/fi/v6la2ydf9biwo1w7e76ck/MmCows_dataset.pdf?rlkey=ay6d407gtlgrjuit8cy4yiatv&st=zfhsxdw7&dl=1), [Supplementary Materials](https://www.dropbox.com/scl/fi/86fx179015w424iy36ehj/MmCows_supplementary.pdf?rlkey=79z3ykysdqgm76xk8qbhezvte&st=mymy14cp&dl=1), [Poster](https://www.dropbox.com/scl/fi/g466wu7mhuygx9ybh5nr9/MmCows_poster.pdf?rlkey=vqf6qt4md3xd86frsl70i08h9&st=g1z36kzr&dl=1)

```
@inproceedings{mmcows,
  title = {MmCows: A Multimodal Dataset for Dairy Cattle Monitoring},
  author = {Hien Vu and Omkar Prabhune and Unmesh Raskar and Dimuth Panditharatne and Hanwook Chung and Christopher Choi and Younghyun Kim},
  booktitle = {Proceedings of the Conference on Neural Information Processing Systems (NeurIPS)},
  year = {2024}
}
```

### Contact us
<div style="display: flex;">
    <div style="flex: 1;"></div> <!-- Empty column -->
    <div style="flex: 1;">
        <a href="https://hienvuvg.github.io">Hien Vu</a> <br>
        <a href="https://www.linkedin.com/in/omkar-prabhune/">Omkar Prabhune</a> <br>
        <a href="https://www.linkedin.com/in/unmesh-raskar-860273188/">Unmesh Raskar</a> <br>
        <a href="https://www.linkedin.com/in/dimuth-panditharatne/">Dimuth Panditharatne</a> <br>
        <a href="https://www.engineering.iastate.edu/people/profile/hwchung/">Hanwook Chung</a> <br>
        <a href="https://bse.wisc.edu/staff/choi-christopher/">Christopher Y. Choi</a> <br>
        <a href="https://engineering.purdue.edu/ECE/People/Faculty/ptProfile?resource_id=293362">Younghyun Kim</a> <br>
    </div>
    <div style="flex: 1;">
        hienvu@purdue.edu <br>
        oprabhun@purdue.edu <br>
        uraskar@wisc.edu <br>
        panditharatn@wisc.edu <br>
        hwchung@iastate.edu <br>
        cchoi22@wisc.edu <br>
        younghyun@purdue.edu <br>
    </div>
    <div style="flex: 1;"></div> <!-- Empty column -->
</div>


### License
MmCows is available under the CC BY-NC-SA 4.0 license. You can use, copy, and redistribute the material for non-commercial purposes, provided you credit the original source, include a link to the license, and indicate any modifications made. If you alter, adapt, or expand upon the material, your contributions must be distributed under the same license as the original. Commercial use of the material is not permitted.

<br />
<br />