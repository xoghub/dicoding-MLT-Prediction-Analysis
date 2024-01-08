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

## Data Preparation

---

* Penjelasan tentang data preparation
* alasan mengapa harus dilakaukan

## Modeling

---

* modelnya apa
* kelebihan dan kekurangan model yang ada
* improvement
* model yang terbaik

## Evaluation

---




