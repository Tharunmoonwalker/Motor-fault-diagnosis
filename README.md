# Motor Fault Diagnosis using Acoustic Data 🎶⚙️

This project focuses on **motor fault diagnosis** using **acoustic signals**.  
Instead of relying on expensive vibration sensors, we leverage **sound recordings** from motors to identify and classify faults such as **bearing faults** and **electric corrosion**.

## 🚀 Project Overview
- Input: **Acoustic data → Mel Spectrogram Images (PNG motifs)**
- Models compared:
  - Temporal Convolutional Network (TCN)
  - Custom CNN
  - Transfer Learning (VGG16, ResNet50, MobileNetV2)
  - EfficientNetB0 (Final Model)
- Datasets:
  - **Healthy vs Unhealthy** (binary classification)
  - **Multifault** (multi-class classification)

## 🧠 Methodology
1. **Data Preprocessing**
   - Acoustic recordings were converted into **1-second Mel spectrograms**.
   - Stored as `.png` images for easier deep learning processing.

2. **Model Training**
   - TCN was tested directly on sequence data (overfitting observed).
   - CNNs and pretrained models (VGG16, ResNet50, MobileNetV2) were evaluated.
   - EfficientNetB0 achieved the **best performance** with ~93% accuracy.

3. **Evaluation**
   - Accuracy & Loss curves
   - Confusion Matrices
   - Comparison of models

## 📊 Results
| Model            | Healthy/Unhealthy | Multifault |
|------------------|------------------|------------|
| TCN              | Overfitting      | Overfitting|
| Custom CNN       | ~70%             | ~65%       |
| VGG16/ResNet50/MobileNetV2 | ~85% | ~80%       |
| **EfficientNetB0** | **93%**        | **88%**    |

## 🔮 Future Work
- Collect larger and more diverse datasets
- Improve robustness in noisy environments
- Deploy models for **real-time diagnosis** on industrial edge devices


## 🛠️ Tech Stack
- Python, TensorFlow/Keras
- NumPy, Matplotlib, scikit-learn
- Librosa (for audio preprocessing)
- Google Colab (training environment)

## 👨‍💻 Author
Developed by **[Your Name]** as part of Final Year Project.  
Focus: **Full-Stack Development + Machine Learning (R&D)**.  
Interested in **R&D roles in AI/ML and full-stack engineering** in Japan.  


# 音響データを用いたモータ故障診断 🎶⚙️

本プロジェクトは、**モータ故障診断**を目的としています。  
高価な振動センサを使わず、**モータの音**から故障を検出・分類します。  
対象となる故障例: **ベアリング故障**, **電気腐食** など。

## 🚀 プロジェクト概要
- 入力: **音響データ → メルスペクトログラム画像（PNGモチーフ）**
- 使用モデル:
  - 時系列畳み込みネットワーク (TCN)
  - カスタムCNN
  - 転移学習 (VGG16, ResNet50, MobileNetV2)
  - EfficientNetB0（最終モデル）
- データセット:
  - **Healthy vs Unhealthy** （2クラス分類）
  - **Multifault** （多クラス分類）

## 🧠 手法
1. **データ前処理**
   - 音響データを **1秒ごとのメルスペクトログラム** に変換
   - `.png` 画像として保存し、学習に使用

2. **モデル学習**
   - TCNはシーケンスデータで実験（過学習あり）
   - CNNおよび転移学習モデル (VGG16, ResNet50, MobileNetV2) を評価
   - EfficientNetB0 が最も高い精度 (~93%) を達成

3. **評価**
   - 精度・損失の学習曲線
   - 混同行列
   - モデル比較

## 📊 結果
| モデル                | Healthy/Unhealthy | Multifault |
|-----------------------|------------------|------------|
| TCN                   | 過学習           | 過学習     |
| カスタムCNN           | ~70%             | ~65%       |
| VGG16/ResNet50/MobileNetV2 | ~85%      | ~80%       |
| **EfficientNetB0**    | **93%**          | **88%**    |

## 🔮 今後の課題
- データセットの拡張と多様化
- ノイズ環境での頑健性向上
- **エッジデバイスでのリアルタイム診断** に対応


## 🛠️ 技術スタック
- Python, TensorFlow/Keras
- NumPy, Matplotlib, scikit-learn
- Librosa (音声前処理)
- Google Colab (学習環境)

## 👨‍💻 作者
**[Your Name]** が卒業研究の一環として開発。  
専門分野: **フルスタック開発 + 機械学習（R&D）**  
将来的に **日本でのAI/MLおよびフルスタック開発のR&D職** を希望。  
