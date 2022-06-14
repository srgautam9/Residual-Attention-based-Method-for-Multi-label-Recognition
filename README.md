# Residual-Attention-based-Method-for-Multi-label-Recognition
**Motivation**
In a computer vision domain, recognizing objects is at the core of many visual tasks. Interestingly, multiple objects may appear in a single image, and
associating multiple labels is practically useful. However, methods usually lack in effectively capturing the various spatial regions occupied by objects
from belonging to different categories. Although attention-based methods are end-to-end solutions to multi-label recognition, however, are complicated
to optimize. Therefore, class-specific residual attention (CSRA) comes into rescue that utilizes the spatial attention for each object class separately
without losing accuracy. In this project, we propose an intuitive interpretation and brief comparison of various pre-trained models integrated with spatial
attention.

**Tasks**
1. Empirical interpretation of various components of CSRA
2. Finding intuitive explanation for CSRA
3. Analyzing the working and effect of different CNN-backbones underneath CSRA module
4. Assessing the effectiveness of CSRA on two multi-label datasets - PASCAL-VOC 2007 and WIDER

**Experimental Setup**
We build an end-to-end multi-label recognition model using three different CNN-backbones, ResNet18, ResNet-101 and ViT-B16 over PASCAL-VOC2007 and WIDER datasets. The CNN backbone
is initialized from various pretrained models, and fine-tuned for 30 epochs. For VOC2007, an image
size of 448x448 with a batch size = 16 and for WIDER, we used 224x224 and batch size = 64 is used.

**Observation and Conclusion**
Since all mAP results are close to each other, we can conclude that the CNN-backbone used underneath CSRA has not significant effect on the performance. The class-agnostic average pooling and
class specific attention matters much to the final performance in multi-label recognition.
Future prospect of the work looks at its applicability to other computer vision tasks - object detection
and more generalized image representations.
