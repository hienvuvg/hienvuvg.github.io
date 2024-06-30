---
layout: temp
title: "MmCows"
permalink: /mmcows/
author_profile: false
redirect_from:
  - /mmcows
---

<h2 style="font-size: 2em; text-align: center;">MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</h2>

---
# Overview

MmCows consists of nine primary modalities and y secondary modalities. The primary modalities includes 3D uwb location, 3D visual location, neck acceleration , pressure, cbt, ankle, thi, isometric-view images. While the secondary modalities consists of 3D head direction, body location ground truth.
The data is collected from a cow pen during 14 days of a real-world deployment.

MmCows also contains a comprehensive set  of isometric-view visual data with 20k of annotated images from multiple cameras where 16 cows with their ID and behavior are labeled. 

Applications of MmCows spanning from behavior monitoring, dietary management, health management, to visual cow identification and multi-view multi-cow visual localization.

[Download Data and Code](https://github.com/hienvuvg/dairycattle_dataset)

<div align="center">
<video width="720" controls autoplay loop>
  <source src="https://hienvuvg.github.io/files/media/mmcows_vision_demo.mp4" type="video/mp4">
</video>
</div>

<br />

Data Acquisition
------

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:18px; margin-top:0; margin-bottom:5px;">The Sensors</p>
    <img src="https://hienvuvg.github.io/files/media/cow_w_sensors.png" style="width:80%; height:auto; vertical-align: middle;" />
</div>

Z wearable and implantable sensors that are used to collect 3D location and head direction, lying behavior, and core body temperature.

Isometric-view cameras provide ground truth as well as a non-invasive approach to behavior monitoring using computer vision.

<br />

<div style="text-align:center;">
    <p style="font-weight:bold; font-size:18px; margin-top:0; margin-bottom:5px;">The Barn Setup</p>
    <img src="https://hienvuvg.github.io/files/media/topview_pen_map.png" style="width:80%; height:auto; vertical-align: middle;" />
</div>





pen size 20x12 m

anchor locations in [x,y,z]:

Uwb, camera, indoor sensor setups
Cow routine: milking, feeding, standing, bunching


<br />

Ground Truth
------
Cow ID and behavior with visual examples

<div align="center">
<img src="https://hienvuvg.github.io/files/media/behavior_examples.jpg" style="width:73%; height:auto;" />
</div>

<br />


Data Processing Flow
------
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

Other Information
------

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

