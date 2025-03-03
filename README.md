
# Final Task: Analysis of Kimia Farma Business Performance 2020 - 2023

Project ini bertujuan untuk menganalisis kinerja bisnis Kimia Farma selama periode 2020-2023 menggunakan dashboard interaktif dan query SQL di BigQuery dan visualisasi data menggunakan Looker Studio.

### **Overview**
---
Sebagai perusahaan farmasi, Kimia Farma perlu menganalisis tren penjualan dan profitabilitas guna mengoptimalkan strategi serta kinerja bisnisnya. Data yang tersedia mencakup berbagai informasi seperi data transaksi, data inventaris, data produk, dan data kantor cabang. Melalui analisis ini, manajemen diharapkan dapat memperoleh wawasan mengenai kinerja bisnis, baik dari segi total penjualan maupun laba, secara keseluruhan maupun per provinsi dalam rentang waktu 2020 hingga 2023. https://drive.google.com/file/d/18YI-xpCq_5ZMSrYIgwIj2m0Qga0Pyarr/view?usp=sharing
https://drive.google.com/file/d/18YI-xpCq_5ZMSrYIgwIj2m0Qga0Pyarr/view?usp=sharing



### **Tahap Pengerjaan**
---
### 1. Mengimport Dataset ke BigQuery
Proses impor dataset ke BigQuery dilakukan melalui beberapa langkah berikut:
1. Membuat project dengan nama Bakamin-KF-Analytics.
2. Membuat dataset bernama kimia_farma.
3. Mengunggah file .csv ke dalam tabel yang telah dibuat, dengan daftar file sebagai berikut:

    kf_final_transactions

    kf_inventory

    kf_kantor_cabang

    kf_Product

### 2. Tabel Analisa
Berikut merupakan gambaran hasil dari tabel yang sudah di analisa :
![Screenshot 2025-03-01 142655](https://github.com/user-attachments/assets/dd684fab-80a0-465b-940e-df562d88974f)
(lihat tabel [kf_analytcs](https://docs.google.com/spreadsheets/d/1XUep0iTDMqESju_LtTV-YN4Q1lmO2wL0QQfaVS6Cza0/edit?usp=sharing))

### 3. Syntax BigQuery
Syntax dijalankan melalui tahapan berikut:
1. Membuat tabel baru dengan nama 'kf_analytics'.
2. Menentukan kolom-kolom yang akan dimasukkan ke dalam tabel, dengan beberapa kolom memerlukan pemrosesan tambahan, seperti:
    - `tahun`: diambil dari tanggal menggunakan fungsi EXTRACT YEAR.
    - `bulan`: diambil dari tanggal menggunakan fungsi EXTRACT MONTH.
    - `persentase_gross_laba`: dihitung berdasarkan kolom harga menggunakan fungsi IF.
    - `net_sales`: nilai harga setelah dikurangi diskon.
    - `net_profit`: dihitung berdasarkan laba dan persentase_gross_laba.
3. Menggabungkan data dengan tabel lainnya menggunakan LEFT JOIN.

### 4. Analisis Kinerja Dashboard Kimia Farma
Dashboard ini dibuat dengan menggunakan Google Looker Studio
![Copy_of_Copy_of_Looker_Studio_Reporting_-_2_27_25,_6_29 PM_page-0001](https://github.com/user-attachments/assets/30b33cb7-4d47-49e9-ae4c-963beb17783a)
![Dashboard_2 (1)_page-0001](https://github.com/user-attachments/assets/e0857463-d14b-43cd-a1cf-8196897b8fdf)


Dengan memanfaatkan tools dari Looker Studio ini, berbagai aspek kinerja bisnis Kimia Farma dapat dijelaskan secara lebih mendalam, mulai dari tren penjualan, profitabilitas, hingga distribusi produk di setiap provinsi. Penggunaan Google Looker Studio memungkinkan manajemen untuk mengakses laporan yang lebih dinamis, mempercepat proses pengambilan keputusan, serta mengidentifikasi peluang strategi guna meningkatkan efisiensi operasional dan daya saing perusahaan.


