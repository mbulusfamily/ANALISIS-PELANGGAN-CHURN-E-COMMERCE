# ANALISIS-PELANGGAN-CHURN-E-COMMERCE

## Ringkasan Proyek

Repository ini berisi notebook Jupyter yang mendemonstrasikan proses analisis data, pengolahan, dan pembuatan model machine learning untuk memprediksi kemungkinan pelanggan loyal e-commerce melakukan churn (berhenti berlangganan atau tidak lagi melakukan pembelian). Dengan pendekatan analisis data modern dan pemanfaatan algoritma klasifikasi, proyek ini bertujuan membantu bisnis e-commerce dalam memahami perilaku pelanggan serta mengambil langkah strategis untuk meningkatkan retensi dan ROI (Return on Investment).

---

## Latar Belakang

Churn pelanggan adalah fenomena di mana pelanggan berhenti menggunakan layanan atau produk dari suatu perusahaan. Dalam industri e-commerce, tingkat churn yang tinggi dapat berdampak signifikan terhadap pendapatan dan pertumbuhan jangka panjang. Prediksi churn yang akurat memungkinkan perusahaan untuk merancang intervensi yang tepat, seperti program loyalitas, penawaran khusus, atau peningkatan layanan pelanggan.

---

## Tujuan dan Manfaat

- Memprediksi kemungkinan pelanggan loyal melakukan churn.
- Mengidentifikasi fitur utama yang berkontribusi terhadap perilaku churn.
- Membandingkan performa beberapa algoritma machine learning dalam klasifikasi churn.
- Memberikan rekomendasi bisnis yang berbasis data untuk meningkatkan retensi pelanggan.
- Membantu tim data dan bisnis dalam membangun pipeline prediksi churn yang siap produksi.

---

## Metodologi

### 1. Eksplorasi Data Awal (EDA)
- Pemeriksaan kualitas data, missing value, dan outlier.
- Analisis distribusi variabel dan korelasi antar fitur.
- Visualisasi data untuk menemukan pola yang relevan dengan churn.

### 2. Preprocessing Data
- Penanganan missing value dan outlier.
- Encoding variabel kategorikal (One-Hot, Label Encoding).
- Normalisasi dan standarisasi fitur numerik.
- Feature selection dan engineering.

### 3. Pemodelan Machine Learning
- Split data menjadi data latih dan data uji.
- Implementasi tiga algoritma utama:
  - **Logistic Regression**: Model baseline.
  - **Random Forest**: Algoritma ensemble untuk menangani non-linearitas.
  - **XGBoost**: Algoritma boosting yang powerful untuk data tabular.
- Tuning hyperparameter dan cross-validation.

### 4. Evaluasi Model
- Penggunaan metrik accuracy, precision, recall, F1-score, ROC-AUC.
- Analisis confusion matrix untuk memahami tipe kesalahan.
- Interpretasi feature importance.

### 5. Insight Bisnis dan Rekomendasi
- Identifikasi fitur yang paling berpengaruh terhadap churn.
- Rekomendasi strategi bisnis untuk retensi pelanggan.

---

## Struktur Direktori

- `notebooks/` : Notebook utama untuk analisis, visualisasi, dan pemodelan.
- `data/` : Dataset pelanggan e-commerce (pastikan privasi dan keamanan data).
- `scripts/` : Script pendukung preprocessing dan evaluasi.
- `requirements.txt` : Daftar dependencies Python.
- `README.md` : Dokumentasi lengkap proyek.
- `output/` : Hasil model, grafik, dan laporan evaluasi.

---

## Instalasi & Cara Penggunaan

### Prasyarat
- Python >= 3.8
- Jupyter Notebook / JupyterLab
- Paket-paket yang tercantum dalam `requirements.txt`

### Langkah-langkah
1. **Clone Repository**
   ```bash
   git clone https://github.com/mbulusfamily/ANALISIS-PELANGGAN-CHURN-E-COMMERCE.git
   cd ANALISIS-PELANGGAN-CHURN-E-COMMERCE
   ```
2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Jalankan Notebook**
   - Buka Jupyter Notebook/JupyterLab.
   - Jalankan notebook di folder `notebooks/`.
   - Ikuti instruksi dan cell secara berurutan.

---

## Library yang Digunakan

- **Pandas, NumPy**: Manipulasi data dan analisis numerik.
- **Matplotlib, Seaborn**: Visualisasi data.
- **Scikit-learn**: Preprocessing, pemodelan, dan evaluasi machine learning.
- **XGBoost**: Implementasi algoritma boosting.
- **Imbalanced-learn**: Penanganan data imbalance (jika diperlukan).

---

## Hasil Analisis dan Pemodelan

Berikut adalah ringkasan hasil utama dari notebook analisis:

### 1. Eksplorasi Data

- Data terdiri atas berbagai fitur terkait transaksi, frekuensi pembelian, interaksi dengan platform, umur akun, dan lain-lain.
- Visualisasi menunjukkan pola tertentu, misalnya pelanggan dengan frekuensi pembelian rendah cenderung lebih mudah churn.
- Korelasi ditemukan antara beberapa fitur dan label churn.

### 2. Preprocessing

- Missing value berhasil ditangani tanpa mengurangi kualitas data.
- Outlier pada fitur numerik diproses sehingga distribusi data menjadi lebih normal.
- Encoding fitur kategorikal meningkatkan akurasi model.

### 3. Pemodelan & Evaluasi

| Model                | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|----------------------|----------|-----------|--------|----------|---------|
| Logistic Regression  | 0.82     | 0.79      | 0.73   | 0.76     | 0.80    |
| Random Forest        | 0.87     | 0.84      | 0.81   | 0.82     | 0.88    |
| XGBoost              | 0.89     | 0.87      | 0.83   | 0.85     | 0.90    |

- **XGBoost** menjadi model terbaik berdasarkan metrik evaluasi, dengan nilai ROC-AUC tertinggi.
- Feature importance menunjukkan fitur 'total_purchase', 'days_since_last_purchase', dan 'is_active_member' sebagai faktor kunci prediksi churn.

### 4. Insight Bisnis

- Pelanggan dengan interaksi rendah dan frekuensi pembelian minim memiliki risiko churn tinggi.
- Program loyalitas dan personalisasi penawaran dapat meningkatkan retensi.
- Segmen pelanggan aktif perlu dipertahankan dengan komunikasi reguler dan penawaran khusus.

### 5. Visualisasi

- Grafik ROC curve, confusion matrix, dan feature importance tersedia di folder output/notebooks.
- Visualisasi memungkinkan tim bisnis memahami hasil model secara intuitif.

---

## Kontribusi

Kontribusi terbuka bagi siapa saja untuk pengembangan fitur baru, penambahan algoritma, perbaikan bug, atau dokumentasi. Silakan lakukan fork, buat branch baru, dan ajukan pull request. Setiap masukan sangat diapresiasi!

---

## Lisensi

Proyek ini didistribusikan dengan lisensi MIT. Silakan gunakan dan modifikasi sesuai kebutuhan, dengan mencantumkan atribusi kepada pemilik repository.

---

## Catatan Privasi Data

Pastikan dataset yang digunakan sudah dianonimkan dan tidak mengandung data sensitif pelanggan. Semua file contoh dalam repository ini telah melalui proses sanitasi data.

---

## FAQ

**Q: Dapatkah notebook ini digunakan untuk data e-commerce lain?**  
A: Ya, struktur notebook bersifat generik dan dapat diadaptasi untuk dataset e-commerce lain dengan penyesuaian fitur.

**Q: Apa langkah selanjutnya setelah mendapatkan model terbaik?**  
A: Model dapat diekspor dan diintegrasikan ke dalam sistem produksi (misalnya API atau dashboard internal).

**Q: Bagaimana jika data sangat imbalance?**  
A: Gunakan teknik sampling (oversampling/undersampling) atau library `imbalanced-learn`.

---

## Kontak & Diskusi

Untuk pertanyaan, diskusi, atau saran, silakan buka [GitHub Issues](https://github.com/mbulusfamily/ANALISIS-PELANGGAN-CHURN-E-COMMERCE/issues) atau hubungi email di profil pemilik repository.

---

Selamat menggunakan repository ini dan semoga membantu pengembangan bisnis e-commerce Anda dalam mengurangi churn pelanggan dan meningkatkan retensi!
