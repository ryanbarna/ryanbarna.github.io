---
layout: post
title:  "Accelerometer Measurements with Respect to a Static Coordinate System"
date:   2023-01-02 19:43:50 -0600
categories: jekyll update
---

# Overview
Accelerometers are useful measurement devices that can accurately measure accelerational forces. However, they always report these forces with respect to their own coordinate systems. This means that as soon as the orientation of these chips change, so do their reported accelerational forces. So, what happens if you want to measure their acceleration relative to a static coordinate system like the Earth's? To do this, the chip's measuremnents must be mathematically corrected as its orientation changes. 


![image tooltip here](/assets/coordinate_system.png)
