# Computer Vision Deep Learning Project

## Description of the idea

The idea is to gather data of a traffic junction through video cameras in order to detect the position of cars, pedestrians, bicycles and traffic in general. Furthermore also the velocity, acceleration could be detected using video streams and not only images.

The outcome is to detect the traffic and optimize the traffic lights given the new amount of real-time data on the streets.

It could also be of interest to be able to detect what type of lanes and streets, directly with the neural network so there would be no need of prior setup phase.

Everything should be then forwarded to a simulation, that will recreate the environment as a digital twin and run some deterministic algorithms in order to direct traffic in the most efficient way.

## Motivation

The main motivation for this project comes from a past hackathon I have done. Due the the limited amount of time we weren't able to begin such a big project. But since I have been thinking of it for a lot of time, and I think such course can be the perfect moment to take this challenge.

## Goal 

My goal would be to be able to understand how does the process of computer vision works, from the beginning to the end, and during the process, being able to develop, test and see some results of the task. The idea would be to make a program that takes any arbitrary type of intersection, and is being able to count how many cars, pedestrian and bycicles are there. If I can make that, the second goal would be to analyze the video in order to gain more data about speed and other metadata of the objects in the scene.


## Data needed

The data needed are going to be centered around the video dataset of an intersection. Also some videos/images of cars, trucks, busses, bycicles and pedestrians are needed to train the network. 
Also some data about the intersection is needed in order to further develop the neural network to understand the geometry of the environment (this would be a step in the future).

Some of the datasets I found:

- https://www.citycam-cmu.com/dataset -> CityCam 60,000 frames with rich information, leading to about 900,000 annotated objects.
- https://detrac-db.rit.albany.edu/download -> UA-DETRAC is a challenging real-world multi-object detection and multi-object tracking benchmark. The dataset consists of 10 hours of videos captured with a Cannon EOS 550D camera at 24 different locations at Beijing and Tianjin in China.
- https://www.uni-ulm.de/in/mrm/forschung/datensaetze.html -> Ko-PER intersection dataset.
- https://open.ottawa.ca/documents/traffic-services-api-webcam-images-traffic-flow/explore -> Ottawa webcam traffic realtime
- https://viratdata.org/#getting-data -> surveillance camerea for more training
- https://data.vision.ee.ethz.ch/cvl/webvision/dataset2018.html -> WEBVISION
- https://databank.illinois.edu/datasets/IDB-3671567 -> STREET dataset with over four millions still images (github source https://github.com/corey-snyder/STREETS)
- https://www.jpjodoin.com/urbantracker/dataset.html -> Urban tracker
- https://www.kaggle.com/datasets/aalborguniversity/aau-rainsnow -> Bad weather conditions records

others:
- http://civicapps.org/datasets/its-cameras-intelligent-transportation-system
- https://motchallenge.net -> car prespective video dataset
- https://archive.org/details/0002201705192 -> car prespective video 4k (from https://github.com/matterport/Mask_RCNN -> to count cars, maybe we should do some comparison with YOLO)
- https://opendata.dc.gov/datasets/2bb8375e31a94067a17911ea70f917ef_11/explore?location=38.891292%2C-77.031333%2C14.89 maybe street cameras?
- https://www.kaggle.com/datasets/aryashah2k/highway-traffic-videos-dataset -> highway dataset
- https://gram.web.uah.es/data/datasets/trancos/index.html
- http://www.cvlibs.net/datasets/kitti/eval_object.php
- https://github.com/VisualComputingInstitute/vkitti3D-dataset
- find out about the cameras at junctions in Osnabrueck
- https://www.cityscapes-dataset.com


## Methods and software

The software I am most likely to use is YOLO, in order to understand where the cars are. I might also try to use unity in order to recreate the digital twin of the road and the position of the cars.

- https://pjreddie.com/darknet/yolo/
- https://github.com/matterport/Mask_RCNN
- probably yolo V3
- SUMO for simulation of the city
- Tensorflow implementation ?

The language would be python, with libraries such pytorch and cv.

I'm not sure how I would link and bring everything together, but I will figure it out during the process, and also I am open for suggestions in that direction.

## Steps

### Step - 01

#### literature to read: 
- ["A Novel Camera Network Dataset for Traffic Flow."](https://www.osti.gov/servlets/purl/1668921) READ
- ["A Survey of Vision-Based Traffic Monitoring of Road Intersections"](https://ieeexplore.ieee.org/document/7458203) READ
- ["Integrating computer vision and traffic modeling for near-real-time signal timing optimization ](https://www.sciencedirect.com/science/article/abs/pii/S2210670721000676?via%3Dihub) TO READ
- ["The Ko-PER Intersection Laserscanner and Video Dataset"](https://www.uni-ulm.de/fileadmin/website_uni_ulm/iui.inst.110/Bilder/Forschung/Datensaetze/20141010_DatasetDocumentation.pdf) TO SKIM-READ

#### Tasks

- Detect cars in an image
- Detect people
- Detect bicycles
- Count the objects in the scene

### Step - 02

- Detect velocity by analyzing not only single images but stream of images

### Step - 03

- Define distance and position of the objects in the world

### Step - 04

- Detect lines, pavement and other environment object
- Create digital twin of the traffic junction
- Position dynamically the cars in the virtual environment and move them accordingly to the real world

## Timeline

### Week 1 - 3

Gathering data and information about the topic. Review the literature on the topic. Define challenges and opportunities.

### Week 3 - 6

Start to train neural network, or use pre-trained ones and asses results.
Iterate in order to get better results?

### Week 6 - 8

Implement the distance analysis

### Week 8 - 10

Video analysis comparison

### Week 10 - Deadline

Improve the network to recognize other environment objects, and create digital twin.

Also some simulations can be made about traffic optimization
