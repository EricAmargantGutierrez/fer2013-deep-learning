# Facial Expression Recognition (FER) — Deep Learning 2025-26

**Group:** Beta  
**Authors:** Eric Amargant, Eya Ben Said, Marc Bosch Manzano  
**Professor:** Laia Tarrés Benet  
**Course:** Deep Learning 2025-26, Universitat Pompeu Fabra  

---

## Overview

This project tackles Facial Expression Recognition (FER) as a 7-class image classification problem using the FER2013 benchmark dataset. We implement and compare two deep learning approaches:

- A **Custom CNN** trained from scratch, used as the baseline
- A **ResNet-18** fine-tuned from ImageNet weights using a two-stage transfer learning strategy

The goal is to quantify the benefit of transfer learning on a noisy real-world benchmark and analyse the systematic failure modes of both architectures.

---

## Results

| Model | Test Accuracy | Macro F1 |
|---|---|---|
| Custom CNN | 57.09% | 0.53 |
| ResNet-18 | 63.42% | 0.62 |
| Human-level (est.) | ~65% | — |

---

## Project Structure

```
fer2013-deep-learning/
│
├── Final_project.ipynb                  # Main notebook with all code
├── team_beta_project_report.pdf         # Written report
├── team_beta_project_presentation.pptx  # Presentation slides
└── README.md                            # This file
```

---

## How to Run

The notebook is designed to run on **Google Colab** with GPU enabled. Follow these steps:

### 1. Open the notebook in Google Colab
Upload `Final_project.ipynb` to Colab or open it directly from GitHub via the badge above.

### 2. Enable GPU
Go to **Runtime → Change runtime type → T4 GPU** and save.

### 3. Get your Kaggle API token
The dataset is downloaded automatically from Kaggle inside the notebook. You do not need to download it manually. You only need a Kaggle API token:
1. Go to [kaggle.com](https://www.kaggle.com) and log in
2. Click your profile picture → **Settings**
3. Scroll to the **API** section and click **Create New Token**
4. This downloads a file called `kaggle.json` to your computer

### 4. Run the notebook
Run all cells in order: **Runtime → Run all**

When the first code cell executes, it will prompt you to upload a file. Upload your `kaggle.json` at that point. The dataset will then be downloaded and unzipped automatically into the Colab runtime. No further manual steps are needed.

> **Note:** Training the CNN takes approximately 15–20 minutes. ResNet-18 Stage 1 + Stage 2 takes approximately 20–30 minutes, depending on GPU availability.

---

## Dependencies

All dependencies are either pre-installed in Google Colab or installed automatically via `pip` inside the notebook. No manual installation is required. The main libraries used are:

- `torch` and `torchvision`
- `numpy`, `pandas`, `matplotlib`, `seaborn`
- `scikit-learn`
- `Pillow`
- `grad-cam`
