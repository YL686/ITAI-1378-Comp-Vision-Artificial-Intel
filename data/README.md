# SmartShelf Vision Dataset

This folder documents the data source planned for the SmartShelf Vision team project.

## Primary Data Source

The team plans to use the **SKU 110K** dataset for retail shelf object detection.

**Dataset source:**  
https://github.com/eg4000/SKU110K_CVPR19

The SKU 110K dataset contains retail shelf images with bounding box annotations for object detection. It is suitable for testing product detection and counting in densely packed retail shelf scenes.

## Data Requirements

The selected data should provide:

- Retail shelf images
- Object annotations
- Bounding boxes
- Product or object category information when available

The team plans to use approximately **1,000 or more images** from the dataset for development and evaluation.

## Labels

SKU 110K primarily provides bounding box annotations for visible products. The project will use these annotations to evaluate product detection and counting.

## Data Selection Criteria

The dataset was selected based on:

1. Availability and accessibility
2. Annotation quality
3. Compatibility with YOLOv8
4. Number of usable images
5. Relevance to retail shelf inventory detection

The team will first test the pretrained YOLOv8 model on a small number of sample images before processing the larger dataset.

The selected data will be used for computer vision development and evaluation.
