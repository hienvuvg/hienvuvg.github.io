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
  	
  	<a href="https://github.com/hienvuvg/dairycattle_dataset" target="_blank" style="text-decoration: none;">
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

MmCows is a large-scale multimodal dataset for behavior monitoring, visual cow identification, multi-view multi-cow visual localization, health management, and dietary management of dairy cattle.

The dataset consists of data from 16 dairy cows collected during a 14-day real-world deployment, divided into two modality groups.
The primary group includes 3D UWB location, cows' neck IMMU acceleration, air pressure, cows' CBT, ankle lying behavior, multi-view RGB images, indoor THI, outdoor weather, and milk yield. 
The secondary group contains measured UWB distances, cows' head direction, ankle acceleration, and health records.

MmCows also contains 20,000 isometric-view images from multiple camera views in one day that are annotated with cows' ID and their behavior as the ground truth.
The annotated cow IDs from multi-views are used to derive their 3D body location ground truth.

<!--<p align="center">
  <a href="https://github.com/hienvuvg/dairycattle_dataset">Download Data and Code</a>
</p>-->


<div align="center">
<video width="720" controls autoplay loop>
  <source src="https://hienvuvg.github.io/files/media/mmcows_vision_demo.mp4" type="video/mp4">
</video>
</div>

<br />

<a id="sensors"></a>
<!-- SENSORS #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<!--<p style="font-size: 25px; text-align: center;"><strong>Data Acquisition</strong></p>-->

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top:5px; margin-bottom:0px;">The Sensors</p>
    <img src="https://hienvuvg.github.io/files/media/cow_w_sensors.png" style="width:80%; height:auto; vertical-align: middle; margin-bottom:15px;" />
</div>

The sensor suite consists of a neck-mounted collar tag, a vaginal temperature logger, and an ankle accelerometer for each of 10 cows, as well as four stationary cameras and six environmental sensors.
The neck tag records distances from the cow to eight stationary UWB anchors, the acceleration and magnetic field, and the ambient air pressure.
The temprature logger measures the core body temperature, while the ankle accelerometer records the leg direction of the cow.

The cameras provide visual data for identification, localization, and ground truth labeling of all 16 cows, while the environmental sensors measure indoor ambient conditions.
Additional data such as outdoor weather is recorded by a nearby weather station, and milk weight is logged by the barn staff.
All sensors are synchronized to the internet time.

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top: 5px; margin-bottom:0px;">The Barn Setup</p>
    <img src="https://hienvuvg.github.io/files/media/topview_pen_map.png" style="width:80%; height:auto; vertical-align: middle; margin-bottom:15px;" />
</div>

The cows are housed in a pen with the size of 20x12 m

anchor locations in [x,y,z]:

Uwb, camera, indoor sensor setups
Cow routine: milking, feeding, standing, bunching


<br />

<a id="ground_truth"></a>
<!-- GROUND TRUTH #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Ground Truth</strong></p>

Cow ID and behavior with visual examples

<div align="center">
<img src="https://hienvuvg.github.io/files/media/behavior_examples.jpg" style="width:73%; height:auto; margin-bottom:15px;" />
</div>

[Annotation rules](https://docs.google.com/document/d/1NAfwlkVOnybEZPSC2KwAE4i7GHH12huKUijDDizSxiI/edit?usp=sharing)

<br />

<a id="processing"></a>
<!-- DATA PROCESSING #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Data Processing Flow</strong></p>

Text

<div align="center">
<img src="https://hienvuvg.github.io/files/media/processing_pipeline.png" style="width:54%; height:auto; margin-bottom:15px;" />
</div>

Uwb localization: including both measured data from an indoor uwb positioning system using two-way ranging, and 3D locations computed from the measured data using an optimization-based  localization algorithm.

Head direction: is derived from the neck acceleration and magnetic data where we use the Earth gravity and magnetic fields as reference vectors in 3D space.

Ankle lying reference: 

Ground truth
ID and behavior labeling
Visual localization

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">
    <div style="text-align: center;">
        <video width="480" controls autoplay loop>
            <source src="https://hienvuvg.github.io/files/media/uwb_loc_vid.mp4" type="video/mp4">
        </video>
        <div>UWB localization for one cow</div>
    </div>
    <div style="text-align: center;">
        <video width="480" controls autoplay loop>
            <source src="https://hienvuvg.github.io/files/media/visual_loc_vid.mp4" type="video/mp4">
        </video>
        <div>Visual localization for multiple cows</div>
    </div>
</div>





<br />

<a id="usage"></a>
<!-- USAGE #################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Citation and Usage</strong></p>


One application that we used to showcase the benefits of MmCows is behavior monitoring. Details of benchmarking MmCows for behavior monitoring using various modalities and their combinations are provided in this paper.

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


Text
```
Text
```

