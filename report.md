# Laporan Proyek Machine Learning - Azka Avicenna Rasjid

## Domain Proyek 
  ### Latar Belakang

Tempat tinggal merupakan seperti kewajiban untuk saat ini. Akan tetapi, tidak semua tempat tinggal atau rumah memilikinya dan hanya dapat menyewa. Prediksi harga sewa rumah (house rent) adalah masalah yang penting dalam industri _real estate_ dan memiliki dampak langsung pada penyewa, pemilik properti, dan pemangku kepentingan lainnya. Harga sewa rumah yang terlalu tinggi dapat membuat pengguna kesulitan untuk memenuhi kebutuhannya, sedangkan harga sewa rumah yang terlalu rendah dapat membuat pemilik rumah mengalami kerugian. Harga sewa rumah adalah faktor kunci dalam keputusan penyewa dan pemilik properti.  Prediksi harga sewa yang baik dapat meningkatkan efisiensi pasar _real estate_. Ini memungkinkan penyewa dan pemilik properti untuk membuat keputusan yang lebih baik. Dalam mencapai hal tersebut, maka dilakukan penelitian untuk memprediksi harga sewa rumah menggunakan _model machine learning_. Diharapkan model ini mampu memprediksi harga sewa yang sesuai dengan harga pasar. Prediksi ini nantinya dijadikan acuan bagi perusahaan dalam menyewa rumah dengan harga yang dapat mendatangkan profit bagi perusahaan.
  
Referensi: [Komparasi Algoritma Machine Learning Dalam Memprediksi Harga Rumah](https://ejournal.itn.ac.id/index.php/jati/article/view/6343) 

## _Business Understanding_

Dalam industri _real estate_, prediksi harga sewa rumah memiliki peran penting dalam keputusan penyewa, pemilik properti, dan pemangku kepentingan lainnya. Tujuan utama dari proyek ini adalah memberikan prediksi harga sewa rumah yang akurat kepada pemilik properti, penyewa, investor, dan pihak terkait lainnya. Solusi yang dapat diambil adalah mengembangkan model prediksi harga sewa rumah menggunakan teknik _machine learning_. 

### _Problem Statements_

1. Bagaimana cara memproses data agar dapat dilatih dengan baik oleh model?
2. Berapa harga aktual sewa rumah dan harga prediksi untuk masa depan?

### _Goals_

1. Melakukan persiapan data untuk dapat dilatih oleh model.
2. Membuat model machine learning yang dapat memprediksi harga sewa rumah seakurat mungkin berdasarkan karakteristik tertentu


    ### _Solution statements_
    -  Mengumpulkan dan membersihkan data terkait, termasuk atribut-atribut seperti _BHK, Rent Size, Floor, Area Type, Furnishing Status, Tenant, Preferred Bathroom, dan Point of Contact_.
    -  Menyiapkan data agar bisa digunakan dalam membangun model.
    - Memilih model_ machine learning_ yang sesuai seperti Decision Tree untuk melakukan prediksi harga sewa.

## Data Understanding
Data yang digunakan untuk prediksi harga sewa rumah adalah house_rent berbentuk csv yang diambil dari Kaggle. Data ini berjumlah lebih dari 4700 data rumah yang terdiri dari 12 kolom yaitu _BHK, rent, size, floor, area type, area local, city, furnishing status, tenant preferred, bathroom, point of contact_. Data dapat diunduh di : [Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/house-rent-prediction-dataset).

Berikut data dari dataset : 
1. Dataset memiliki format CSV (Comma-Seperated Values).
2. Dataset memiliki 4746 sample dengan 12 fitur.
3. Dataset memiliki 4 fitur bertipe int64 dan 8 fitur bertipe object.
4. Tidak ada missing value dalam dataset.


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
1. Data normalization
   Data akan diubah menjadi data kuantitatif
2. Train Test Split
   Data akan dibagi menjadi train dan test agar disiapkan untuk membangun model
   
## Modeling
Pembuatan model_ Machine Learning_ untuk prediksi harga sewa menggunakan _Decision Tree_ adalah proses membangun model prediksi berdasarkan pohon keputusan. _Decision tree_ adalah algoritma pembelajaran mesin yang dapat digunakan baik untuk masalah klasifikasi maupun regresi terutama saat ingin memprediksi harga berkelanjutan. _Decision tree_ relatif mudah diimplementasikan dan dipahami. Ada banyak alat dan pustaka yang tersedia, seperti scikit-learn di Python, yang memudahkan pembuatan, pelatihan, dan evaluasi model Decision Tree.
Berikut adalah hasil dari pelatihan harga prediksi sewa rumah dengan harga aktual .
Decision Tree :
Decision Tree (Pohon Keputusan) adalah algoritma pembelajaran mesin yang digunakan dalam klasifikasi dan regresi. Konsep dasar Decision Tree adalah sebagai berikut:
1. Node (Node): Setiap node dalam pohon keputusan mewakili pemilihan atau tes pada atribut tertentu.
2. Pertanyaan (Question): Pada setiap node, model mengajukan pertanyaan tentang nilai atribut. Misalnya, "Apakah jumlah BHK lebih besar dari 3?"
3. Cabang (Branches): Setiap cabang dalam node mengarah ke pilihan yang berbeda berdasarkan jawaban pertanyaan. Jika jawabannya "Ya," maka Anda akan pergi ke salah satu cabang, dan jika jawabannya "Tidak," Anda akan pergi ke cabang lain.
4. Leaf Node (Node Daun): Ketika Anda mencapai node daun, itu adalah tempat di mana model membuat prediksi. Misalnya, dalam prediksi harga sewa, node daun mungkin memiliki nilai prediksi harga sewa.
5. Kriteria Splitting (Kriteria Pemisahan): Model memilih atribut mana yang harus digunakan sebagai pertanyaan pada setiap node. Pemilihan ini didasarkan pada kriteria seperti Information Gain, Gini Impurity, atau Mean Squared Error (untuk regresi).
6. Penghentian (Stopping Criteria): Anda dapat mengatur kriteria untuk menghentikan pembentukan pohon, seperti kedalaman maksimum pohon atau jumlah sampel minimum di setiap node.
Kelebihan Decision Tree terutama dalam interpretabilitas dan kemampuan penanganan atribut campuran menjadikannya pilihan yang baik dalam banyak kasus, termasuk dalam prediksi harga sewa rumah. 
## Evaluation
Setelah model dibangun, evaluasi kinerjanya menggunakan metrik evaluasi yang sesuai, seperti _Mean Absolute Error_ (MAE), _Mean Squared Error_ (MSE), dan _R-squared _(koefisien determinasi). Metrik ini membantu Anda memahami sejauh mana model Anda dapat memprediksi harga sewa dengan akurat. Hasilnya adalah MAE : 11965.626316193628, MSE : 917785754.6561476, R-squared : 917785754.6561476. 
Fungsi: MAE mengukur kesalahan rata-rata antara prediksi model dan nilai sebenarnya. Ini mengukur sejauh mana prediksi model mendekati harga sewa yang sebenarnya.
Fungsi: MSE mengukur seberapa besar kesalahan kuadrat antara prediksi model dan nilai sebenarnya. Ini memberi bobot lebih besar kepada kesalahan besar.
Fungsi: R2 mengukur sejauh mana variasi dalam harga sewa yang dijelaskan oleh model. Ini adalah pengukuran seberapa baik model Anda cocok dengan data.

 | Prediction of Rent | Actual Rent |
  |-------------------|-------------|
  | 10000.0           | 10500       |
  | 50000.0           | 80000       |
  | 120000.0  	      | 120000      |
  | 25000.0   	      | 17000       |
  | 85000.0	  	      | 65000       |
