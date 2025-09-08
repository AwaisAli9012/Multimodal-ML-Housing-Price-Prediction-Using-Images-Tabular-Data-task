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
