# Financial Transaction Analysis: Customer Profiling & Classification

Proyek ini adalah submission akhir untuk kelas **"Belajar Machine Learning untuk Pemula"** di Dicoding. [cite_start]Proyek ini mendemonstrasikan penerapan pipeline Machine Learning yang lengkap, mulai dari eksplorasi data, pengelompokan (*clustering*) nasabah, hingga pembangunan model prediksi (*classification*)[cite: 293, 822].

## 📌 Deskripsi Proyek
[cite_start]Dataset ini mencakup 2.512 sampel transaksi yang berisi informasi mendalam mengenai perilaku keuangan, demografi nasabah, dan pola penggunaan[cite: 276, 277]. [cite_start]Tujuan utamanya adalah mengidentifikasi segmen nasabah untuk mendukung analisis keamanan finansial dan pengembangan model prediktif[cite: 275].

### Alur Kerja (Workflow)

#### 1. Eksplorasi & Pembersihan Data (EDA & Preprocessing)
* [cite_start]**Pembersihan**: Menangani data hilang (*missing values*) menggunakan `dropna()` dan menghapus data duplikat[cite: 825, 849, 859].
* [cite_start]**Seleksi Fitur**: Menghapus kolom yang tidak relevan seperti ID, alamat IP, dan tanggal[cite: 827, 865, 879].
* [cite_start]**Outlier Handling**: (Advanced) Menggunakan metode Interquartile Range (IQR) untuk memfilter data pencilan[cite: 931, 944].
* [cite_start]**Encoding**: Mengubah data kategorikal menjadi numerik menggunakan `LabelEncoder` dan melakukan *binning* pada fitur usia[cite: 828, 897, 963, 979].
* [cite_start]**Scaling**: Menstandardisasi fitur numerik menggunakan `StandardScaler` agar memiliki skala yang seragam[cite: 301, 950, 955].

#### 2. Clustering (Unsupervised Learning)
* [cite_start]**Elbow Method**: Menentukan jumlah cluster optimal ($k=2$) menggunakan `KElbowVisualizer` dengan metrik *Silhouette Score*[cite: 1007, 1011, 1024].
* [cite_start]**K-Means**: Mengimplementasikan algoritma K-Means untuk segmentasi nasabah[cite: 1055, 1059].
* [cite_start]**Visualisasi PCA**: Menggunakan *Principal Component Analysis* (PCA) untuk memvisualisasikan hasil cluster dalam ruang 2 dimensi[cite: 1085, 1103].

#### 3. Classification (Supervised Learning)
* [cite_start]**Model**: Membangun model prediksi berdasarkan label cluster menggunakan **Decision Tree** dan **Random Forest**[cite: 82, 105, 111].
* [cite_start]**Optimasi**: Melakukan *Hyperparameter Tuning* dengan `GridSearchCV` untuk mendapatkan performa model terbaik[cite: 107, 190, 205].
* [cite_start]**Evaluasi**: Model mencapai akurasi, presisi, dan recall sebesar **1.00** pada data uji[cite: 146, 173].

## 📊 Interpretasi Cluster
[cite_start]Berdasarkan hasil analisis, nasabah terbagi menjadi dua kelompok[cite: 1217, 1218]:

| Cluster | Profil Nasabah | Karakteristik (Scaled) |
| :--- | :--- | :--- |
| **Cluster 1** | Nasabah Muda Aktif | [cite_start]Usia dan saldo di bawah rata-rata, namun aktivitas transaksi sedikit lebih tinggi[cite: 1219, 1225, 1226]. |
| **Cluster 0** | Nasabah Senior Konservatif | [cite_start]Usia dan saldo di atas rata-rata, namun perilaku transaksi lebih rendah/hati-hati[cite: 1227, 1233, 1234]. |

## 🛠️ Teknologi yang Digunakan
* **Bahasa**: Python
* **Library Utama**:
    * [cite_start]Data Analysis: `pandas`, `numpy` [cite: 297, 298]
    * [cite_start]Visualization: `matplotlib`, `seaborn`, `yellowbrick` [cite: 299, 300, 305]
    * [cite_start]Machine Learning: `scikit-learn` [cite: 301, 302, 303]
    * [cite_start]Model Saving: `joblib` [cite: 306]

---
**Yehezkiel Athanasius Manurung (Anju)**
*Mahasiswa Informatika - Universitas Gunadarma*
