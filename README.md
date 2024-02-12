# ML-PredictiveAnalytics

## Domain Proyek
Topik yang diangkat dari proyek ini yaitu mengenai bidang ekonomi dan bisnis, di mana suatu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan mingguan.

### Latar Belakang
Memprediksi permintaan suatu produk dan menyimpannya sesuai kebutuhan dimasa yang akan datang merupakan hal penting dalam penjualan bisnis supermarket. Dengan prediksi yang akurat, dapat dicapai retensi pelanggan yang lebih baik, kepuasan pelanggan, dan menghindari situasi stok berlebihan dan kekurangan stok [[1]](https://ijcrt.org/papers/IJCRT22A6470.pdf).

Salah satu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan dan permintaan dengan akurat. Ada beberapa acara dan hari libur yang mempengaruhi penjualan setiap harinya [[2]](https://www.kaggle.com/code/yasserh/walmart-sales-prediction-best-ml-algorithms). Pada project ini, akan dilakukan prediksi Machine Learning untuk penjualan mingguan pada supermarket Walmart. Diharapkan prediksi ini bisa menjadi acuan penting bagi bisnis karena dapat memberikan informasi dalam pengambilan keputusan mengenai inventaris, staf, dan upaya pemasaran. Dengan memahami faktor-faktor yang mendorong penjualan dan menggunakan model yang andal untuk memperkirakan penjualan di masa depan, bisnis supermarket Walmart dapat merencanakan masa depan dengan lebih baik, mengoptimalkan sumber daya, dan mendatangkan keuntungan lebih banyak [[3]](https://eprajournals.com/IJSR/article/11646/abstract).

## Business Understanding
### Problem Statement
1. Bagaimana mengidentifikasi kapan waktu tertentu yang mempengaruhi penjualan supermarket?
2. Bagaimana meningkatkan prediksi penjualan di masa depan berdasarkan faktor-faktor yang ada?
### Goals
1. Menganalisis dan mengidentifikasi pola kapan penjualan supermarket cenderung lebih tinggi atau lebih rendah.
2. Mengetahui  faktor-faktor yang memengaruhi tingkat penjualan, dengan tujuan meningkatkan prediksi penjualan dengan tingkat kesalahan lebih kecil.
### Solution Statements
1. Melakukan eksplorasi data dan visualisasi untuk memahami hubungan antara waktu tertentu dan penjualan supermarket, serta variabel-variabel lain yang berpotensi mempengaruhi penjualan.
2. Membangun model machine learning untuk memprediksi penjualan supermarket dengan menggunakan variabel-variabel yang diidentifikasi sebelumnya.
3. Melakukan evaluasi model dengan menggunakan metrik seperti Mean Squared Error (MSE) dan Root Mean Square Error (RMSE) untuk menilai sejauh mana model dapat menghasilkan prediksi yang akurat.

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

Gambar 1. Grafik Penjualan semua toko
- Toko 4 dan 20 memiliki tingkat penjualan mingguan tertinggi
- Toko 5 dan 33 memiliki tingkat penjualan mingguan terendah
  
**Trend Penjualan Mingguan**
![download (1)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/f0712752-fa75-4996-bc99-8965bf2ae64c)

Gambar 2. Trend Penjualan Mingguan

Gambar 2 menunjukkan bahwa penjualan mingguan di Walmart umumnya tetap stabil sepanjang tahun, kecuali pada bulan November dan Desember yang mengalami peningkatan penjualan yang signifikan.

![download (2)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/36aa8c77-39f0-4aa8-8896-6facf0eb760f)

Gambar 3. Penjualan Mingguan Setiap Bulan
Kenaikan penjualan mingguan ini kemungkinan terjadi karena musim liburan Natal dan Akhir Tahun. Namun terjadi penurunan signifikan di bulan Januari, ini kemungkinan disebabkan karena event atau promo menarik telah dilaksanakan di dua bulan sebelumnya dan pelanggan telah menghabiskan uangnya di bulan November dan Desember.

**Hubungan Antara Fitur Sales dengan Unemployment Rate dan CPI** 
![unemployment](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/28d95ddd-d7ec-4219-89f3-6a5988268e20)

Gambar 4. Penjualan terhadap Tingkat Pengangguran
Penjualan dipengaruhi oleh tingkat pengangguran, sehingga semakin tinggi tingkat pengangguran, semakin rendah penjualan.

![CPI](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/af5eceec-a69b-465c-ac56-b84451f6204f)

Gambar 5. Penjualan terhadap CPI
Penyusutan Indeks Harga Konsumen (CPI) tidak mempengaruhi penjualan. Berdasarkan distribusi rata-rata harga konsumen di atas, pelanggan dapat dibagi menjadi dua kategori:
- Pelanggan yang membayar antara 120 hingga 150 (pelanggan kelas menengah).
- Pelanggan yang membayar antara 180 hingga 230 (pelanggan kelas atas).

## Data Preparation
- Memeriksa apakah ada missing values dengan mengecek setiap sel dalam dataset yang memiliki nilai kosong dan duplikasi pada data. Jika ada, maka missing values dan data yang duplikat akan dihapus.
- Menghapus kolom yang tidak diperlukan pada tahapan modeling.
- Melakukan standarisasi pada data dengan menggunakan StandardScaler dari _library_ sckit-learn.
- Melakukan split dataset dengan rasio 80:20. Proses ini dilakukan dengan menggunakan modul train_test_split dari _library_ scikit-learn.
  
## Modeling
### Linear Regression
Linear Regression mengasumsikan hubungan linear antara variabel independen (fitur) dan variabel dependen (target). Algoritma ini memiliki parameter yang paling penting yaitu fit_intercept dan koefisien.
- Kelebihan: Mudah dipahami dan diinterpretasikan, efisien secara komputasional saat berurusan dengan dataset besar, dan tidak membuat asumsi tentang distribusi fitur.
- Kekurangan: mengasumsikan hubungan linear antara variabel independen dan dependen, sensitif terhadap outliers, kompleksitas terbatas, tidak cocok untuk data non-linear.
### Support Vector Machine
SVR tujuannya adalah menemukan hiperplane yang terbaik sesuai dengan data dengan margin maksimum. Parameter yang digunakan pada algoritma ini adalah tipe kernel yang dipilih tergantung dengan jenis data dan C yang merupakan parameter regularisasi.
- Kelebihan: Efektif dalam ruang dimensi tinggi, tahan terhadap overfitting, kernel yang serbaguna, berfungsi baik dengan dataset kecil, optimalitas global.
- Kekurangan: Mahal secara komputasional, sensitif terhadap hiperparameter, sulit diinterpretasikan, membutuhkan banyak memori, kurangnya output probabilitas.
### Random Forest
Random Forest adalah metode pembelajaran ensemble yang membangun beberapa pohon keputusan selama pelatihan. Parameter yang digunakan pada algoritma ini adalah n_estimators yaitu merupakan function yang digunakan agar dapat menentukan jumlah tree yang terdapat didalam model RF dan max_features yaitu jumlah fitur yang akan dipertimbangkan saat mencari pemisahan terbaik. 
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

Tabel 1. RMSE train dan test model
|   |                    Model |         Train |          Test |
|--:|-------------------------:|--------------:|--------------:|
| 0 |        Linear Regression | 521308.592130 | 520962.802146 |
| 1 | Support Vector Regressor | 571446.438654 | 568799.580038 |
| 2 |  Random Forest Regressor |  45157.623051 | 114990.508702 |

![download (3)](https://github.com/ainunannisak/ML-PredictiveAnalytics/assets/70701995/4faf48a5-6d5e-42d0-abbb-1e8698fe7bf1)

Gambar 4. Perbandingan performa masing-masing model

Dari Tabel 1 dan Gambar 4 diatas menunjukkan Random Forest melebihi regressor lain dengan RMSE sebesar 1.14e+05. RMSE sebesar 1.14e+05 (1.14 x 10^5) adalah nilai kesalahan rata-rata yang dihasilkan oleh model Random Forest dalam memprediksi penjualan di masa depan. Ini memberikan perkiraan yang baik untuk penjualan di masa depan karena memiliki kesalahan rata-rata sekitar 11%. Dalam kasus ini, jika nilai RMSE sebesar 1.14e+05 dan kita mengasumsikan nilai penjualan sebenarnya adalah suatu angka tertentu, kita dapat menghitung persentase kesalahan. Persentase kesalahan sekitar 11% menunjukkan bahwa model memiliki kesalahan sekitar 11% dari nilai penjualan sebenarnya. Artinya, prediksi model memiliki kesalahan sekitar 11% dalam memperkirakan penjualan di masa depan. Semakin kecil nilai RMSE sebagai persentase dari nilai penjualan sebenarnya, semakin baik kinerja model.

Dari hasil perbandingan ketiga model, RandomForest memiliki kinerja lebih baik daripada model lainnya. Namun, RandomForest memiliki kecenderungan terlalu overfitting pada model yang telah dibangun.

Tabel 1. Hasil prediksi masing-masing model
|      |     y_true | prediksi_LR | prediksi_SVR | prediksi_RFR |
|-----:|-----------:|------------:|-------------:|-------------:|
|  559 | 2174514.13 |   1421495.4 |     960363.5 |    2178019.8 |
| 5825 | 1238844.56 |    821589.2 |     960283.1 |    1412937.4 |
| 6275 |  358461.58 |    833694.4 |     960244.7 |     331128.9 |
| 1316 | 1727565.42 |   1291498.6 |     960359.0 |    1864301.6 |
| 2291 |  749549.55 |   1249850.4 |     960314.6 |     854783.5 |
|  856 | 1436883.99 |   1253474.3 |     960296.0 |    1448458.7 |
| 6256 |  315641.80 |    773757.2 |     960247.9 |     310259.4 |
| 2050 |  509640.77 |   1324343.1 |     960381.5 |     553441.9 |
| 5344 |  377672.46 |    869558.8 |     960280.3 |     370263.2 |
|  784 | 1705506.29 |   1213514.7 |     960314.2 |    1599620.0 |

Dapat kita lihat dari Tabel 1 bahwa prediksi dari ketiga algoritma yang paling mendekati y_true dengan 10 sampel data acak adalah prediksi Random Forest. Ini menandakan bahwa Random Forest merupakan algoritma terbaik dibandingkan dengan algoritma yang lain pada dataset Walmart.

### Kesimpulan

Penjualan selama minggu pada musim liburan secara signifikan lebih tinggi dibandingkan dengan minggu yang bukan pada musim liburan, dengan penjualan rata-rata meningkat dua kali lipat. Penjualan rata-rata toko tertinggi dapat mencapai hingga 500% lebih tinggi daripada toko yang paling rendah.

Model terbaik untuk memprediksi penjualan di masa depan adalah model Random Forest Regressor, yang mencapai nilai RMSE sebesar 1.14e+05. 

## References

[1] M. Dulam, A. Singh, A. Dharipalli, and R. Bollepally, "Predictive Analysis of Supermarket Sales Using Machine Learning," in International Journal of Computer Applications & Research Trends, vol. 10, no. 6, June 2022, pp., ISSN: 2320-2882. Hyderabad, Telangana: CMR Technical Campus, 2022.

[2] M YASSER H, Walmart Sales Prediction - (Best ML Algorithms)

[3] C. S. D. Abhinaya, B. Lahari, C. D. Priya, D. Anjali, B. S. Navya, and B. S. Jyothi, "Supermarket Sales Prediction Using Machine Learning," EPRA International Journal of Research and Development (IJRD), vol. 8, no. 11, pp. 1-5, Nov. 2023. [Online]. Available: https://doi.org/10.36713/epra2016
