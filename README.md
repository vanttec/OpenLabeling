# OpenLabeling: open-source image and video labeler

[![GitHub stars](https://img.shields.io/github/stars/Cartucho/OpenLabeling.svg?style=social&label=Stars)](https://github.com/Cartucho/OpenLabeling)

Image labeling in multiple annotation formats:
- [YOLO darknet](https://github.com/pjreddie/darknet)

<img src="https://media.giphy.com/media/l49JDgDSygJN369vW/giphy.gif" width="40%"><img src="https://media.giphy.com/media/3ohc1csRs9PoDgCeuk/giphy.gif" width="40%">
<img src="https://media.giphy.com/media/3o752fXKwTJJkhXP32/giphy.gif" width="40%"><img src="https://media.giphy.com/media/3ohc11t9auzSo6fwLS/giphy.gif" width="40%">


## Table of contents

- [Prerequisites](#prerequisites)
- [Run project](#run-project)
- [GUI usage](#gui-usage)
- [Authors](#authors)

### Prerequisites

You need to install:

- [Python3]
- [OpenCV] version >= 3.0
- numpy, tqdm and lxml:
  
Running Requirements.txt:
```
python3 -mpip install -U pip
python3 -mpip install -U -r requirements.txt
```
    
### Run project

Step by step:

  1. Open the `main/` directory
  2. Insert the input images and videos in the folder **input/**
  3. Insert the classes in the file **class_list.txt** (one class name per line)
  4. Run the code:
  5. You can find the annotations in the folder **output/**

         python3 main.py [-h] [-i] [-o] [-t] [--tracker TRACKER_TYPE] [-n N_FRAMES]

         optional arguments:
          -h, --help                Show this help message and exit
          -i, --input               Path to images and videos input folder | Default: input/
          -o, --output              Path to output folder (if using the PASCAL VOC format it's important to set this path correctly) | Default: output/
          -t, --thickness           Bounding box and cross line thickness (int) | Default: -t 1
          --tracker tracker_type    tracker_type being used: ['CSRT', 'KCF','MOSSE', 'MIL', 'BOOSTING', 'MEDIANFLOW', 'TLD', 'GOTURN', 'DASIAMRPN']
          -n N_FRAMES               number of frames to track object for


### GUI usage

Keyboard, press: 

<img src="https://github.com/Cartucho/OpenLabeling/blob/master/keyboard_usage.jpg">

| Key | Description |
| --- | --- |
| a/d | previous/next image |
| s/w | previous/next class |
| e | edges |
| h | help |
| q | quit |

Video:

| Key | Description |
| --- | --- |
| p | predict the next frames' labels |

Mouse:
  - Use two separate left clicks to do each bounding box
  - **Right-click** -> **quick delete**!
  - Use the middle mouse to zoom in and out
  - Use double click to select a bounding box

### Label Custom Dataset

insert dataset on 

    OpenLabeling/main/input/

Get output labeled data from

    OpenLabeling/main/output/YOLO_darknet

## Authors

* **João Cartucho** - Please give me your feedback: to.cartucho@gmail.com

    Feel free to contribute

    [![GitHub contributors](https://img.shields.io/github/contributors/Cartucho/OpenLabeling.svg)](https://github.com/Cartucho/OpenLabeling/graphs/contributors)
