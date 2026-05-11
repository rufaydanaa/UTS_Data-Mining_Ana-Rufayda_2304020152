📊 Wine Quality Prediction - Classification Task

📌 **Deskripsi**

Proyek ini bertujuan untuk memprediksi kualitas wine menggunakan berbagai fitur fisikokimia. Variabel target, 'quality', telah dibagi menjadi dua kategori: wine berkualitas rendah (0) dan wine berkualitas tinggi (1). Analisis dilakukan untuk membangun dan mengevaluasi model klasifikasi untuk tugas ini.

🎯 **Tujuan**
*   Membersihkan dan mempersiapkan data.
*   Melakukan eksplorasi dan visualisasi data untuk memahami distribusi dan hubungan antar variabel.
*   Membagi variabel `quality` menjadi biner (0 dan 1) untuk tugas klasifikasi.
*   Membangun dan mengevaluasi model klasifikasi (K-Nearest Neighbors, Gradient Boosting Machines, Light Gradient Boosting Machine).
*   Melakukan tuning hyperparameter untuk model klasifikasi.
*   Memprediksi kualitas wine pada data pengujian.

📊 **Dataset**

Dataset yang digunakan adalah Wine Quality, yang berisi informasi tentang berbagai atribut wine seperti:
*   `fixed acidity`
*   `volatile acidity`
*   `citric acid`
*   `residual sugar`
*   `chlorides`
*   `free sulfur dioxide`
*   `total sulfur dioxide`
*   `density`
*   `pH`
*   `sulphates`
*   `alcohol`
Variabel target adalah `quality`.

⚙️ **Metodologi dan Hasil**
🔹 **1. Data Preprocessing**
*   **Missing Values**: Dataset tidak memiliki nilai kosong (null values).
*   **Variabel Target**: Variabel `quality` yang awalnya memiliki rentang 3-8, diubah menjadi masalah klasifikasi biner: `0` untuk kualitas rendah (3-5) dan `1` untuk kualitas tinggi (6-8).
*   **Pembagian Data**: Data dibagi menjadi set pelatihan (75%) dan pengujian (25%) menggunakan stratifikasi pada variabel `quality` untuk menjaga proporsi kelas.
*   **Standardisasi**: Fitur dinormalisasi menggunakan `MinMaxScaler` agar nilainya berada dalam rentang [0, 1].

🔹 **2. Eksplorasi Data (EDA) & Visualisasi**
*   Mengamati distribusi data menggunakan histogram dan kepadatan kernel.
*   Mengidentifikasi multikolinearitas antar fitur dengan pairplot dan heatmap korelasi.
*   Menganalisis hubungan antar variabel menggunakan scatterplot dan regplot.
*   Visualisasi interaktif menggunakan Plotly Express.

🔹 **3. Klasifikasi**
*   **Model**:
    *   K-Nearest Neighbors (KNN)
    *   Gradient Boosting Machines (GBM)
    *   Light Gradient Boosting Machine (LightGBM)
*   **Hyperparameter Tuning**: Dilakukan menggunakan `GridSearchCV` untuk setiap model guna menemukan parameter terbaik.
*   **Hasil Accuracy (pada test set)**:
    *   KNN: 0.465
    *   GBM: 0.521
    *   LightGBM: 0.465
*   **Evaluasi**: Dilakukan menggunakan *accuracy score*, *classification report* (precision, recall, f1-score), dan *ROC AUC* (khusus LightGBM).

📈 **Kesimpulan**
*   Notebook ini berhasil menerapkan model klasifikasi untuk memprediksi kualitas wine berdasarkan fitur fisikokimia.
*   Multikolinearitas antar fitur diidentifikasi dan perlu dipertimbangkan lebih lanjut.
*   Model GBM menunjukkan akurasi tertinggi di antara model yang diuji (0.521).
*   ROC AUC untuk LightGBM juga dianalisis untuk memahami performa model.

📂 **Struktur File**
*   `wine_quality_prediction.ipynb` → notebook analisis
*   `README.md` → dokumentasi proyek

🚀 **Cara Menjalankan**
1.  Buka notebook di Google Colab.
2.  Jalankan seluruh cell.
3.  Pastikan dataset `data_training.csv` dan `data_testing.csv` tersedia di lingkungan Colab (`/content/`).

👤 **Author**
Nama: Ana Rufayda NIM: 2304020152

LINK GOOGLE COLAB: https://colab.research.google.com/drive/152FdVGdtyTH4gmkr7hT6zUFn_HuL_wO8?usp=sharing
