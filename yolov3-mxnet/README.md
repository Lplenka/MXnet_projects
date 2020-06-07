# yolov3-mxnet
A yolov3 simple implementation in MXNet, based on version 1.2.0 and cuda 9.0(optional), python3.
Works on Windows and Ubuntu 16.04.

## Table of Contents

- [yolov3-mxnet](#yolov3-mxnet)
  * [Installation](#installation)
  * [Detection](#detection)
  * [Train](#train)

## Installation

    $ git clone https://github.com/Fermes/yolov3-mxnet.git
    $ cd yolov3-mxnet/
    $ sudo pip3 install opencv-python mxnet-cu90==1.2.0

## Detection

put your images in ./images, and

    $ python detect.py [--gpu GPU ID]

you will get the results in ./results
or you can detect a video file, this need your opencv is compiled with ffmpeg.

    $ python detect.py --video VIDEO_FILE

you will get result.avi in ./results

## Train (for reference only)

The IMAGE_FOLDER should contains two directorys, "train" and "train_label", (or four, "train", "train_label", "val", "val_label") label should be xml file like VOC's format.
PS: You can use voc_label.py in https://pjreddie.com/darknet/yolo/ to get train.txt and val.txt, set path to --train and --val instead of --images.
```
    train.py [-h] [--epochs EPOCHS] [--images IMAGES FOLDER]
                [--batch_size BATCH_SIZE]
                [--params WEIGHTS_PATH] [--classes CLASS_PATH]
                [--confidence CONF_THRES] [--nms_thresh NMS_THRES]
                [--gpu GPU ID] [--prefix PARAMS FILE NAME PREFIX]
```
