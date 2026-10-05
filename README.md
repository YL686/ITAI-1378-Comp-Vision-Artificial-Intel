# SmartShelf Vision: Retail Shelf Inventory and Out of Stock Alert System

**Team Members:** Yilin Leng, Lufei Yu

**Course:** ITAI 1378 Computer Vision and AI

**Project Type:** Team Project

**Tier:** Tier 1

## Problem Statement

Retail employees often need to manually inspect shelves to determine which products are available and which products need to be restocked. Manual inventory checks can be time consuming and may result in missed or inaccurate counts. A computer vision system could help retail employees identify visible products, estimate inventory counts, and detect potential low stock conditions more efficiently.

## Solution Overview

SmartShelf Vision is a computer vision application that analyzes retail shelf images and automatically detects visible products. The system will use object detection to identify products, count detected items, and generate a low stock alert when the number of visible products falls below a predefined threshold.

The system will follow this workflow:

**Input → Model → Output**

**Retail Shelf Image → YOLOv8 Object Detection → Product Detection → Inventory Count → Low Stock Alert**

The goal is to create a practical proof of concept that demonstrates how computer vision can support retail inventory monitoring.

## Tier Selection

**Tier 1**

The team selected Tier 1 because it allows us to build a useful computer vision application using a pretrained object detection model and custom application logic. This scope is achievable within one term while still demonstrating an end to end computer vision workflow.

## Technical Approach

### Computer Vision Technique

**Object Detection**

### Model

**Pretrained YOLOv8 Small (`yolov8s.pt`)**

### Frameworks and Libraries

* Python
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy

The project will begin with a pretrained YOLOv8 model to establish a working end to end detection pipeline. This allows the team to test the core computer vision workflow before spending significant time on additional data preparation or model development.

After the detection pipeline works, the team will implement application logic to process detected objects, estimate visible product counts, and identify potential low stock conditions.

## Data Plan

The project will use publicly available retail shelf image datasets.

Potential sources include:

* SKU 110K
* RP2K
* Public Kaggle datasets
* Public Roboflow datasets

The target dataset size is approximately **1,000 or more images or image samples** for development and evaluation.

The selected data should contain retail shelf images and object annotations. Depending on the final dataset, annotations may include bounding boxes and product or object category information.

The final dataset will be selected based on:

* Accessibility
* Annotation quality
* Relevance to retail shelf detection
* Compatibility with YOLOv8
* Available number of usable images

The team will first test the pretrained model on a small number of sample images before using the larger selected dataset.

## Success Metrics

### Primary Metric

**mAP@0.5 ≥ 0.88**

The primary metric will measure object detection performance using mean Average Precision at an Intersection over Union threshold of 0.5.

### Secondary Metric

**Visible Shelf Item Count Accuracy ≥ 90%**

The system will compare its detected counts with the expected number of visible products in evaluation images.

### Additional Performance Measure

The team will also record inference time, with a target of approximately **200 milliseconds or less per image when feasible** using available Google Colab computing resources.

## Milestone Plan

| Phase               | Goal                                                                                   | Milestone                               |
| ------------------- | -------------------------------------------------------------------------------------- | --------------------------------------- |
| Blueprint           | Finalize the problem, solution, technical approach, data plan, and evaluation strategy | Proposal submitted                      |
| First Working Demo  | Run the pretrained YOLOv8 model on sample retail shelf images                          | End to end detection pipeline works     |
| Make It Yours       | Add the selected data and implement product counting and low stock alert logic         | Application works on the target problem |
| Improve and Measure | Test, debug, and evaluate detection and counting performance                           | Metrics recorded                        |
| Package and Present | Complete documentation, final presentation, and demonstration                          | Final project submitted                 |

### Development Priority

**Working Pipeline → Application Logic → Evaluation → Final Presentation**

The team will establish a working demonstration before spending significant time on additional data preparation or optimization.

## Team Responsibilities

The project will be completed collaboratively by **Yilin Leng and Lufei Yu**.

Both team members will contribute to project planning, data preparation, computer vision implementation, application development, testing, documentation, and presentation.

Specific responsibilities may be adjusted as the project progresses based on the needs of each development phase.

## Risks and Plan B

### Risk 1: Product Occlusion

Products may overlap with each other or be partially hidden on crowded shelves, which could cause the model to miss some products.

**Plan B:** The system will focus on visible front facing products rather than attempting to estimate every completely hidden product behind the front row. This keeps the project scope realistic for a one term project.

### Risk 2: Similar Product Packaging

Different products or product variants may have similar visual appearances, which could cause incorrect classifications.

**Plan B:** Visually similar variants can be grouped into broader product categories when necessary. The project will prioritize reliable detection and counting over extremely fine grained product classification.

## Computing Resources

The team will primarily use **Google Colab** for development and testing.

### Software

* Python
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy

### Estimated Cost

**$0 using available free computing resources.**

## Project Goal

The final goal of SmartShelf Vision is to demonstrate a practical computer vision workflow that can analyze retail shelf images, detect visible products, estimate inventory counts, and identify potential low stock situations.
