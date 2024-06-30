---
layout: temp
title: "MmCows"
permalink: /mmcows/
author_profile: false
redirect_from:
  - /mmcows
---


<!--<h2 style="font-size: 2em; text-align: center;">MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</h2>-->

<p style="font-size: 25px; text-align: center;"><strong>MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</strong></p>

<br />

<!--#################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Overview</strong></p>

MmCows consists of data from 16 dairy cows collected during a 14-day real-world deployment, divided into two modality groups.
The primary group includes 3D UWB location, cows' neck IMMU acceleration, air pressure, cows' CBT, ankle lying behavior, RGB images, indoor THI, outdoor weather, and milk yield. 
The secondary group contains measured UWB distances, cows' head direction, ankle acceleration, and health records.

MmCows also contains a comprehensive set of isometric-view visual data with 20,000 annotated images from multiple camera views in one day.
All 16 cows with their ID and behavior are labeled as the ground truth, which was used to derive their 3D body location ground truth.

Applications of MmCows span from behavior monitoring, health management, and dietary management, to visual cow identification and multi-view multi-cow visual localization.

<p style="text-align: center;">
  [Download Data and Code](https://github.com/hienvuvg/dairycattle_dataset)
</p>

<div align="center">
<video width="720" controls autoplay loop>
  <source src="https://hienvuvg.github.io/files/media/mmcows_vision_demo.mp4" type="video/mp4">
</video>
</div>

<br />

<!--#################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<!--<p style="font-size: 25px; text-align: center;"><strong>Data Acquisition</strong></p>-->

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top:0; margin-bottom:5px;">The Sensors</p>
    <img src="https://hienvuvg.github.io/files/media/cow_w_sensors.png" style="width:80%; height:auto; vertical-align: middle;" />
</div>

Z wearable and implantable sensors that are used to collect 3D location and head direction, lying behavior, and core body temperature.

Isometric-view cameras provide ground truth as well as a non-invasive approach to behavior monitoring using computer vision.

<br />

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:25px; margin-top:0; margin-bottom:5px;">The Barn Setup</p>
    <img src="https://hienvuvg.github.io/files/media/topview_pen_map.png" style="width:80%; height:auto; vertical-align: middle;" />
</div>





pen size 20x12 m

anchor locations in [x,y,z]:

Uwb, camera, indoor sensor setups
Cow routine: milking, feeding, standing, bunching


<br />

<!--#################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Ground Truth</strong></p>

Cow ID and behavior with visual examples

<div align="center">
<img src="https://hienvuvg.github.io/files/media/behavior_examples.jpg" style="width:73%; height:auto;" />
</div>

<br />

<!--#################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Data Processing Flow</strong></p>

Text

<div align="center">
<img src="https://hienvuvg.github.io/files/media/processing_pipeline.png" style="width:54%; height:auto;" />
</div>

Uwb localization: including both measured data from an indoor uwb positioning system using two-way ranging, and 3D locations computed from the measured data using an optimization-based  localization algorithm.

Head direction: is derived from the neck acceleration and magnetic data where we use the Earth gravity and magnetic fields as reference vectors in 3D space.

Ankle lying reference: 

Ground truth
ID and behavior labeling
Visual localization

<div style="display: flex; justify-content: center; gap: 20px;">
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

<!--#################################################-->
<hr style="border: 1px; border-top: none; margin-bottom: 5px;">
<p style="font-size: 25px; text-align: center; margin-top: 0;"><strong>Other Information</strong></p>


One application that we used to showcase the benefits of MmCows is behavior monitoring. Details of benchmarking MmCows for behavior monitoring using various modalities and their combinations are provided in this paper.

### Contact us
<div style="display: flex;">
    <div style="flex: 1;"></div> <!-- Empty column -->
    <div style="flex: 1;">
        <a href="https://hienvuvg.github.io">Hien Vu</a> <br>
        Omkar Prabhune <br>
        Unmesh Raskar <br>
        Dimuth Panditharatne <br>
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

