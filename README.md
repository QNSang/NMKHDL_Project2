# NMKHDL_Project2
Project on combining PCA using EM and Autoencoder mimicking PCA

# 🎓 PCA-EM & Constrained Autoencoder Project

## 📌 Overview

This project investigates scenarios where feature relationships are **non-linear** or **cluster-dependent**. We develop:
1. A method to combine **multiple PCA models** using the **EM (Expectation–Maximization)** algorithm.
2. A **constrained Autoencoder** (1-layer encoder, 1-layer decoder) that mimics PCA behavior.

---

## 👥 Team Members
- **[TRAN QUANG SANG]** – PCA + EM implementation (Python)
- **[NGUYEN HONG YEN]** – Constrained Autoencoder (PyTorch)

---

## 🧠 Objectives

- Simulate data with **multiple clusters** and **non-linear relationships**.
- Apply **PCA separately** on each cluster using **EM algorithm**.
- Train an **Autoencoder** that behaves similarly to PCA:
  - Linear encoder & decoder
  - Shared weights (`decoder = encoder.T`)
  - No non-linear activation

---

## 🧱 Project Structure

```bash
pca-em-autoencoder/
├── data/                   # Dữ liệu mô phỏng và lưu output
│   ├── generate_data.py    # File tạo dữ liệu nhiều cụm, phi tuyến
│   └── simulated_data.npy  # File lưu dữ liệu đầu ra
├── pca_em/                 # Phần PCA + EM algorithm
│   ├── pca_em.py           # Cài đặt EM và multiple PCA
│   ├── utils.py            # Hàm phụ trợ: PCA, chuẩn hóa, visualize
│   └── evaluate_em.py      # So sánh kết quả phân cụm
├── autoencoder/            # Mô hình Autoencoder (PyTorch)
│   ├── model.py            # Định nghĩa encoder + decoder
│   ├── train.py            # Huấn luyện AE
│   └── evaluate_ae.py      # Đánh giá AE vs PCA
├── plots/                  # Biểu đồ, hình ảnh trực quan hóa
│   ├── clusters_pca.png
│   └── loss_plot.png
├── report/                 # Tài liệu báo cáo
│   ├── report_draft.md
│   └── references.bib
├── requirements.txt        # Thư viện cần cài
├── README.md               # Mô tả tổng quan project
└── .gitignore              # Bỏ qua file không cần push
