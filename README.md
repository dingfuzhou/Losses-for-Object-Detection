## Loss Functions for Object Detection: An Overview
This repository provides an up-to-date list of loss functions proposed for solving the object detection problem, which includes both the 2D/3D, axis-aligned/rotated object detection tasks. 
 
=============================
# Table of contents
1. [Ground Truth Label Assignment](#1)  
    1.1 [One-to-Many Assignment](#1.1)  
    1.2 [One-to-One Assignment](#1.2)  
2. [Classification Losses](#2)  
	2.1 [Classical Classification Losses](#2.1)  
	2.2  [Sampling-based Approaches](#2.2)  
	2.3  [Re-weighting-based Approaches](#2.3)  
	2.4  [Gradient-based Approaches](#2.4)  
	2.5  [Ranking-based Approaches](#2.5)  
3. [Regression Losses](#3)  
	3.1 [Scale Imbalance Issue](#3.1)  
	3.2 [Optimization Issue](#3.2)  
	3.3 [Outlier Problem](#3.3)  
4. [Loss Function for Oriented Object Detection](#4)  
	4.1 [Boundary Discontinuity Problem](#4.1)  
	4.2 [Complicated-IoU-Computation-Issue](#4.2)  
 5. [ Future Research Directions](#5)  
	5.1 [Unifying Classification and Localisation Tasks](#5.1)  
	5.2 [Automation Loss Function Searching](#5.2)  
	5.3 [End-to-end Object Detection](#5.3)  
	5.4 [Mulit-tasks Learning](#5.4)  




----------------------------------
# 1. Ground Truth Label Assignment <a name="1"></a>  
## 1.1 One-to-Many Assignment<a name="1.1"></a>
  - Many object detectors are designed with this strategy such as RCNN Series, One-stage, Two-stages Anchor-based Anchor-free, and many 3D detectors;
## 1.2 One-to-One Assignment<a name="1.2"></a>  
  - DETR based object detectors, such as:  
  -End-to-End Object Detection with Transformers. [[Paper]](https://arxiv.org/pdf/2005.12872.pdf)  
  -End-to-end object detection with fully convolutional network. [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Wang_End-to-End_Object_Detection_With_Fully_Convolutional_Network_CVPR_2021_paper.pdf)  
  -Rethinking transformerbased set prediction for object detection. [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/papers/Sun_Rethinking_Transformer-Based_Set_Prediction_for_Object_Detection_ICCV_2021_paper.pdf)  
  -Sparse r-cnn: End-to-end object detection with learnable proposals. [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Sun_Sparse_R-CNN_End-to-End_Object_Detection_With_Learnable_Proposals_CVPR_2021_paper.pdf)  
  -Deformable DETR: Deformable transformers for end-to-end object detection. [[Paper]](https://openreview.net/pdf?id=gZ9hCDWe6ke)  
  -Pnp-detr: towards efficient visual analysis with transformers. [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/papers/Wang_PnP-DETR_Towards_Efficient_Visual_Analysis_With_Transformers_ICCV_2021_paper.pdf)  
  -Conditional detr for fast training convergence. [[Paper]](https://openaccess.thecvf.com/content/ICCV2021/papers/Meng_Conditional_DETR_for_Fast_Training_Convergence_ICCV_2021_paper.pdf)  

# 2. Classification Losses <a name="2"></a>  
## 2.1 Classical Classification Losses <a name="2.1"></a>  
- Boosting series，such as AdaBoost etc: 
- Support Vector Manchine.  
## 2.2 Sampling-based Approaches <a name="2.2"></a>  
- Offline Sampling-based Approaches.   
  -Many object detectors are designed with this strategy such as RCNN Series, One-stage, Two-stages Anchor-based Anchor-free, and many 3D detectors;  
  -CBGS: Class-balanced Grouping and Sampling for Point Cloud 3D Object Detection. [[Paper]](https://arxiv.org/pdf/1908.09492.pdf)     
  -Copy-and-Paste: [PointRCNN](https://openaccess.thecvf.com/content_CVPR_2019/papers/Shi_PointRCNN_3D_Object_Proposal_Generation_and_Detection_From_Point_Cloud_CVPR_2019_paper.pdf), [CenterPoint](https://openaccess.thecvf.com/content/CVPR2021/papers/Yin_Center-Based_3D_Object_Detection_and_Tracking_CVPR_2021_paper.pdf), [SECOND](https://pdfs.semanticscholar.org/5125/a16039cabc6320c908a4764f32596e018ad3.pdf), [PointPillars](https://openaccess.thecvf.com/content_CVPR_2019/papers/Lang_PointPillars_Fast_Encoders_for_Object_Detection_From_Point_Clouds_CVPR_2019_paper.pdf), etc.  
  -Rendering-based Copy and Paste: LiDAR-Aug: A General Rendering-based Augmentation Framework for 3D Object Detection. [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Fang_LiDAR-Aug_A_General_Rendering-Based_Augmentation_Framework_for_3D_Object_Detection_CVPR_2021_paper.pdf)    
 - Online Sampling-based Approaches.   
  -Training Region-based Object Detectors with Online Hard Example Mining. [[Paper]](https://openaccess.thecvf.com/content_cvpr_2016/papers/Shrivastava_Training_Region-Based_Object_CVPR_2016_paper.pdf)  
  -S-OHEM: Stratified Online Hard Example Mining for Object Detection. [[Paper]](https://arxiv.org/pdf/1705.02233.pdf)  
  -Libra R-CNN: Towards Balanced Learning for Object Detection. [[Paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)  
  -Prime Sample Attention in Object Detection. [[Paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Cao_Prime_Sample_Attention_in_Object_Detection_CVPR_2020_paper.pdf)  
  -Generating Positive Bounding Boxes for Balanced Training of Object Detectors. [[Paper]](https://openaccess.thecvf.com/content_WACV_2020/papers/Oksuz_Generating_Positive_Bounding_Boxes_for_Balanced_Training_of_Object_Detectors_WACV_2020_paper.pdf)  
## 2.3 Re-weighting-based Approaches <a name="2.3"></a>  
-Focal Loss for Dense Object Detection. [[Paper]](https://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf)  
-Focal Loss in 3D Object Detection. [[Paper]](https://arxiv.org/pdf/1809.06065.pdf)  
-Automated focal loss for image based object detection. [[Paper]](https://arxiv.org/pdf/1904.09048.pdf)  
-Spatial focal loss for pedestrian detection in fisheye imagery. [[Paper]](https://ieeexplore.ieee.org/abstract/document/8658951)   
-Focal text: an accurate text detection with focal loss. [[Paper]](https://ieeexplore.ieee.org/document/8451241)  
-Class-discriminative focal loss for extreme imbalanced multiclass object detection towards autonomous driving. [[Paper]](https://link.springer.com/article/10.1007/s00371-021-02067-9)  
-Dldenet: Deep local directional embeddings with increased foreground focal loss for object detection. [[Paper]](https://ieeexplore.ieee.org/document/8966436)  

## 2.4 Gradient-based Approaches <a name="2.4"></a> 
-Equalization loss for long-tailed object recognition. [[Paper]](https://arxiv.org/pdf/2003.05176.pdf)  
-Gradient harmonized single-stage detector. [[Paper]](https://arxiv.org/pdf/1811.05181.pdf)  
-Equalization loss v2: A new gradient balance approach for long-tailed object detection. [[Paper]](https://arxiv.org/pdf/2012.08548.pdf)  
-Droploss for longtail instance segmentation. [[Paper]](https://arxiv.org/pdf/2104.06402.pdf)   
-Distribution-balanced loss for multi-label classification in long-tailed datasets. [[Paper]](https://arxiv.org/pdf/2007.09654.pdf)  
-Distributional robustness loss for long-tail learning. [[Paper]](https://arxiv.org/pdf/2104.03066.pdf)  
-Adaptive class suppression loss for long-tail object detection. [[Paper]](https://arxiv.org/pdf/2104.00885.pdf)  
-Seesaw loss for long-tailed instance segmentation. [[Paper]](https://arxiv.org/pdf/2008.10032.pdf)  
## 2.5 Ranking-based Approaches <a name="2.5"></a>  
-Towards accurate one-stage object detection with ap-loss. [[Paper]](https://arxiv.org/pdf/1904.06373.pdf)  
-Ap-loss for accurate one-stage object detection. [[Paper]](https://arxiv.org/pdf/2008.07294.pdf)  
-Dr loss: Improving object detection by distributional ranking. [[Paper]](https://arxiv.org/pdf/1907.10156.pdf)  
-Rank & sort loss for object detection and instance segmentation. [[Paper]](https://arxiv.org/pdf/2107.11669.pdf)   
-A ranking-based, balanced loss function unifying classification and localisation in object detection. [[Paper]](https://arxiv.org/pdf/2009.13592.pdf)  
-Rankdetnet: Delving into ranking constraints for object detection. [[Paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Liu_RankDetNet_Delving_Into_Ranking_Constraints_for_Object_Detection_CVPR_2021_paper.pdf)  
-Tackling class imbalance with ranking. [[Paper]](https://ieeexplore.ieee.org/document/7727469)  
-Combining ranking with traditional methods for ordinal class imbalance. [[Paper]](https://ieeexplore.ieee.org/document/7727469)  

# 3. Regression Losses <a name="3"></a>  
## 3.1. Scale Imbalance <a name="3.1"></a>  
-A scale balanced loss for bounding box regression. [[Paper]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9112187)  
-Scaloss: Side and corner aligned loss for bounding box regression. [[Paper]](https://arxiv.org/pdf/2104.00462.pdf)  
-Scale-balanced loss for object detection. [[Paper]](https://www.sciencedirect.com/science/article/abs/pii/S0031320321001849)   
## 3.2. Optimization Issue <a name="3.2"></a>  
-Unitbox: An advanced object detection network. [[Paper]](https://arxiv.org/pdf/1608.01471.pdf)   
-Generalized Intersection over Union: A Metric and A Loss for Bounding Box Regression. [[Paper]](https://giou.stanford.edu/GIoU.pdf)  
-Distance-iou loss: Faster and better learning for bounding box regression. [[Paper]](https://arxiv.org/pdf/1911.08287.pdf)  
-Focal and efficient iou loss for accurate bounding box regression. [[Paper]](https://arxiv.org/pdf/2101.08158.pdf)  
-Alpha-iou:A family of power intersection over union losses for bounding box regression. [[Paper]](https://arxiv.org/pdf/2110.13675.pdf) 
-IoU Loss for 2D/3D Object Detection. [[Paper]](https://arxiv.org/pdf/1908.03851.pdf) 
## 3.3. Outlier Problem <a name="3.3"></a>  
-Unitbox: An advanced object detection network. [[Paper]](https://arxiv.org/pdf/1608.01471.pdf)   
-Generalized Intersection over Union: A Metric and A Loss for Bounding Box Regression. [[Paper]](https://giou.stanford.edu/GIoU.pdf)  
-Distance-iou loss: Faster and better learning for bounding box regression. [[Paper]](https://arxiv.org/pdf/1911.08287.pdf)  
-Focal and efficient iou loss for accurate bounding box regression. [[Paper]](https://arxiv.org/pdf/2101.08158.pdf)  
-Alpha-iou:A family of power intersection over union losses for bounding box regression. [[Paper]](https://arxiv.org/pdf/2110.13675.pdf) 
-IoU Loss for 2D/3D Object Detection. [[Paper]](https://arxiv.org/pdf/1908.03851.pdf) 
# 4. Loss Function for Oriented Object Detection <a name="4"></a>  
## 4.1. Boundary Discontinuity Problem <a name="4.1"></a>  
## 4.2. Complicated IoU Computation Issue <a name="4.2"></a>  

# 5. Future Research  Directions <a name="5"></a>  
## 5.1. Unifying Classification and Localisation Tasks <a name="5.1"></a>  
## 5.2. Automation Loss Function Searching <a name="5.2"></a> 
## 5.3. End-to-end Object Detection <a name="5.3"></a> 
## 5.4. Mulit-tasks Learning <a name="5.4"></a> 
 
 
