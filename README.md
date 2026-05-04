# 📊 UTS Data Mining - Advanced Feature Engineering & Modeling

## 📌 Deskripsi

Proyek ini merupakan tugas UTS Data Mining yang mengimplementasikan teknik:

* Data Preprocessing
* Feature Engineering
* Clustering
* Klasifikasi
* Regresi

Analisis dilakukan pada dataset Titanic untuk memahami pola data dan meningkatkan performa model machine learning.

---

## 🎯 Tujuan

* Membersihkan dan mempersiapkan data
* Melakukan feature engineering lanjutan
* Mengelompokkan data menggunakan clustering
* Membuat variabel target (Y) secara mandiri
* Membangun model klasifikasi dan regresi
* Membandingkan performa model

📊 Dataset

Dataset yang digunakan adalah Titanic: Machine Learning from Disaster, yang berisi informasi penumpang seperti:

Pclass
Sex
Age
Fare
Cabin
Embarked
Survived
---

## ⚙️ Metodologi dan Hasil

### 🔹 1. Data Preprocessing

* **Missing Values:**

  * `Age`: median berdasarkan `Pclass` & `Sex`
  * `Embarked`: diisi 'S'
  * `Fare`: median penumpang kelas 3 (solo traveler)
* **Encoding:** menggunakan `LabelEncoder`
* **Cleaning:**

  * `Cabin` dihapus (missing tinggi)
  * Diganti dengan fitur `Deck`

---

### 🔹 2. Feature Engineering

* **Transformasi:**

  * `Cabin` → `Deck` (A, B, C → ABC; D, E → DE; F, G → FG)
* **Fitur Baru:**

  * `Family_Size`
  * `Ticket_Frequency`
  * `Title`
  * `Is_Married`
  * `Family_Survival_Rate`
  * `Ticket_Survival_Rate`
  * `Survival_Rate`
  * `Survival_Rate_NA`
* **Binning:**

  * `Age` → 10 kategori
  * `Fare` → 13 kategori
* **Feature Selection:**

  * Menghapus fitur tidak relevan

---

### 🔹 3. Clustering

* **Metode:** K-Means
* **Optimal Cluster:** 3 (Elbow Method)
* **Fitur:**

  * Age, Fare, Ticket_Frequency, Survival_Rate
* **Hasil:**

  * Data terbagi menjadi 3 cluster

---

### 🔹 4. Pembentukan Variabel Target (Y)

* Target: `y_cluster_logic`
* Dibuat berdasarkan rata-rata survival tiap cluster

**Distribusi:**

* 0 (low survival): 788
* 1 (high survival): 103
* Mean: ~0.1156

---

### 🔹 5. Klasifikasi

**Model:**

* Decision Tree
* SVM
* KNN
* Logistic Regression
* Naive Bayes
* Random Forest

**Hasil Accuracy:**

* Decision Tree: **0.9529**
* SVM: 0.8799
* KNN: 0.8653
* Logistic Regression: 0.8631
* Naive Bayes: 0.8272

**Evaluasi:**

* Confusion Matrix
* Classification Report

---

### 🔹 6. Regresi

**Model:**

* Linear Regression
* Decision Tree Regression
* Random Forest Regression

**Hasil:**

| Model             | MAE    | MSE    | RMSE   | R2       |
| ----------------- | ------ | ------ | ------ | -------- |
| Linear Regression | 0.0000 | 0.0000 | 0.0000 | 1.0000   |
| Decision Tree     | 0.0000 | 0.0000 | 0.0000 | 1.0000   |
| Random Forest     | 0.0002 | 0.0000 | 0.0022 | 0.999951 |

---

### 🔹 7. Perbandingan Model

#### 📌 Klasifikasi

* Decision Tree memiliki akurasi tertinggi
* SVM, KNN, Logistic Regression lebih stabil (generalisasi lebih baik)

#### 📌 Regresi

* Semua model menunjukkan performa hampir sempurna
* Random Forest sedikit di bawah namun tetap sangat akurat

---

## 📈 Kesimpulan

* Feature engineering sangat meningkatkan kualitas data
* Clustering membantu memahami pola survival
* Target buatan (`y_cluster_logic`) sangat prediktif
* Model klasifikasi dan regresi menunjukkan performa tinggi
* Kombinasi metode menghasilkan analisis yang komprehensif

---

## 📂 Struktur File

* `UTS_Data_Mining.ipynb` → notebook analisis
* `README.md` → dokumentasi proyek

---

## 🚀 Cara Menjalankan

1. Buka notebook di Google Colab
2. Jalankan seluruh cell
3. Pastikan dataset tersedia

---

## 👤 Author

Nama: Ana Rufayda
NIM: 2304020152

