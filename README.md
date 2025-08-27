## 🧪 Clustering-Based Identification of Sepsis and Non-Sepsis in ICU Patients

This repository contains the implementation and findings of an unsupervised clustering study aimed at distinguishing **sepsis** from **non-sepsis SIRS** (Systemic Inflammatory Response Syndrome) using routine clinical and laboratory data at ICU admission.

### 🎯 Project Aim

To evaluate whether combinations of readily available parameters — such as **CRP**, **APACHE II**, **SOFA**, **white blood cell counts**, and other hemogram markers — can effectively separate patients with **sepsis** from those with **non-septic SIRS**, using clustering algorithms.

---

### 🧬 Dataset Features

The analysis focuses on variables such as:

* **CRP** (C-Reactive Protein)
* **APACHE II** and **SOFA scores**
* **WBC**, **Neutrophil count (NeuC)**, **Lymphocyte count (LymC)**, **Platelet count (PLTc)**, **MPV**, **NLCR**
* **Sex**, **Age**, **Mortality**, **ICU Length of Stay**

---

### 🧠 Methods Used

Clustering was performed using:

* **K-Means**: Optimal k=2 (Silhouette score: 0.207)
* **Hierarchical Clustering** (Ward linkage)
* **DBSCAN** (ε = 3.58, minPts = 3)

---

### 🔍 Key Findings

* **Cluster 2 (C2)** consistently identified high-risk patients:

  * Higher **CRP**, **SOFA**, **APACHE II** scores
  * Higher **mortality**
  * Shorter ICU stay but elevated **NLCR**
* **Cluster 1 (C1)** grouped lower-risk patients with:

  * Lower inflammation/severity scores
  * Better clinical outcomes

> Not all variables were significant: **NeuC**, **LymC**, and **MPV** showed limited discriminative power.

---

### 📊 Visual Analysis

* **Scatter plots** (e.g., CRP vs APACHE II, SOFA vs WBC)
* **Box plots** (NeuC, LymC)
* **FreeViz plots** highlighting feature influence
* **Mortality-colored cluster plots** confirmed alignment between clustering and outcomes

---

### ✅ Conclusion

The study confirms that **unsupervised clustering** can reveal clinically meaningful patient groups in SIRS cases, especially when using multi-dimensional data. While some individual markers (like CRP or NeuC) are insufficient alone, combined variables can successfully stratify patients by sepsis risk.


