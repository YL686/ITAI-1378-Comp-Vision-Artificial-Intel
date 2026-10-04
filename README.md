# ITAI-1378-Comp-Vision-Artificial-Intel
# SmartShelf Vision — Retail Shelf Inventory & Out-of-Stock Alert System

**Team Member:** Yilin Leng  
**Course:** ITAI 1378 Computer Vision and AI  
**Tier Selection:** Tier 1 — Utilizing a pretrained YOLOv8 object detection backbone combined with custom OpenCV application logic for class-wise product tallying and automated restock alerting.

---

## 📌 Problem Statement
Retail store associates spend over 15 hours per week manually auditing shelf inventory, leading to up to 25% error rates in stock tracking and delayed restocks. Traditional per-product RFID tag systems are cost-prohibitive for everyday consumer goods.

## 💡 Solution Overview
SmartShelf Vision is an automated computer vision application that converts static retail shelf images into structured live inventory counts and immediate low-stock notifications.

## 🧰 Technical Approach
* **Computer Vision Technique:** Object Detection & Class-Wise Tallying Logic.
* **Model:** Pretrained YOLOv8 Small (`yolov8s.pt`).
* **Framework:** PyTorch, OpenCV, Ultralytics, NumPy.
* **Language:** Python 3.10+

## 📊 Data Plan
* **Source:** SKU-110K / RP2K Dataset (Publicly available via Kaggle/Roboflow).
* **Size:** 1,000+ annotated shelf images under varying product densities and lighting conditions.
* **Labels:** Bounding boxes with category labels for consumer packaged goods.

## 🎯 Success Metrics
* **Primary Metric:** $\ge 88\%$ mAP@0.5 object detection precision and $\ge 90\%$ accuracy in total shelf item counts.
* **Secondary Metric:** Inference processing speed $\le 200\text{ ms}$ per high-resolution image.

## 🗓 Milestone Plan
1. **Phase 1: Blueprint (Current)** — Finalize proposal, set up GitHub repository structure, and define baseline configurations.
2. **Phase 2: First Working Demo** — Run pretrained YOLOv8 on sample retail shelf images to establish an end-to-end pipeline.
3. **Phase 3: Application Logic** — Implement product classification, class-wise inventory tallying, and low-stock alerting logic.
4. **Phase 4: Evaluation & Testing** — Benchmark mAP, precision, recall, and count error rate on dense shelf displays.
5. **Phase 5: Packaging & Presentation** — Complete README documentation, record a 5-minute video presentation, and submit final deliverables.

## ⚠️ Risks and Mitigations
* **Risk 1:** Occlusion on deep shelves leading to missed item counts.
  * *Mitigation:* Restrict count calculations to front-facing product units ("Facing Count") per shelf row.
* **Risk 2:** Similar visual packaging across different flavors/variants causing misclassification.
  * *Mitigation:* Aggregate visually indistinguishable variants into single parent product groups to maintain high accuracy.
