# Hear Sign Language: A Real-time End-to-End Sign Language Recognition System



## Abstract：

Sign language recognition (SLR) bridges the communication gap between the hearing-impaired and the ordinary people. However, existing SLR systems either cannot provide continuous recognition or suffer from low recognition accuracy due to the difficulty of sign segmentation and the insufficiency of capturing both finger and arm motions. The latest system, SignSpeaker, has a significant limit in recognizing two-handed signs with only one smartwatch. To address these problems, this paper designs a novel real-time end-to-end SLR system, called DeepSLR, to translate sign language into voices to help people “hear” sign language. Specifically, two armbands embedded with an IMU sensor and multi-channel sEMG sensors are attached on the forearms to capture both coarse-grained arm movements and fine-grained finger motions. We propose an attention-based encoder-decoder model with a multi-channel convolutional neural network (CNN) to realize accurate, scalable, and end-to-end continuous SLR without sign segmentation. We have implemented DeepSLR on a smartphone and evaluated its effectiveness through extensive evaluations. The average word error rate of continuous sentence recognition is 6.6%, and it takes less than 1.1s for detecting signals and recognizing a sentence with 4 sign words, validating the recognition efficiency and real-time ability of DeepSLR in real-world scenarios. 

## 中文：

手语识别(SLR)在听障人士和普通人之间架起了沟通的桥梁。然而，现有的SLR系统要么不能提供连续的识别，要么由于手势分割的困难和对手指和手臂动作的捕捉不足而导致识别精度低。最新的系统SignSpeaker在只用一块智能手表识别双手标志方面有很大的限制。为了解决这些问题，本文设计了一个新颖的实时端到端SLR系统，称为DeepSLR，将手语翻译成声音，帮助人们 "听 "出手语。具体来说，两个嵌入了IMU传感器和多通道sEMG传感器的臂带被安装在前臂上，以捕捉粗粒度的手臂运动和细粒度的手指运动。我们提出了一个基于注意力的编码器-解码器模型和一个多通道卷积神经网络（CNN），以实现准确的、可扩展的和端到端的连续SLR，而无需符号分割。我们在智能手机上实现了DeepSLR，并通过大量的评估对其有效性进行了评价。连续句子识别的平均单词错误率为6.6%，检测信号和识别一个有4个标志词的句子所需时间不到1.1秒，验证了DeepSLR在真实世界场景中的识别效率和实时性能力。



# 一、选题背景

## 创意来源

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000327.png)

## 实现方案对比

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000347.png)

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000405.png)

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000443.png)

# 二、设计方案

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000539.png)

## 1、数据预处理

### 1.1 数据集构建

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000705.png)

### 1.2 降噪MSLE算法

![基于极值(Minimaxi)原则的db12小波变换去噪效果最好](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711000751.png)

### 1.3 使用双向双层LSTM神经网络进行Speech2Text转换

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001111.png)

## 2、实时识别系统构建

### 2.1 系统概述

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001153.png)

### 2.2 系统评估

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001225.png)

## 方案优势

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001313.png)

# 三、演示

## 1、单词识别

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001413.png)

## 2、句子识别

![](https://raw.githubusercontent.com/BBQldf/PicGotest/master/20220711001443.png)





# 结语：

### --尽绵薄之力为社会贡献一点点力量~

