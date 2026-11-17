Optimasi Prediksi Biaya Asuransi Kesehatan Tahunan Menggunakan Random Forest, ANN, dan Linear Regression
Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis dan memprediksi biaya asuransi kesehatan tahunan berdasarkan karakteristik individu menggunakan tiga pendekatan berbeda:

Linear Regression – metode statistik dasar untuk melihat hubungan linear antara fitur dan target.

Random Forest – algoritma ensemble learning yang menangani interaksi variabel kompleks dan tahan terhadap outlier.

Artificial Neural Network (ANN) – model deep learning untuk menangkap hubungan non-linear antar fitur.

Penelitian ini juga membahas efek penanganan outlier terhadap performa masing-masing model serta memberikan evaluasi awal untuk menentukan metode terbaik dalam memprediksi biaya medis tahunan.

Tim Penulis
- Refochella Florentine Gwacevo Pertiwi (24031554045)
- Stella Dagatha (24031554080)
- Gita Nurani (24031554122)
- Nadia Zahra Yuvina (24031554192)

Kelas: 2024 B
Dosen Pengampu: Kartika Chandra Dewi, S.Si., M.Si.
Program Studi: S1 Sains Data, FMIPA, Universitas Negeri Surabaya


Dataset
- Sumber: Kaggle – Medical Insurance Cost Prediction
- Jumlah Observasi: 100.000
- Jumlah Fitur: 54 (termasuk annual_medical_cost sebagai target)
- Jenis Fitur: Demografi, gaya hidup, rekam medis, utilitas layanan kesehatan, detail polis, klaim medis.


Preprocessing
- Handle Missing Value: Mengisi nilai hilang pada fitur kategorikal (alcohol_freq) dengan modus.
- Pengecekan Duplikasi: Menghapus data duplikat untuk menjaga integritas dataset.
- Handle Outlier: Dua skenario dibuat:
Skenario A (Optimasi): Outlier ditangani menggunakan log transform, winsorization, atau IQR capping sesuai skewness.
Skenario B (Baseline): Outlier dibiarkan pada kondisi asli.
- Feature Engineering: Kolom kategorikal diubah menjadi numerik menggunakan one-hot encoding.


Metodologi
- Train-Test Split
- Proporsi 80/20 menggunakan Stratified Regression Split berdasarkan quantile binning pada target annual_medical_cost.
- Scaling
- StandardScaler diterapkan pada fitur numerik agar rata-rata = 0 dan standar deviasi = 1.


Pemodelan
- Linear Regression: Baseline model.
- Random Forest: Ensemble learning dengan banyak decision tree.
- ANN (MLPRegressor): Deep learning dengan dua hidden layer.


Metrik Evaluasi
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE).