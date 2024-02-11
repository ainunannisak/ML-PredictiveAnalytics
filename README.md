# ML-PredictiveAnalytics

## Domain Proyek
Topik yang diangkat dari proyek ini yaitu mengenai bidang ekonomi dan bisnis, di mana suatu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan mingguan.

### Latar Belakang
Memprediksi permintaan suatu produk dan menyimpannya sesuai kebutuhan dimasa yang akan datang merupakan hal penting dalam penjualan bisnis supermarket. Dengan prediksi yang akurat, dapat dicapai retensi pelanggan yang lebih baik, kepuasan pelanggan, dan menghindari situasi stok berlebihan dan kekurangan stok [1](https://ijcrt.org/papers/IJCRT22A6470.pdf)
to Markdown converter.

Salah satu toko ritel terkemuka di Amerika Serikat, yaitu Walmart, ingin memprediksi penjualan dan permintaan dengan akurat. Ada beberapa acara dan hari libur yang mempengaruhi penjualan setiap harinya [2](https://www.kaggle.com/code/yasserh/walmart-sales-prediction-best-ml-algorithms). Pada project ini, akan dilakukan prediksi Machine Learning untuk penjualan mingguan pada supermarket Walmart.

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




