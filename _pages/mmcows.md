---
layout: temp
title: "MmCows"
permalink: /mmcows/
author_profile: false
redirect_from:
  - /mmcows
---

<h2 style="font-size: 2em; text-align: center;">MmCows: A Multimodal Dataset for Dairy Cattle Monitoring</h2>


Overview
------

MmCows is a large-scale multimodal dataset of dairy cattle for automated livestock monitoring consisting nine primary modalities and y secondary modalities. The primary modalities includes 3D uwb location, 3D visual location, neck acceleration , pressure, cbt, ankle, thi, isometric-view images. While the secondary modalities consists of 3D head direction, body location ground truth.
The data is collected from a cow pen during 14 days of a real-world deployment.

MmCows also contains a comprehensive set  of isometric-view visual data with 20k of annotated images from multiple cameras where 16 cows with their ID and behavior are labeled. 

Applications of MmCows spanning from behavior monitoring, dietary management, health management, to visual cow identification and multi-view multi-cow visual localization.

[Download Data and Code](https://github.com/hienvuvg/dairycattle_dataset)

<div align="center">
<video width="720" controls autoplay loop>
  <source src="https://hienvuvg.github.io/files/media/mmcows_vision_demo.mp4" type="video/mp4">
</video>
</div>

Sensors
------

<div align="center">
<img src="https://hienvuvg.github.io/files/media/cow_w_sensors.png" style="width:80%; height:auto;" />
</div>

Z wearable and implantable sensors that are used to collect 3D location and head direction, lying behavior, and core body temperature.

Isometric-view cameras provide ground truth as well as a non-invasive approach to behavior monitoring using computer vision.

Barn Environment
------

<div align="center">
<img src="https://hienvuvg.github.io/files/media/topview_pen_map.png" style="width:80%; height:auto;" />
</div>

pen size 20x12 m

anchor locations in [x,y,z]:

Uwb, camera, indoor sensor setups
Cow routine: milking, feeding, standing, bunching


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

Other Information
------

One application that we used to showcase the benefits of MmCows is behavior monitoring. Details of benchmarking MmCows for behavior monitoring using various modalities and their combinations are provided in this paper.

Text
```
Text
```

