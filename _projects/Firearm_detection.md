---
name: Firearm Detection ML Model Project
tools: [Python, Machine Learning, Object Detection Model]
image: assets/pngs/gun_example.png
description: This is a firearm detection model for law enforcement purposes. (2024)
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Introduction

This report will discuss the final implementation of the weapons object detection model. The model trained using a custom dataset with over 1000 images and 200 epochs. Epochs being the number of iterations the entire dataset has been used to train the model.

This is done by using YOLOv8 as the base model and training it to detect weapons with high speed and relative accuracy. The training datasets are taken from Roboflow, a collection of open source computer vision datasets. After YOLOv8 has been trained using the custom dataset, it is then tested with bodycam and security footage videos found on Youtube. 

# Accuracy Takeaways

1. The current model has accuracy issues in terms of precision and recall
2. The model excels at predicting bounding boxes and  identifying the object’s category 

# Testing Results

The model has been tested with two different types of videos: security camera footage (CCTV) and police body camera footage. 

Security Camera Footage 
<img title="gun example 1" alt="model example 1" src="/assets/pngs/gun_example.png">

The model tested with the CCTV footage is more accurate and reliable compared to the police body camera footage. This is due to the chaotic nature of the footage. There are a lot more variables to consider from a body camera than a stationary CCTV. These challenges include motion blur, variable lighting conditions, different perspectives, dynamic backgrounds, and limited field of view. For the model to become more accurate with the bodycam, more finetuning will need to be done to adjust for it. This can include adjusting detection thresholds dynamically instead of setting it at a constant of 0.5 and incorporating temporal information. 

There are also issues with the detection system where it highlights black objects as weapons. 

<img title="gun example 2" alt="model example 2" src="/assets/pngs/gun_example2.png">