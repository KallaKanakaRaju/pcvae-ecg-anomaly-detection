# pcvae-ecg-anomaly-detection
Physio-aware Contrastive Variational Autoencoder (P-CVAE) for unsupervised single-beat ECG anomaly detection using morphology-guided representation learning.
# P-CVAE: Physio-aware Contrastive Variational Autoencoder for ECG Anomaly Detection

This repository provides the official implementation of a **Physio-aware Contrastive Variational Autoencoder (P-CVAE)** for **unsupervised single-beat ECG anomaly detection**.  
The method integrates variational representation learning, contrastive regularization, and morphology-aware constraints to learn discriminative and physiologically meaningful latent embeddings using only normal ECG beats.

---

## 🔍 Overview

Electrocardiogram (ECG) anomaly detection is challenging due to limited labeled abnormal data and high inter-subject variability.  
The proposed P-CVAE addresses this by:

- Learning probabilistic latent representations via a VAE
- Structuring the latent space using contrastive (NT-Xent) learning
- Enforcing physiological consistency through a QRS template–based morphology loss
- Detecting anomalies using a composite score based on reconstruction error and latent deviation

---

## 🧠 Model Architecture

The P-CVAE consists of:
- Residual 1D CNN encoder
- Variational bottleneck (mean and log-variance estimation)
- Symmetric CNN decoder
- Composite loss function:
  - Reconstruction loss
  - KL divergence
  - Contrastive (NT-Xent) loss
  - Morphology-aware (QRS correlation) loss

---

## 📊 Key Features

- Fully **unsupervised training** (normal ECG beats only)
- **Physiology-aware learning** via QRS template alignment
- Robust **latent-space separability**
- Interpretable **anomaly scoring**
- CPU-safe and reproducible implementation

---

## 📁 Repository Structure

