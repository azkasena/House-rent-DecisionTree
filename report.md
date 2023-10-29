# Laporan Proyek Machine Learning - Azka Avicenna Rasjid

## Latar Belakang 

Prediksi harga sewa rumah (house rent) adalah masalah yang penting dalam industri real estate dan memiliki dampak langsung pada penyewa, pemilik properti, dan pemangku kepentingan lainnya. Harga sewa rumah yang terlalu tinggi dapat membuat pengguna kesulitan untuk memenuhi kebutuhannya, sedangkan harga sewa rumah yang terlalu rendah dapat membuat pemilik rumah mengalami kerugian. Harga sewa rumah adalah faktor kunci dalam keputusan penyewa dan pemilik properti.  Prediksi harga sewa yang baik dapat meningkatkan efisiensi pasar real estate. Ini memungkinkan penyewa dan pemilik properti untuk membuat keputusan yang lebih baik. 
  
  Format Referensi: [KOMPARASI ALGORITMA MACHINE LEARNING DALAM MEMPREDIKSI HARGA RUMAH](https://ejournal.itn.ac.id/index.php/jati/article/view/6343) 

## Business Understanding

Dalam industri real estate, prediksi harga sewa rumah memiliki peran penting dalam keputusan penyewa, pemilik properti, dan pemangku kepentingan lainnya.

### Problem Statements

Bagaimana hasil dapat memprediksi harga sewa rumah (house rent) dengan akurat berdasarkan atribut-atribut tertentu seperti jumlah kamar tidur (BHK), ukuran sewa, lantai, tipe area, status perabotan, jenis penyewa, jumlah kamar mandi yang diinginkan, dan lainnya?

### Goals

- Mencapai tingkat akurasi yang tinggi dalam memprediksi harga sewa rumah agar penyewa dapat membuat keputusan yang cerdas dan pemilik properti dapat menetapkan harga sewa yang kompetitif.
- Memungkinkan pemilik properti untuk memaksimalkan pendapatan mereka dengan menetapkan harga sewa yang tepat

    ### Solution statements
    -  Mengumpulkan dan membersihkan data terkait, termasuk atribut-atribut seperti BHK, Rent Size, Floor, Area Type, Furnishing Status, Tenant, Preferred Bathroom, dan Point of Contact
    - Memilih model machine learning yang sesuai seperti Decision Tree untuk melakukan prediksi harga sewa.

## Data Understanding
Data yang digunakan untuk prediksi harga sewa rumah adalah house_rent yang diambil dari Kaggle. Data ini berjumlah lebih dari 4700 data rumah yang terdiri dari 12 kolom yaitu, BHK, rent, size, floor, area type, area local, city, furnishing status, tenant preferred, bathroom, point of contact
Link: [Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/house-rent-prediction-dataset).


### Variabel-variabel House rent adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
