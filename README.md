# <img src="images/chug-logo.png" alt="Dataset Banner" width="25"> CHUG: Crowdsourced User-Generated HDR Video Quality Dataset




[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)](https://creativecommons.org/licenses/by-nc/4.0/) [![Paper](https://img.shields.io/badge/Paper-PDF-red)](./static/pdfs/chug.pdf) [![Supplementary](https://img.shields.io/badge/Supplementary-PDF-blue)](./static/pdfs/chug-supp.pdf) \
[![IEEE Xplore](https://img.shields.io/badge/View%20on-IEEE%20Xplore-blue)](https://ieeexplore.ieee.org/document/YOUR_PAPER_ID) [![arXiv](https://img.shields.io/badge/View%20on-arXiv-red)](https://arxiv.org/abs/YOUR_ARXIV_ID) 



## 📌 Overview
CHUG is the **first large-scale User-Generated HDR (UGC-HDR) video quality dataset**, designed for perceptual video quality assessment and No-Reference HDR-VQA research.

### **Key Features**
✅ **5,992 videos** from **856 UGC-HDR reference videos**  
✅ **Authentic UGC-HDR distortions**, including compression artifacts  
✅ **Bitrate ladder encoding**, simulating real-world streaming scenarios  
✅ **211,848 subjective ratings** collected via **Amazon Mechanical Turk (AMT)**  
✅ **Balanced mix of portrait and landscape videos**  

This dataset serves as a benchmark for **No-Reference (NR) UGC HDR-VQA models** and HDR quality assessment research.

---

## 📂 Downloading Dataset

Direct download link for dataset: **COMING SOON**

***For manual download, please see below.***

---

## 🔗 **Accessing Videos**

### **1️⃣ Directly from AWS S3 (via Browser)**
Each video is hosted on AWS S3 and can be accessed using:

    https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/VIDEO.mp4 

Replace `VIDEO` with a hashed video ID from `chug.csv` or `chug-video.txt`.

Example:  
Museum: [https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/9ae245a27cc5ea9d2f3fae9692250281.mp4](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/9ae245a27cc5ea9d2f3fae9692250281.mp4)

### **2️⃣ Downloading Videos Using AWS CLI**
To download all videos:
```sh
cat chug-video.txt | while read video; do
    aws s3 cp s3://ugchdrmturk/videos/${video}.mp4 ./CHUG_Videos/
done
```

To download a single video:
```sh
aws s3 cp s3://ugchdrmturk/videos/VIDEO.mp4 ./CHUG_Dataset/
```

To download selected videos, create a new text file with list of video IDs:
```sh
cat sample-video.txt | while read video; do
    aws s3 cp s3://ugchdrmturk/videos/${video}.mp4 ./CHUG_Videos/
done
```
---
## 📊 Key Dataset Insights
- Higher resolutions & bitrates improve perceptual quality 📈
- UGC-HDR videos exhibit unique distortions, including banding and overexposure 🌈
- Landscape vs. Portrait orientation has minimal impact on MOS, though portrait is slightly favored 📱
- Compression artifacts degrade MOS significantly at low bitrates ⚠️

### 📄 Paper and Supplementary Material

For a detailed analysis, check our [paper](./static/pdfs/chug.pdf) and [supplementary material](./static/pdfs/chug-supp.pdf).

---
## 🎬 Sample Videos (Direct Playback)

Below, you can directly play some sample HDR videos from our dataset:

### **Indoor Scene**
<video width="640" height="360" controls>
  <source src="https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/9ae245a27cc5ea9d2f3fae9692250281.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### **Carousel**
<video width="640" height="360" controls>
  <source src="https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/273a5d8a3b8c2d0eb4d4c8ff5fcfe360.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### **Rodeo**
<video width="640" height="360" controls>
  <source src="https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/7b7c9033da9fdb1a5762527f19baf54d.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### **Nature**
<video width="640" height="360" controls>
  <source src="https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/482dc1789b58cd2a353408602e9cd903.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


More sample are listed here in table:

| Category       | Video ID                                 | MOS Score | Resolution | Link |
|---------------|-----------------------------------------|-----------|------------|------|
| Indoor Scene  | `9ae245a27cc5ea9d2f3fae9692250281`     | 33.46     | 1080p      | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/9ae245a27cc5ea9d2f3fae9692250281.mp4) |
| Carousel      | `273a5d8a3b8c2d0eb4d4c8ff5fcfe360`     | 14.14     | 720p       | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/273a5d8a3b8c2d0eb4d4c8ff5fcfe360.mp4) |
| Rodeo         | `7b7c9033da9fdb1a5762527f19baf54d`     | 25.21     | 1080p      | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/7b7c9033da9fdb1a5762527f19baf54d.mp4) |
| Nature        | `482dc1789b58cd2a353408602e9cd903`     | 51.28     | 1080p      | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/482dc1789b58cd2a353408602e9cd903.mp4) |
| Museum        | `6ecb44305c0a4c421201b7bcfd369acb`     | 51.91     | 1080p      | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/6ecb44305c0a4c421201b7bcfd369acb.mp4) |
| Mountains     | `7435fdf9b5cda9a4299a7be5707ff911`     | 53.37     | 1080p      | [▶ Watch Video](https://ugchdrmturk.s3.us-east-2.amazonaws.com/videos/7435fdf9b5cda9a4299a7be5707ff911.mp4) |

Please checkout the full dataset.



---
## 🏆 Use Cases and Future Impact
CHUG serves as a crucial benchmark for No-Reference UGC HDR Video Quality Assessment (NR-HDR-VQA) and real-world HDR streaming quality analysis. Key applications:

### ✅ UGC-HDR Distortion Analysis
- CHUG captures banding, overexposure, luminance inconsistencies, making it an essential dataset for HDR distortion research.
### ✅ HDR Streaming Optimization
- Streaming providers can leverage CHUG to evaluate bitrate-resolution trade-offs, improving HDR compression pipelines.
### ✅ Advancing HDR Quality Metrics
- CHUG enables refinement of HDR-specific VQA metrics such as HDR-VMAF, HDR-SSIM, and learning-based perceptual models.

CHUG is expected to guide industry standards and HDR-VQA research for years to come.


## 📜 Citation
If you use CHUG in your research, please cite:

**COMING SOON**

## 📜 License
CHUG is released under a Creative Commons Attribution-NonCommercial (CC BY-NC 4.0) License.

## 📬 Contact
For questions, please reach out:
📧 [Redacted for Blind Review]

