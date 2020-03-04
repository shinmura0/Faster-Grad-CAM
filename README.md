# Faster-Grad-CAM
**Faster and more precisely than Grad-CAM.**

![fig1](https://github.com/shinmura0/Faster-Grad-CAM/blob/master/images/janken.png "fig1")

Upper result is...
+ The size of images is 96 * 96.  
+ We used MobileNet V2 with ArcFace.  
+ We measured the processing time on Colaboratory(Tesla P4).

## Based paper
*[Adapting Grad-CAM for Embedding Networks(arXiv, Jan 2020)](https://arxiv.org/abs/2001.06538)*  

We changed below.
+ change Triplet to ArcFace.  
+ change k-means clusters(from 50 to 10).


## Usage(Janken Demo)
+ Keras 2.2.4
+ TensorFlow 1.9.0
+ sklearn 0.19.0
+ Opencv 3.4.3.18
+ RapberryPi3 modelB(below result) or PC

![gif1](https://github.com/shinmura0/Faster-Grad-CAM/blob/master/images/heatmap.gif "gif1")

command below

```
python3 janken_demo.py
```

press [s] to change below mode(like ObjectDetection).

![gif2](https://github.com/shinmura0/Faster-Grad-CAM/blob/master/images/like_ObjectDetection.gif "gif2")

## Method
Coming soon.

## Procedure of training
Look at **Train_Faster-Grad-CAM.ipynb**

### More faster(Raspberry Pi)
+ Change MobileNet V2 to V3. Because V3 is faster than V2 on CPU.
+ Change Raspberry Pi3 to Pi4(or JetsonNANO).

## Special thanks
+ [janken_dataset](https://github.com/karaage0703/janken_dataset)(karaage0703)
