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
- [Regression Losses](#REGRESSION-LOSSES)
	- [Scale Imbalance Issue](#Scale-Imbalance)
	- [Optimization Issue](#Optimization-Issue)
	- [Outlier Problem](#Outlier-Problem)
- [Loss Function for Oriented Object Detection](#Loss-Function-for-Oriented-Object-Detection)
	- [Boundary Discontinuity Problem](#Boundary-Discontinuity-Problem)
	- [Complicated-IoU-Computation-Issue](#Complicated-IoU-Computation-Issue)
 - [ Future Research Directions](#Future-Research-Directions)
	- [Unifying Classification and Localisation Tasks](#Unifying-Classification-and-Localisation-Tasks)
	- [Automation Loss Function Searching](#Automation-Loss-Function-Searching)
	- [End-to-end Object Detection](#End-to-end-Object-Detection)
	- [Mulit-tasks Learning](#Mulit-tasks-Learning)




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
## 2.2 Sampling-based Approaches <a name="2.2"></a>
## 2.3 Re-weighting-based Approaches <a name="2.3"></a>
## 2.4 Gradient-based Approaches <a name="2.4"></a>
## 2.5 Ranking-based Approaches <a name="2.5"></a>

# Regression Losses
## Scale Imbalance
## Optimization Issue
## Outlier Problem

# Loss Function for Oriented Object Detection
## Boundary Discontinuity Problem
## Complicated IoU Computation Issue

# Future Research  Directions
## Unifying Classification and Localisation Tasks
## Automation Loss Function Searching
## End-to-end Object Detection
## Mulit-tasks Learning
 
 
