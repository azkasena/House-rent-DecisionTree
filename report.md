# Laporan Proyek Machine Learning - Azka Avicenna Rasjid

## Latar Belakang 

Prediksi harga sewa rumah (house rent) adalah masalah yang penting dalam industri _real estate_ dan memiliki dampak langsung pada penyewa, pemilik properti, dan pemangku kepentingan lainnya. Harga sewa rumah yang terlalu tinggi dapat membuat pengguna kesulitan untuk memenuhi kebutuhannya, sedangkan harga sewa rumah yang terlalu rendah dapat membuat pemilik rumah mengalami kerugian. Harga sewa rumah adalah faktor kunci dalam keputusan penyewa dan pemilik properti.  Prediksi harga sewa yang baik dapat meningkatkan efisiensi pasar _real estate_. Ini memungkinkan penyewa dan pemilik properti untuk membuat keputusan yang lebih baik. 
  
Referensi: [Komparasi Algoritma Machine Learning Dalam Memprediksi Harga Rumah](https://ejournal.itn.ac.id/index.php/jati/article/view/6343) 

## _Business Understanding_

Dalam industri _real estate_, prediksi harga sewa rumah memiliki peran penting dalam keputusan penyewa, pemilik properti, dan pemangku kepentingan lainnya. Tujuan utama dari proyek ini adalah memberikan prediksi harga sewa rumah yang akurat kepada pemilik properti, penyewa, investor, dan pihak terkait lainnya. Solusi yang dapat diambil adalah mengembangkan model prediksi harga sewa rumah menggunakan teknik _machine learning_. 

### _Problem Statements_

Bagaimana hasil akurasi agar dapat memprediksi harga sewa rumah dengan akurat berdasarkan atribut-atribut tertentu seperti jumlah kamar tidur (BHK), ukuran sewa, lantai, tipe area, status perabotan, jenis penyewa, jumlah kamar mandi yang diinginkan, dan lainnya?

### _Goals_

- Mencapai tingkat akurasi yang tinggi dalam memprediksi harga sewa rumah agar penyewa dapat membuat keputusan yang cerdas dan pemilik properti dapat menetapkan harga sewa yang kompetitif.
- Memungkinkan pemilik properti untuk memaksimalkan pendapatan mereka dengan menetapkan harga sewa yang tepat

    ### _Solution statements_
    -  Mengumpulkan dan membersihkan data terkait, termasuk atribut-atribut seperti _BHK, Rent Size, Floor, Area Type, Furnishing Status, Tenant, Preferred Bathroom, dan Point of Contact_.
    - Memilih model_ machine learning_ yang sesuai seperti Decision Tree untuk melakukan prediksi harga sewa.

## Data Understanding
Data yang digunakan untuk prediksi harga sewa rumah adalah house_rent berbentuk csv yang diambil dari Kaggle. Data ini berjumlah lebih dari 4700 data rumah yang terdiri dari 12 kolom yaitu _BHK, rent, size, floor, area type, area local, city, furnishing status, tenant preferred, bathroom, point of contact_. Data dapat diunduh di : [Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/house-rent-prediction-dataset).


### Variabel-variabel pada Dataset:
Posted On: Tanggal data diposting.
BHK: Jumlah dari kamar tidur, aula, dan dapur.
Rent: Harga sewa dari rumah/apartemen.
Size: Luas dari rumah/apartemen dalam square feet (sqft).
Floor: Letak dan jumlah lantai rumah/apartemen.
Area Type: Ukuran dari rumah dalam kategori Super Area atau Carpet Area atau Build Area.
Area Locality: Lokasi rumah/apartemen.
City: Kota dimana rumah/apartemen berada.
Furnishing Status: Status perabotan rumah/apartemen, baik Furnished atau Semi-Furnished atau Unfurnished.
Tenant Preferred: Jenis penyewa yang diutamakan pemilik atau agen.
Bathroom: Jumlah kamar mandi.
Point of Contact: Kontak yang dihubungi untuk informasi lebih lanjut mengenai rumah/apartemen.


## Data Preparation
Pertama data diupload ke google colab. Kemudian periksa apakah dataset memiliki missing value atau tidak dengan menggunakan df.isnull().sum(). Data kemudian akan diubah menjadi data kuantitatif pada kolom area type, city, furnishing status, dan point of contact. Pada area type carpet area : 1, super area : 2, built area : 3. Pada city Kolkata : 1, Delhi : 2, Mumbai : 3, Bangalore : 4, Hyderabad : 5, Chennai : 6. Pada furnishing status, unfurnished : 1, semi-furnished : 2, furnished : 3. Pada point of contact, contact owner : 1, contact agent : 2, contact builder : 3. Kemudian data akan dibagi menjadi train dan test dengan test size = 0.15

## Modeling
Pembuatan model_ Machine Learning_ untuk prediksi harga sewa menggunakan _Decision Tree_ adalah proses membangun model prediksi berdasarkan pohon keputusan. _Decision tree_ adalah algoritma pembelajaran mesin yang dapat digunakan baik untuk masalah klasifikasi maupun regresi terutama saat ingin memprediksi harga berkelanjutan. _Decision tree_ relatif mudah diimplementasikan dan dipahami. Ada banyak alat dan pustaka yang tersedia, seperti scikit-learn di Python, yang memudahkan pembuatan, pelatihan, dan evaluasi model Decision Tree.
Berikut adalah hasil dari pelatihan harga prediksi sewa rumah dengan harga aktual .
![image](https://github.com/azkasena/House-rent-DecisionTree/assets/73009518/d39bcdb4-8527-401d-a628-10851188e330)

## Evaluation
Setelah model dibangun, evaluasi kinerjanya menggunakan metrik evaluasi yang sesuai, seperti _Mean Absolute Error_ (MAE), _Mean Squared Error_ (MSE), dan _R-squared _(koefisien determinasi). Metrik ini membantu Anda memahami sejauh mana model Anda dapat memprediksi harga sewa dengan akurat. Hasilnya adalah MAE : 11965.626316193628, MSE : 917785754.6561476, R-squared : 917785754.6561476. 
Fungsi: MAE mengukur kesalahan rata-rata antara prediksi model dan nilai sebenarnya. Ini mengukur sejauh mana prediksi model mendekati harga sewa yang sebenarnya.
Fungsi: MSE mengukur seberapa besar kesalahan kuadrat antara prediksi model dan nilai sebenarnya. Ini memberi bobot lebih besar kepada kesalahan besar.
Fungsi: R2 mengukur sejauh mana variasi dalam harga sewa yang dijelaskan oleh model. Ini adalah pengukuran seberapa baik model Anda cocok dengan data.

![image](https://github.com/azkasena/House-rent-DecisionTree/assets/73009518/6a878371-9b13-4ac8-8b88-924a5f725cf5)
