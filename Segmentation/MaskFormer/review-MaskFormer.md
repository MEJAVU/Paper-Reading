# Per-Pixel Classification is Nopt All You Need for Semantic Segmentation

### Simple Summary
Per-Pixel Classification 을 사용하지 않고 Mask Classification 으로도 Semantic Segmentation 문제에서 높은 성능을 보여주었음.
Mask Loss Prediction 은 Transformer 기반의 Object Detection 모델 DETR 


## Introduction
제안된 FCN 모델들 대다수는 Per-Pixel Classification 을 이용하여 Semantic Segmentation 에서 강세를 보여주고 있다.
하지만, Regions, Segments 값을 구할 수 없기 때문에 Instance Segmentation 를 해결 할 수 없었다.
Mask Classification 은 단일 클래스에 대한 Binary Mask 의 모음(set)을 예측하기 때문에 Instance Segmentation 문제를 해결하는데 적합하면서,
Mask R-CNN, DETR 모델은 Instance Segmentation 과 Semantic Segmentation 을 동시에 해야 하는 Panoptic Segmentation 도 해결 할 수
있었다. 

![DETR - Panoptic Segmentation](../fig/MaskFormer-DETR_Decoder.png?raw=true "DETR Panoptic Segmentation")

#### DETR를 이용한 Panoptic Segmentation 예시
