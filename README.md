# efficientocr
a High Performance OCR model based on EfficientNet 

# Overview

There were many OCR models opensourced with feature extraction structure based on RCNN, Densenet and so on. with the release of EfficientNet in 2019, it achieve SOTA in many CV tasks with smaller parameter size, "why don't apply this great model in OCR since the feature extraction layers are the same thing" drives me explore the possibility of high performance OCR model.

with hundred of experiments and testings, finally I found a working model based on efficientnet which performs great in OCR tasks, named as "EfficientOCR".

below is the architecture of this model:

![arch.jpg]

# Changes

Add 2 RNN layers and 1 linear Dense layer and some minor modification to the original EfficientNet, now we can have a good performance with 1~2 Epochs training on large scale OCR datasets.

# Optimizations

1. OCR Label Smoothing
2. Data Augmentation (distortion,stretch,perspective,zoom out,random line,blur,squeeze & extract,text erase,background erase,shear)
3. Focal CTC Loss

# Supported Language

Some open source OCR model don't support blank in Chinese model but we resolved this issue and supporting below languages

1. English                          99%+
2. Simplified Chinese (Print)       97%+
3. Traditional Chinese (Print)      95%+
4. Simplified Chinese (Handwriten)  75%+
5. Traditional Chinese (Handwriten) 70%+

# Performance Comparision (with Google OCR, Baidu OCR, XunFei OCR) TBC


