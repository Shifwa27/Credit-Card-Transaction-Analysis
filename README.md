# Credit-Card-Transaction-Analysis
## Project Overview

Proyek ini merupakan analisis data dari dataset transaksi kartu kredit skala besar (\~1 juta baris). Tujuan utamanya adalah untuk menggali *insight* dari perilaku transaksi, mengidentifikasi segmen users yang berbeda, menganalisis potensi risiko, dan menyajikannya dalam sebuah *dashboard*.

Proyek ini terdiri dari beberapa tahapan, mulai dari pembersihan data (ETL), analisis mengguakan SQL, pemodelan *machine learning*, dan visualisasi menggunakan Looker Studio.

## Goals

  * Menganalisis pola dan tren utama dalam perilaku transaksi.
  * Mengidentifikasi segmen-segmen users berdasarkan profil finansial dan demografis.
  * Mendeteksi anomali dan menganalisis metrik risiko yang terkait dengan transaksi (misalnya, *error*).
  * Menyajikan insight secara visual melalui *dashboard* untuk mendukung pengambilan keputusan berbasis data.

## Tools

  * **Bahasa Pemrograman:** SQL dan Python.
  * **Libraries:** Pandas, Scikit-learn, Matplotlib, Seaborn.
  * **Lingkungan Analisis:** Google Colab.
  * **Data Warehouse:** Google BigQuery Sandbox.
  * **Alat Visualisasi (BI Tool):** Looker Studio.

## Project Workflow

Proyek ini dilaksanakan melalui beberapa tahapan utama:

1.  **Pembersihan & Persiapan Data (ETL):** Data mentah dari file CSV dimuat ke dalam DataFrame Pandas. Proses pembersihan melibatkan penanganan tipe data yang tidak konsisten (mengubah kolom mata uang dari teks ke angka), mengelola nilai yang hilang, dan memastikan integritas data.
2.  **Analisis Data Eksploratif (EDA):** Analisis mendalam dilakukan menggunakan query SQL di Google Colab untuk mengetahui tren waktu, pola geografis, dan *insight* lainnya.
3.  **Machine Learning - Segmentasi Users:** Sebuah model *unsupervised learning* **K-Means Clustering** dibangun untuk mengelompokkan users ke dalam beberapa kelompok yang berbeda berdasarkan kesamaan finansial.
4.  **Cloud Data Warehousing:** Karena keterbatasan lingkungan lokal dan batasan *upload* pada *tool* Looker Studio untuk memproses dataset yang besar, ketiga tabel yang sudah bersih di-upload ke **Google BigQuery Sandbox**. Ini memastikan analisis berjalan cepat dan efisien.
5.  **Dashboarding & Visualisasi:** Sebuah *dashboard* interaktif dibangun di **Looker Studio** yang terhubung langsung ke BigQuery, menyajikan semua *insight* secara visual dan mudah dipahami.


## Dashboard Preview

> **[Klik di sini untuk mengakses Dashboard Interaktif Looker Studio](https://lookerstudio.google.com/s/sHvOmUFpJbA)**

## Model Machine Learning: Segmentasi Users

Model K-Means menghasilkan 4 segmen users dengan karakteristik unik sebagai berikut:

| Cluster | Persona | Karakteristik Utama |
| :--- | :--- | :--- |
| **0** | **The Savers** | Pendapatan, utang, dan limit kredit paling rendah. Profil risiko rendah. |
| **1** | **The High Rollers** | Pendapatan tinggi, namun utang juga sangat tinggi. Bernilai tinggi, namun berisiko tinggi. |
| **2** | **The Established Elders** | Usia senior, utang sangat rendah, skor kredit baik. Pelanggan stabil dan loyal. |
| **3** | **The Prime Users** | Skor kredit paling tinggi, utang terkelola baik. Profil yang bagus dengan potensi pertumbuhan tinggi. |


##  Author

  * **Shifwa Luqyaanaa**
      * [LinkedIn](https://www.linkedin.com/in/shifwa-luqyaanaa/)
