---
layout: post
title:  "Accelerometer Measurements with Respect to a Static Coordinate System"
date:   2023-01-02 19:43:50 -0600
categories: jekyll update
---

# Overview
Accelerometers are useful measurement devices that can accurately quantify accelerational forces. However, they always report these forces with respect to their own coordinate systems. This means that as soon as the orientation of these chips change, so do their reported accelerational forces. This is a limitation of these chips because, in many cases, humans find it more intuitive to express the accleration of objects with respect to the Earth. Thankfully, this correction to an Earth frame is possible with a few mathematical tricks. Accurate real-time algorithms employ these mathematical techniques to output intuitive accelerometer data.

<!-- # Mat

Thankfully the chip's measuremnents must be mathematically corrected as its orientation changes.  -->


![image tooltip here](/assets/coordinate_system.png)
