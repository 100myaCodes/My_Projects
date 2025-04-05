# Deep Learning-Based Multi-Omics Integration for Cancer Subtyping

This repository presents a research project that applies **deep learning and multi-omics integration** to identify clinically relevant **cancer subtypes**. By combining transcriptomic, methylomic, and copy number variation data using **autoencoder architectures**, the model discovers latent representations that enhance cancer stratification and survival prediction.

---

# Project Objectives

- Integrate multi-omics data (RNA-seq, DNA methylation, CNV) from **TCGA Breast Cancer (BRCA)** samples.
- Train unsupervised deep learning models (autoencoders) to reduce noise and learn biological signals.
- Cluster patients into **distinct subtypes** using learned latent features.
- Evaluate subtype relevance using **t-SNE visualization** and **Kaplan-Meier survival analysis**.

---

# Methodology

🔹 Data Source
- [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/tcga)
- Omics types:
  - Gene expression (RNA-seq)
  - DNA methylation (450K array)
  - Copy number variation (CNV)

🔹 Model Pipeline

1. Data Preprocessing:
   - Normalization, missing value imputation, PCA for dimensionality reduction.
2. Multi-modal Autoencoder:
   - Separate encoders for each omics type → shared latent space.
3. Clustering:
   - K-Means and Deep Embedded Clustering (DEC).
4. Evaluation:
   - t-SNE cluster plots
   - Survival analysis with Kaplan-Meier curves

<p align="center">
  <img src="A_flowchart-style_diagram_illustrates_a_machine_le.png" width="600"/>
</p>

---

# Key Results

- **t-SNE Clustering** revealed 3 biologically meaningful clusters:
  <p align="center"><img src="tsne_clusters.png" width="500"/></p>

- **Survival curves** show significant differences between clusters:
  <p align="center"><img src="survival_curve_simulated.png" width="500"/></p>

- **Cluster Summary Table**:
  <p align="center"><img src="cluster_comparison_table.png" width="500"/></p>

---

# Tools & Libraries

- Python, NumPy, Pandas
- Scikit-learn
- TensorFlow / Keras
- Seaborn, Matplotlib
- DeepChem (for omics processing)

---

# Future Work

- Extend pipeline to other cancer types (e.g., lung, colon).
- Integrate additional omics: proteomics, metabolomics.
- Add explainability (e.g., SHAP, attention).
- Deploy as a web tool for oncologists.

---

# License

This project is for educational and research purposes. Please cite appropriately if used.

---

# Acknowledgments

Thanks to the TCGA Research Network and the authors of **"Deep Learning for the Life Sciences"** and **DeepChem** for foundational concepts.

