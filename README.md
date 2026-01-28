# 📱 Analisis Sentimen Ulasan iPhone: Mengungkap "Hype vs Realita"

Dataset:
https://www.kaggle.com/datasets/mrmars1010/iphone-customer-reviews-nlp

## 📌 Tentang Proyek
Proyek ini bertujuan untuk melakukan **Analisis Sentimen** terhadap ribuan ulasan pengguna iPhone menggunakan algoritma **Support Vector Machine (SVM)**. 

Fokus utama analisis ini bukan hanya pada akurasi model, tetapi juga pada analisis bisnis **"Hype vs Realita"**:
* **Hype:** Apakah klaim pemasaran Apple (Kamera & Baterai) divalidasi oleh pengguna?
* **Realita:** Adakah masalah teknis tersembunyi yang sering dikeluhkan namun jarang dibahas di iklan?

## 📊 Insight Bisnis Utama (Hype vs Realita)
Berdasarkan hasil Text Mining dan visualisasi WordCloud, ditemukan fakta menarik:
1.  ✅ **Validasi Hype:** Kata kunci **"Camera"** dan **"Battery"** mendominasi ulasan Positif. Pengguna memvalidasi kualitas fitur unggulan ini.
2.  ⚠️ **Realita Tersembunyi:** Kata kunci **"Heating" (Panas)** dan **"Overheating"** mendominasi ulasan Negatif. Ini mengindikasikan adanya isu manajemen suhu yang signifikan pada perangkat.

## 🛠️ Metodologi & Tahapan
Proyek ini mengikuti alur kerja Data Science standar:
1.  **Data Cleaning:** Pembersihan data (hapus missing values, regex cleaning).
2.  **Preprocessing:** * Case Folding
    * Stopword Removal
    * **Lemmatization** (Mengubah kata ke bentuk dasar, misal: *Batteries* -> *Battery*).
    * Labeling (Rating 4-5: Positif, 1-2: Negatif).
3.  **Feature Extraction:** Menggunakan **TF-IDF**.
4.  **Feature Selection:** Menggunakan **Chi-Square** untuk mereduksi fitur dari **5.000 menjadi 2.000 fitur terbaik**.
5.  **Modeling:** Algoritma **SVM (Support Vector Machine)** dengan **Kernel Linear**.

## 📈 Performa Model
Model dievaluasi menggunakan data testing (20%) dengan hasil sebagai berikut:

| Metrik | Nilai | Keterangan |
| :--- | :--- | :--- |
| **Akurasi** | **88.52%** | Model sangat handal dalam memprediksi sentimen secara umum. |
| **Precision (Negatif)** | **91%** | Model memiliki kemampuan sangat tinggi dalam mendeteksi keluhan/komplain nyata (minim False Positive). |

## 📂 Struktur File
* `UAS_ZULFA_5512.ipynb`: Notebook utama berisi seluruh kode (End-to-End).
* `iphone.csv`: Dataset ulasan pengguna (sumber: Kaggle).
* `svm_model.pkl`: Model SVM yang sudah dilatih (Saved Model).
* `tfidf_vectorizer.pkl`: Vectorizer untuk konversi teks ke angka.
* `chi2.pkl`: Model seleksi fitur Chi-Square.

## 🚀 Cara Menjalankan (Installation)
1.  Clone repository ini:
    ```bash
    git clone https://github.com/ulpaav/Sentiment-Analysis-iPhone-SVM.git
    ```
2.  Install library yang dibutuhkan:
    ```bash
    pip install -r requirements.txt
    ```
3.  Jalankan Notebook `UAS_ZULFA_23.11.5512.ipynb`

## 👤 Author
**Zulfa Meydita Rahma** S1 Informatika - Universitas Amikom Yogyakarta  
NIM: 23.11.5512  
Mata Kuliah: Big Data & Data Mining