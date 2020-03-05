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
+ Quantization like [this](https://github.com/PINTO0309/PINTO_model_zoo/tree/master/15_Faster-Grad-CAM).

## Application examples
1.Anomaly detection  
When you use [Self-supervised-learning](https://medium.com/analytics-vidhya/spotting-defects-deep-metric-learning-solution-for-mvtec-anomaly-detection-dataset-c77691beb1eb), anomaly region is visualised by using Faster-Grad-CAM.  
Next example is that circle is normal.

![fig3](https://github.com/shinmura0/Faster-Grad-CAM/blob/master/images/normal_image.png "normal")  

And extra line or missing line is anomaly image.

![fig4](https://github.com/shinmura0/Faster-Grad-CAM/blob/master/images/anomaly_detection.png "anomaly")  

Realtime visualization is like this(Coming soon).

2.[Auto-Annotation](https://github.com/shinmura0/Auto-Annotation)

## Special thanks
+ [janken_dataset](https://github.com/karaage0703/janken_dataset)(karaage0703)
