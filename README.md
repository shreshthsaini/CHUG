# CHUG: Crowdsourced User-Generated HDR Video Quality Dataset

![Dataset Banner](images/banner.png)

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Download Dataset](https://img.shields.io/badge/Download-CHUG-blue)](https://utexas.box.com/v/chug-dataset)

## 📌 Overview
CHUG is the **first large-scale User-Generated HDR (UGC-HDR) video quality dataset**, filling a crucial gap in perceptual quality assessment. It features:

✅ **5,992 videos** sourced from **856 UGC-HDR reference videos**  
✅ **Crowdsourced HDR videos**, ensuring real-world distortions  
✅ **Compression artifacts simulated** via a **bitrate ladder**  
✅ **211,848 subjective ratings** collected via **Amazon Mechanical Turk (AMT)**  
✅ **Balanced mix of portrait and landscape videos**  

This dataset is a benchmark for **No-Reference (NR) HDR-VQA models** and **HDR quality assessment research**.

---

## 📂 Dataset Structure

    CHUG_Dataset/
    │── metadata/
    │   ├── chug_videos.csv  # Metadata file with video details (MOS, SI, TI, bitrate, resolution)
    │   ├── subjective_scores.csv  # Raw human ratings from AMT study
    │── videos/
    │   ├── 1080p_ref/  # Reference HDR videos
    │   ├── 1080p_3Mbps/
    │   ├── 720p_2Mbps/
    │   ├── 360p_0.2Mbps/
    │── example_videos/  # Sample videos from dataset
    │── figures/
    │   ├── si_ti_distribution.png
    │   ├── mos_vs_resolution.png
    │   ├── bitrate_vs_mos.png
    │── README.md




---

## 🖥️ Sample Videos

🔗 [Example 1 (1080p Reference)](example_video_1.mp4)  
🔗 [Example 2 (720p @ 2Mbps)](example_video_2.mp4)  
🔗 [Example 3 (360p @ 0.2Mbps)](example_video_3.mp4)  

---

## 📊 Key Findings from the Dataset

- **Higher resolutions & bitrates improve perceptual quality** 📈  
- **UGC-HDR videos exhibit unique distortions, including banding and overexposure** 🌈  
- **Landscape vs. Portrait orientation has minimal impact on MOS, though portrait is slightly favored** 📱  
- **Compression artifacts degrade MOS significantly at low bitrates** ⚠️  

For full analysis, check our **[paper](paper_link_here.pdf)**.

---

## 📝 How to Use the Dataset?

1. **Download the dataset** [here](https://utexas.box.com/v/chug-dataset).
2. **Extract the dataset** and explore metadata in `chug_videos.csv`.
4. **Benchmark your NR-HDR-VQA models** using CHUG.

---

## 📜 Citation

If you use CHUG in your research, please cite:

***COMING SOON***


## 📜 License
CHUG is released under a Creative Commons Attribution-NonCommercial (CC BY-NC 4.0) License.


## 📬 Contact
For questions, reach out to:\
📧 ***NONE***

## Acknowledgments
Parts of this project page were adopted from the [Nerfies](https://nerfies.github.io/) page.

## Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
