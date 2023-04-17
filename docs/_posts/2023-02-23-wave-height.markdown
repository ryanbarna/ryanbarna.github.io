---
layout: post
title:  "IMU Accelerometer Measurements with Respect to a Static Coordinate System"
date:   2023-01-02 19:43:50 -0600
categories: jekyll update
---

# Overview
Inertial measurement units (IMUs) are useful measurement devices that contain magnetometers, gyroscopes, and accelerometers. These tools can accurately quantify accelerational forces, however, they always report these forces with respect to their own coordinate systems. This means that as soon as the orientation of these chips change, so do their reported accelerational forces. This is a limitation of these chips because in many cases, humans find it more intuitive to express the accleration of objects with respect to the Earth. Thankfully, this correction to an Earth frame is possible with a few mathematical tricks. By deriving the chips orientation from its sensors and rotating this expression a predetermined amount,  Accurate real-time algorithms employ these mathematical techniques to output intuitive accelerometer data in three-dimensional space.

![image tooltip here](/assets/coordinate_system.png)

# Madgwick Filtering
The combination of the three sensor measurements on most IMU chips (accelerometers, gyroscopes and magnetometers) allow for the precise calculation of orientation that are not explicitly reported by the IMU itself. One such technique is known as Madgwick filtering, and returns the chip's orientation as a quaternion, a sum of complex and imaginary parts. These quaternions are mathematically represented by `a+bi+cj+dk`, where `a`, `b`. `c`, and `d` are real numbers and `i`, `j`, and `k` are complex numbers that can be interpreted as vectors along the three dimensional axes. This expression has advantages over other ways of quantifying orientation.