# ML-PredictiveAnalytics

## Domain Proyek
Topik yang diangkat dari proyek ini yaitu mengenai bidang ekonomi dan bisnis, di mana suatu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan mingguan.

### Latar Belakang
Memprediksi permintaan suatu produk dan menyimpannya sesuai kebutuhan dimasa yang akan datang merupakan hal penting dalam penjualan bisnis supermarket. Dengan prediksi yang akurat, dapat dicapai retensi pelanggan yang lebih baik, kepuasan pelanggan, dan menghindari situasi stok berlebihan dan kekurangan stok [[1]](https://ijcrt.org/papers/IJCRT22A6470.pdf)
to Markdown converter.

Salah satu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan dan permintaan dengan akurat. Ada beberapa acara dan hari libur yang mempengaruhi penjualan setiap harinya [[2]](https://www.kaggle.com/code/yasserh/walmart-sales-prediction-best-ml-algorithms). Pada project ini, akan dilakukan prediksi Machine Learning untuk penjualan mingguan pada supermarket Walmart.

## Business Understanding
### Problem Statement
1. Bagaimana mengidentifikasi kapan waktu tertentu yang mempengaruhi penjualan supermarket?
2. Apa faktor yang mempengaruhi penjualan dari suatu supermarket?
### Goals
1. Mengetahui pada waktu kapan penjualan supermarket cenderung lebih tinggi atau lebih rendah.
2. Mengetahui faktor apa saja yang mempengaruhi penjualan dari suatu toko supermarket
### Solution Statements
1. Memahami data dan memvisualisasikannya untuk mengetahui faktor seperti apa yang mempengaruhi penjualan supermarket.
2. Membangun model machine learning untuk memprediksi penjualan supermarket dan mengevaluasi model yang digunakan.

## Data Understanding
Dataset yang digunakan pada project ini berasal dari Kaggle oleh [M Yasser H](https://www.kaggle.com/yasserh) yang dapat diunduh pada tautan berikut [Walmart Dataset](https://www.kaggle.com/datasets/yasserh/walmart-dataset/data).

Dataset ini menyediakan data histori penjualan untuk 45 toko Walmart yang terletak di berbagai wilayah tersedia. Bisnis ini menghadapi tantangan akibat permintaan yang tidak terduga dan kadang-kadang kehabisan stok.

Berikut adalah informasi dataset: 
Dataset terdiri dari 6435 sampel dan 8 fitur. Data historis yang mencakup penjualan dari tanggal 5 Februari 2010 hingga 1 November 2012, dalam file Walmart_Store_sales. Dalam file ini, terdiri dari beberapa field berikut:
1. Store - nomor toko
2. Date - minggu penjualan
3. Weekly_Sales - penjualan untuk toko tertentu
4. Holiday_Flag - minggu tersebut adalah minggu libur khusus (1 – Minggu libur, 0 – Minggu bukan libur)
5. Temperature - suhu pada hari penjualan
6. Fuel_Price - Biaya bahan bakar di wilayah tersebut
7. CPI - Indeks harga konsumen yang berlaku
8. Unemployment - Tingkat pengangguran yang berlaku
9. Holiday Events\ Super Bowl: 12-Feb-10, 11-Feb-11, 10-Feb-12, 8-Feb-13\ Labour Day: 10-Sep-10, 9-Sep-11, 7-Sep-12, 6-Sep-13\ Thanksgiving: 26-Nov-10, 25-Nov-11, 23-Nov-12, 29-Nov-13\ Christmas: 31-Dec-10, 30-Dec-11, 28-Dec-12, 27-Dec-13

**Grafik Penjualan semua toko**
![download](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/9148711f-65db-4ef8-aa97-a0dad37f3eaf)
- Toko 4 dan 20 memiliki tingkat penjualan mingguan tertinggi
- Toko 5 dan 33 memiliki tingkat penjualan mingguan terendah
  
**Trend Penjualan Mingguan**
![download (1)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/f0712752-fa75-4996-bc99-8965bf2ae64c)

Grafik menunjukkan bahwa penjualan mingguan di Walmart umumnya tetap stabil sepanjang tahun, kecuali pada bulan November dan Desember yang mengalami peningkatan penjualan yang signifikan.

![download (2)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/36aa8c77-39f0-4aa8-8896-6facf0eb760f)

Kenaikan penjualan mingguan ini kemungkinan terjadi karena musim liburan Natal dan Akhir Tahun. Namun terjadi penurunan signifikan di bulan Januari, ini kemungkinan disebabkan karena event atau promo menarik telah dilaksanakan di dua bulan sebelumnya dan pelanggan telah menghabiskan uangnya di bulan November dan Desember.

## Data Preparation
- Melakukan pengecekan apakah ada missing values dan duplikasi pada data.
- Menghapus kolom yang tidak diperlukan pada tahapan modeling.
- Melakukan standarisasi pada data dengan menggunakan StandardScaler dari library sckit-learn.
- Melakukan split dataset dengan rasio 80:20. Proses ini dilakukan dengan menggunakan modul train_test_split dari library scikit-learn.
  
## Modeling
### Linear Regression
- Kelebihan: Mudah dipahami dan diinterpretasikan, efisien secara komputasional saat berurusan dengan dataset besar, dan tidak membuat asumsi tentang distribusi fitur.
- Kekurangan: mengasumsikan hubungan linear antara variabel independen dan dependen, sensitif terhadap outliers, kompleksitas terbatas, tidak cocok untuk data non-linear.
### Support Vector Machine
- Kelebihan: Efektif dalam ruang dimensi tinggi, tahan terhadap overfitting, kernel yang serbaguna, berfungsi baik dengan dataset kecil, optimalitas global.
- Kekurangan: Mahal secara komputasional, sensitif terhadap hiperparameter, sulit diinterpretasikan, membutuhkan banyak memori, kurangnya output probabilitas.
### Random Forest
- Kelebihan: Akurasi tinggi, ketangguhan terhadap outliers, pentingnya fitur, menangani data dimensi tinggi, hubungan non-linear.
- Kekurangan: Interpretabilitas model, kompleksitas komputasional, penggunaan memori, kecenderungan terhadap fitur dengan kardinalitas tinggi, penyetelan hiperparameter.

## Evaluation
Setelah beberapa model dibangun akan dilakukan perbandingan kinerja mereka menggunakan metrik Root Mean Square Error (RMSE). Nilai RMSE digunakan untuk membandingkan kinerja berbagai model dan menentukan model mana yang memiliki nilai error terendah dan memilih model yang terbaik untuk melakukan prediksi penjualan toko supermarket.

### Mean Squared Error (MSE)
MSE adalah rata-rata dari perbedaan kuadrat antara nilai yang diamati dan nilai yang diprediksi. MSE memberikan penalti yang lebih besar untuk kesalahan yang lebih besar dibandingkan dengan kesalahan yang lebih kecil, hal ini disebabkan oleh operasi pemangkatan dua.
MSE = Σ(yi − pi)2/n
### Root Mean Squared Error (RMSE)
RMSE adalah akar kuadrat dari MSE. RMSE sering digunakan karena memiliki unit yang sama dengan variabel target dan dapat diinterpretasikan dalam skala asli data.
RMSE = √(MSE)

Dimana:
- n: jumlah titik data (sampel)
- yᵢ: nilai yang diamati (aktual) dari variabel target untuk titik data ke-i
- pᵢ: nilai prediksi yang sesuai untuk yi

![Screenshot 2024-02-11 135724](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/3b48f9bd-5774-4bde-be87-11f6c0a43dca)

Dari tabel diatas menunjukkan Random Forest melebihi regressor lain dengan RMSE sebesar 1.14e+05. Ini memberikan perkiraan yang baik untuk penjualan di masa depan karena memiliki kesalahan rata-rata sekitar 11%.

![download (3)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/4faf48a5-6d5e-42d0-abbb-1e8698fe7bf1)

Dari hasil perbandingan ketiga model, RandomForest memiliki kinerja lebih baik daripada model lainnya. Namun, RandomForest memiliki kecenderungan terlalu overfitting pada model yang telah dibangun.

![Screenshot 2024-02-11 135732](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/8ad7761e-8204-4c66-ab6b-868ac471c1d1)

Dapat kita lihat bahwa prediksi dari ketiga algoritma yang paling mendekati y_true dengan 10 sampel data acak adalah prediksi Random Forest. Ini menandakan bahwa Random Forest merupakan algoritma terbaik dibandingkan dengan algoritma yang lain pada dataset Walmart.

### Kesimpulan

Penjualan selama minggu pada musim liburan secara signifikan lebih tinggi dibandingkan dengan minggu yang bukan pada musim liburan, dengan penjualan rata-rata meningkat dua kali lipat. Penjualan rata-rata toko tertinggi dapat mencapai hingga 500% lebih tinggi daripada toko yang paling rendah.

Model terbaik untuk memprediksi penjualan di masa depan adalah model Random Forest Regressor, yang mencapai nilai RMSE sebesar 1.14e+05. Ini merupakan perkiraan yang baik karena hanya terdapat selisih 88.5% dari nilai median penjualan data.












