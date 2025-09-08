# 🏡 Multimodal Housing Price Prediction

> **Predict house prices using both images + tabular data**  
> A PyTorch-based multimodal deep learning project combining CNN (images) + MLP (tabular) for regression.

---

## 🎯 Objective

Build a model that predicts housing prices by **fusing two data modalities**:
- 🖼️ **House Images** → processed via CNN (ResNet18)
- 📊 **Tabular Features** → bedrooms, bathrooms, sqft, age, neighborhood rating → processed via MLP
- ➕ **Fused** → concatenated features → final regression head
- 📉 **Evaluated** using MAE & RMSE

---

## 🧰 Tech Stack

- **Framework**: PyTorch
- **CNN Backbone**: ResNet18 (pretrained, feature extractor)
- **Tabular MLP**: Custom 2-layer network
- **Fusion**: Feature concatenation + regression head
- **Data Loading**: Custom `Dataset` + `DataLoader`
- **Image Preprocessing**: Resize, Normalize (ImageNet stats)
- **Evaluation**: MAE, RMSE (scikit-learn)

---

## 📁 Project Structure
profile
Qwen3-Max-Preview
11:20 pm
Actually, you meant README.md — the Markdown file for GitHub/project docs 😊
There’s no such thing as readme.d — that’s not a standard file.

✅ Here’s Your Complete, Polished, Ready-to-Use README.md
📄 Copy-paste this entire block into a file named README.md in your project root:

markdown


1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
⌄
⌄
⌄
# 🏡 Multimodal Housing Price Prediction with Images + Tabular Data

> **“What if AI could look at a house photo AND read its specs to predict price?”**  
> This project combines **Convolutional Neural Networks (CNNs)** for images and **MLP** for tabular data to predict housing prices — a true multimodal deep learning system built in PyTorch.

---

## 🎯 Task Objective

As part of a machine learning assignment, this project fulfills the following:

- ✅ Use **CNNs to extract features from house images**
- ✅ **Combine image features with tabular data** (bedrooms, sqft, age, etc.)
- ✅ **Train a fused model** using both modalities
- ✅ **Evaluate performance** using MAE and RMSE

Perfect for learning **multimodal ML, CNNs, feature fusion, and regression modeling**.

---

## 🧠 Model Architecture

[House Image] ────> [ResNet18] ───────┐
├─> [Concatenate] ──> [Fusion MLP] ──> [Predicted Price]
[Tabular Data] ─> [2-Layer MLP] ──────┘



1
2
3
4
5
6
7
8
9
10
11

- **Image Branch**: Pretrained ResNet18 → removes final layer → outputs 512-dim feature vector
- **Tabular Branch**: 5 features → Linear(64) → ReLU → Linear(32) → ReLU
- **Fusion**: Concatenate 512 + 32 → Linear(128) → ReLU → Linear(1) → Predicted Price
- **Loss**: MSELoss
- **Optimizer**: Adam (lr=1e-4)

---

## 📁 Project Structure

my_first_project/
├── data/
│ ├── housing_data.csv # 100 realistic house listings
│ └── images/ # 100 generated placeholder images (RGB 224x224)
│ ├── house_001.jpg
│ └── ...
├── generate_images.py # Script to generate placeholder house images
├── multimodal_housing.py # Main training script (run this!)
├── dvh2_3.ipynb # Jupyter notebook version (optional)
└── README.md # This file — your project’s front page!

