# SimpleCVReproduction

我将感兴趣/推荐的模型也放在这个库中，以供学习。由于好多库从头开始学习难度太大，所以在这里提供了笔者的经验，其中大部分都是跑过的模型、准备读的代码、已经读过的代码笔记、自己开发的simple系列简单代码、常用代码段。

尽量提供简化版本的，便于理解的模型文件。

如果有推荐的便于初学者学习的库，也欢迎在issue中提出，之后会补充上来。

## 即插即用模块（注意力模块）

- 注意力模块Attention

  - BAM
  - BiSeNet
  - CBAM
  - CCNet
  - GCBlock
  - HRNet
  - Non-Local
  - OCR
  - ResNeSt
  - scSE
  - SE
  - SK
  - DANet: Dual Attention
  - AFF
    - MC-CAM
    - AFF
    - iAFF
- Plug-and-play module: 即插即用模块：
  - ACBlock
  - Swish、wish Activation
  - ASPP Block
  - DepthWise Convolution
  - Fused Conv & BN
  - MixedDepthwise Convolution
  - PSP Module
  - RFBModule
  - SematicEmbbedBlock
  - SSH Context Module
  - Some other usefull tools such as concate feature map、flatten feature map
  - WeightedFeatureFusion:EfficientDet中的FPN用到的fuse方式
  - StripPooling：CVPR2020中核心代码StripPooling
  - GhostModule: CVPR2020GhostNet的核心模块
  - SlimConv: SlimConv3x3 
  - Context Gating： video classification
  - EffNetBlock: EffNet
  - ECCV2020 BorderDet: Border aligment module
  - CVPR2019 DANet: Dual Attention
  - ICCV2019 CCNet: Criss Cross Attention
  - Object Contextual Representation for sematic segmentation: OCRModule
  - FPT: 包含Self Transform、Grounding Transform、Rendering Transform
  - DOConv: 阿里提出的Depthwise Over-parameterized Convolution
  - PyConv: 起源人工智能研究院提出的金字塔卷积
  - ULSAM：用于紧凑型CNN的超轻量级子空间注意力模块
  - DGC: ECCV 2020用于加速卷积神经网络的动态分组卷积
  - DCANet: ECCV 2020 学习卷积神经网络的连接注意力
  - PSConv: ECCV 2020 将特征金字塔压缩到紧凑的多尺度卷积层中
  - Dynamic Convolution: CVPR2020 动态滤波器卷积（非官方实现，蹲）

> PS: 关于如何在YOLOv3中加入以上模块，可以访问[这个博客](https://blog.csdn.net/DD_PP_JJ/article/details/104109369)，这个里边实现了SE,SK,CBAM,SPP,ASPP等在内的模型，对应的代码在https://github.com/GiantPandaCV/yolov3-point。

## 其他推荐项目

- CenterNet 是一个简化版本的（并非原版），正在分析和学习源码。
- SmallObjectAugmentation是一个专门用于小目标增强库，实际效果不是很理想。增加了一些处理工具模块。
- captcha-CTC-loss CTC loss+ LSTM 
- deep_sort-master 官方实现，通过该库理解了标准的输入输出格式。
- easy-receptive-fields-pytorch-master: 用于计算pytorch常用CNN的感受野，非常方便
- kalman 知乎上的一个简单的卡尔曼滤波算法实现代码
- opencv-mot 用OpenCV中自带的跟踪器如KCF等实现跟踪，第一帧目标需要在代码中指定。
- pytorch-commen-code pytorch中常用的一些代码
- pytorch-grad-cam-master grad cam的实现
- pytorch-semseg pytorch实现语义分割，目前仅在自己数据集上训练了Unet，无法收敛。
- siamese-triplet : 孪生网络+triplet loss
- simple-DCGAN : DCGAN, 还没来得及研究
- simple-faster-rcnn-pytorch 陈云老师的实现
- simple-triple-loss 自己仿照一个库写了一个简化版的triple loss
- tiny_classifier : 目标检测级联一个分类网络中的分类网络的简单实现。
- tools: 目前只有voc2coco.py工具
- yolov3-6: U版yolov3中release出来的稳定版本，其中使用的是原始的yolov3 loss，改动不多。
- DBFace:readme中展示了非常好的检测效果碾压retinaFace,CenterFace，目前只提供inference，还没有train，期待公开训练代码...（ps: landmark用的是heatmap）
- simple_keypoints: 简单的关键点检测，提供了通过heatmap和回归两种方法进行检测
- ultralytics_newest_yolov3: 这个库在coco数据集上已经刷到了SOTA，但是根据我在2020年4月14日跑的自己的数据集来说，效果并不好，即便加载预训练权重，yolov3.cfg只能达到60%的mAP, 可能是作者调用了大量的trick来对coco上的结果进行优化，虽然在COCO上mAP@0.5都刷到62.8了，但是训练自己的数据集效果却越来越差。之前也用过这个训练同样的数据集，老版本的这个库虽然在coco上效果不那么惊人，但是在我的数据集上能达到80%的mAP。不知道问题在何，如果有看到这里的大佬欢迎在issue中交流一下，指点一下。
- YOLOv3-complete-pruning: 基于U版进行剪枝的库，效果还不错。
- yolov5: 于8月6日，在小麦检测比赛上效果惊人，超过了cascade rcnn等传统比赛常用模型。
- TSNE: 可视化重识别数据集、分类数据集，效果挺好的，不过一般需要对服务器内存要求比较高
- tikz-cnn: 用LaTeX中tikz包绘制卷积神经网络结构图


## 感谢

@zhongqiu1245 补充的borderDet中的BAM模块,补充了FPT

@1187697147 补充的context-gating模块