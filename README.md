
# Final Task: Analisis Kinerja Bisnis Kimia Farma tahun 2020 - 2023

Project ini bertujuan untuk menganalisis kinerja bisnis Kimia Farma selama periode 2020-2023 menggunakan dashboard interaktif dan query SQL di BigQuery dan visualisasi data menggunakan Looker Studio.

### **Overview**
---
Kimia Farma, sebagai perusahaan farmasi, perlu memahami tren penjualan dan profitabilitas untuk mengoptimalkan kinerja dan strategi bisnisnya. Dataset yang tersedia mencakup informasi transaksi seperti data transaksi, data inventori, data produk, dan data kantor cabang. Analisis ini akan membantu manajemen dalam memahami bagaimana bagaimana kinerja bisnis dalam total penjualan dan profit, baik secara keseluruhan maupun per provinsi dari tahun 2020 hingga 2023.



### **Tahap Pengerjaan**
---
### 1. Mengimport Dataset ke BigQuery
Proses impor dataset ke BigQuery dilakukan melalui beberapa langkah berikut:
Membuat project dengan nama Bakamin-KF-Analytics.
Membuat dataset bernama kimia_farma.
Mengunggah file .csv ke dalam tabel yang telah dibuat, dengan daftar file sebagai berikut:
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
![Copy_of_Copy_of_Looker_Studio_Reporting_-_2_27_25,_6_29 PM_page-0001](https://github.com/user-attachments/assets/36597175-dd3a-4f2d-8fe3-a048436ed62f)

