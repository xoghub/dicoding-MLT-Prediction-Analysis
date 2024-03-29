# Laporan Proyek Machine Learning - Gunthur Bayu Wibisono

---

## Domain Proyek

---

### Latarbelakang
Mobil merupakan kendaraan bermotor yang digunakan untuk transportasi. Mobil berbahan bakar bensin atau diesel beroda 4. Ada banyak variable yang dibutuhkan untuk menentukan harga untuk membuat konsumen dapat tertarik dengan mobil yang diproduksi oleh pabrikan mobil. Terutama, jika pabrikan yang memproduksi mobil berbeda lokasi yang cukup jauh dengan target pasar. Maka manajerial perusahaan harus mengetahui variable yang tepat dalam menentukan harga.

## Business Understanding

---

### Problem Statements

Sebuah perusahaan mobil Cina, Geely Auto, bercita-cita untuk memasuki pasar AS dengan mendirikan unit produksi mereka di sana dan memproduksi mobil secara lokal untuk bersaing dengan rekan-rekan mereka di AS dan Eropa.

Mereka telah mengontrak sebuah perusahaan konsultan mobil untuk memahami faktor-faktor yang menentukan harga mobil. Secara khusus, mereka ingin memahami faktor-faktor yang memengaruhi harga mobil di pasar Amerika, karena mungkin sangat berbeda dengan pasar Cina. 
Perusahaan ingin tahu:
 * Variabel mana yang signifikan dalam memprediksi harga mobil
Seberapa baik variabel-variabel tersebut menggambarkan harga mobil
* Berdasarkan berbagai survei pasar, perusahaan konsultan tersebut telah mengumpulkan sekumpulan data yang besar dari berbagai jenis mobil di pasar Amerika.

### Goals

Kita diharuskan untuk memodelkan harga mobil dengan variabel independen yang tersedia. Ini akan digunakan oleh manajemen untuk memahami bagaimana tepatnya harga bervariasi dengan variabel independen. Dengan demikian, mereka dapat memanipulasi desain mobil, strategi bisnis, dan lain-lain untuk memenuhi tingkat harga tertentu. Lebih jauh lagi, model ini akan menjadi cara yang baik bagi manajemen untuk memahami dinamika harga di pasar yang baru.

### Solution Statement

Model regressi yang akan kita buat dapat memprediksi harga mobil yang pantas berdasarkan beberapa variable independen yang penting berdasarkan data yang ada. Hal ini dapat dicapai dengan beberapa algoritma, yaitu dengan linear regression, random flores, dan boosting algoritma. Hasil algoritma tersebut dapat kita evaluasi dengan metric, seperti mean squared error(MSE) loss. Metric tersebut menghitung selisih kuadrat rata-rata antara nilai estimasi yang dihasilkan oleh algorithma dan nilai aktual pada data sebenarnya.

## Data Understanding

---

### Sumber Dataset
Data berasal dari kaggle : https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data

Data ini terdiri dari 205 row dengan 26 columns. 

### Variable pada Data set

Data yang kita akan lakukan modeling terdiri dari 26 variabel: 
car_ID, symboling, CarName, fueltype, aspiration, doornumber, carbody, drivewheel,
enginelocation, wheelbase, carlength, carwidth, carheight, curbweight, enginetype,
cylindernumber, enginesize, fuelsystem, boreratio, stroke, compressionratio, horsepower,
peakrpm, citympg, highwaympg, price.

Ada beberapa informasi yang akan kita gunakan, yaitu variable price, dimensi body mobil (carlength, carwidth, carheight, curbweight), fueltype, aspiration, doornumber, carbody, drivewheel, enginelocation, enginetype, cylindernumber, fuelsystem, wheelbase, overall_size, boreratio, hoursepower, citympg, highwaympg.

### Visualisasi data yang ada

**Rata-rata price variable relatif kepada setiap feature kategori**
![mean_price_terhadap_feature_fueltype](https://drive.google.com/uc?export=view&id=17TM6FiJQ5-pv0U0IWKEh0Laq1BlaOvLZ)

![mean_price_terhadap_feature_enginetype](https://drive.google.com/uc?export=view&id=1pmSjqSMnkiucHKnO8hbFIJIFKL3KbN6p)

![mean_price_terhadap_feature_enginelocation](https://drive.google.com/uc?export=view&id=18-RYahSJFTCo8I8eYjXEaMJJNOLI0idg)

![mean_price_terhadap_feature_drivewheel](https://drive.google.com/uc?export=view&id=1S-WixJZ8_7stNSVI0PK6i70odp4ZccwV)

![mean_price_terhadap_feature_cylinderumber](https://drive.google.com/uc?export=view&id=1xdHT_bRtmYO2R86odiZc8JAseuSJliti)

![mean_price_terhadap_feature_carbody](https://drive.google.com/uc?export=view&id=1ey4VuPPVK87vzUD8SylrcBVIsjYGO6ir)

![mean_price_terhadap_feature_aspiration](https://drive.google.com/uc?export=view&id=1TBULeit0Goc07Iv3D6Nt528aRokMNLzI)

**Correlation Matrix Between Price with rest of the fearture**
![korelasi_price_terhadap_feature_lainnya](https://drive.google.com/uc?export=view&id=1--OGIhcyxz6Ym_NqVA6SQ-vE-zZgJfaN)

## Data Preparation

---

Pada data preparation, kami melakukan beberapa hal, yaitu 
* Dropping Data yang diluar IQR

Dropping dilakukan untuk menangani data yang bersifat pecicilan yang diluar data lainnya. Hal ini dilakukan untuk mengurangi kesalahan pada 

* One-Hot Encoder

One-Hot Encoder dilakukan untuk mempermudah kalkulasi pada algoritma pada kategorikal feature.

* PCA (Dimensi Reduksi)

Pada saat melakukan korelasi matriks terdapat beberapa variabel yang memiliki korelasi yang tinggi dan kami melakukan reduksi jumlah feature tersebut untuk membuat komputasi lebih efisien. 

* Standar Scaller

Kami melakukan normalisasi dengan standar scaller untuk membuat semua data dengan numerikal feature tersebut agar mengikuti distribusi normal.

## Modeling

---

Model pada proyek ini terdapat 3, yaitu Linear Regression, Random Forest Regression, dan Ada Boosting. 
### Kelebihan dan Kekurangan Model
* Linear Regression
Kelebihan : Simple
Kekurangan : Tidak bagus untuk complex data
* Random Forest Regression
Kelebihan : Cocok untuk complex data
Kekurangan : Model terbilang cukup complex
* Ada Boosting
Kelebihan : cocok untuk complex data
Kekurangan : Model terbilang cukup complex

### Model yang Terbaik

Model yang terbaik sejauh ini adalah Random Forest Regression dengan training loss yang cukup kecil, seperti yang ada dibawah ini. 

![random_forest_regression_loss](https://drive.google.com/uc?export=view&id=1xhyL4azWIWNyFA2_zpCQDWxaiIjaEcCl)

## Evaluation

---

Hasil akhir menunjukan bahwa random forest regression memiliki loss yang cukup rendah dan akurasi yang cukup tinggi untuk regressi pada dataset ini.

![evaluasi_algoritma_loss](https://drive.google.com/uc?export=view&id=13dU4BpgBFykrwdtqTQW9qVRP3pFuB0je)


