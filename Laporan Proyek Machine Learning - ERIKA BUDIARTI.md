# Laporan Proyek Machine Learning 
**- ERIKA BUDIARTI -**


## Domain Proyek

Nama *Project* : **Gold Price Prediction**

**Latar Belakang**:      
Harga emas merupakan salah satu aset investasi yang terkenal di seluruh dunia. Nilai dari emas sangat dipengaruhi oleh berbagai faktor, seperti inflasi, tingkat suku bunga, kondisi ekonomi global, dan tingkat permintaan terhadap logam mulia tersebut. Kemampuan harga emas untuk berfluktuasi dengan cepat telah menjadi tantangan bagi para investor yang berusaha memproyeksikan bagaimana harga emas akan bergerak di masa mendatang.
Pendekatan menggunakan teknologi *Machine Learning (ML)* muncul sebagai solusi yang potensial untuk memprediksi pergerakan harga emas di masa depan. Dalam konteks ini, ML dapat digunakan untuk menganalisis dan memahami pola-pola yang ada dalam data historis harga emas. Dengan memanfaatkan pembelajaran dari data masa lalu, ML dapat memberikan perkiraan tentang bagaimana harga emas mungkin akan berubah di masa depan.

Dataset ini menggunakan informasi harga emas dari tahun 2009-2018 dengan rata-rata harga emas per tahun adalah sebagai berikut:

|*Year*| *Gold*|
|------|-------|    
| 2008 | 86.11 |    
| 2009 | 95.83 |    
| 2010 | 119.97|    
| 2011 | 152.59|    
| 2012 | 162.15|    
| 2013 | 136.85|    
| 2014 | 121.72|    
| 2015 | 111.17|    
| 2016 | 118.78|    
| 2017 | 119.55|    
| 2018 | 126.02|    

**Penelitian Terkait**:      
Anisa Aulia : 
"Emas adalah logam mulia yang sangat diminati, karena secara umum nilai emas cenderung stabil dan harganya per gram akan meningkat setiap tahun. Investasi emas terbagi menjadi dua, yaitu investasi digital dan investasi fisik. Terkadang dalam investasi emas ini investor akan mengalami kerugian serta mendapatkan keuntungan. Untuk meminimalisir hal tersebut, dibutuhkan teknik untuk memprediksi harga emas. Teknik prediksi merupakan salah satu teknik yang digunakan dalam Machine Learning. Penelitian ini bertujuan untuk memprediksi harga emas menggunakan algoritma *Support Vector Regression (SVR)* dan *Linear Regression (LR)* sebagai perbandingan." [1]


## Business Understanding

### Problem Statements

1. Harga emas merupakan salah satu aset investasi yang sangat diminati di seluruh dunia. Dalam situasi di mana harga emas dipengaruhi oleh sejumlah faktor, para investor menghadapi tantangan dalam memprediksi pergerakan harga emas di masa depan.
Dampak ekonomi global dan faktor-faktor memengaruhi harga emas:
    * **Inflasi** 
    Inflasi adalah salah satu faktor utama yang memengaruhi harga emas. Ketika tingkat inflasi naik, daya beli mata uang menurun, dan ini mendorong orang untuk mencari *safe haven asset* seperti emas. Sebagai perlindungan nilai terhadap inflasi, harga emas cenderung naik ketika inflasi tinggi.
    * **Suku Bunga** 
    Suku bunga juga memiliki dampak besar pada harga emas. Ketika suku bunga naik, investasi berbasis bunga seperti obligasi menjadi lebih menarik dibandingkan dengan emas yang tidak menghasilkan bunga. Sebagai hasilnya, harga emas dapat turun ketika suku bunga naik, dan sebaliknya.
    * **Kondisi Ekonomi Global**
    Kondisi ekonomi global, termasuk pertumbuhan ekonomi, stabilitas geopolitik, dan ketidakpastian, dapat mempengaruhi harga emas. Saat kondisi ekonomi tidak stabil atau terjadi krisis, emas sering dianggap sebagai tempat berlindung yang aman. Oleh karena itu, harga emas dapat naik dalam situasi-situasi ini.
    * **Permintaan dan Penawaran** 
    Permintaan dan penawaran fisik emas juga memengaruhi harga. Permintaan emas dapat bervariasi berdasarkan sektor industri (misalnya, perhiasan dan teknologi), dan juga oleh bank sentral yang membeli atau menjual emas sebagai cadangan. Faktor-faktor ini dapat mempengaruhi ketersediaan dan harga emas.
    * **Dolar AS** 
    Harga emas sering memiliki korelasi terbalik dengan nilai dolar AS. Ketika dolar melemah, emas biasanya naik, karena harga emas yang dihargai dalam dolar menjadi lebih murah bagi investor asing, dan sebaliknya.
    * **Spekulasi dan Sentimen Pasar** 
    Perilaku investor dan sentimen pasar juga berdampak pada harga emas. Keputusan pembelian dan penjualan berdasarkan faktor-faktor psikologis dan spekulasi dapat menciptakan fluktuasi harga yang signifikan.
    * **Faktor-faktor Geopolitik** 
    Peristiwa geopolitik, seperti konflik, sanksi ekonomi, atau ketegangan internasional, dapat meningkatkan permintaan atas emas sebagai *safe haven asset*. Dalam situasi-situasi ini, harga emas cenderung naik. 

2. Pemanfaatan teknologi *Machine Learning (ML)* telah menjadi pendekatan yang menjanjikan untuk memprediksi harga emas di masa depan. Meskipun ML mampu memahami dan memodelkan pola-pola dari data historis harga emas, tingkat akurasi dalam prediksi harga emas masih belum mencapai optimal. Diversifikasi portofolio dan penggunaan analisis prediktif juga tetap penting dalam pengambilan keputusan investasi.

### Goals

1. Meningkatkan akurasi prediksi harga emas dengan memanfaatkan teknik-teknik ML yang lebih canggih dan efisien dan mengembangkan model ML yang lebih fleksibel dan adaptif, mampu mengatasi berbagai kondisi pasar yang berubah-ubah dengan pendekatan yang lebih tepat.
    
2. Memberikan informasi berharga kepada investor untuk mendukung pengambilan keputusan investasi yang lebih tepat dan informatif dan menyediakan perkiraan harga emas di masa depan dengan tingkat akurasi yang tinggi, sehingga membantu mengurangi ketidakpastian dalam investasi emas.
Berikut adalah beberapa informasi berharga yang dapat disediakan kepada investor dan bagaimana hal itu akan membantu mengurangi ketidakpastian dalam investasi emas:
    * **Informasi tentang faktor-faktor ekonomi** yang memengaruhi harga emas, seperti inflasi, suku bunga, dan situasi geopolitik, dapat membantu investor memahami dasar-dasar harga emas. Dengan memantau faktor-faktor ini secara teratur, investor dapat mengambil keputusan yang lebih informasi tentang kapan membeli atau menjual emas.
    * **Informasi tentang pola dan tren historis harga emas** melalui analisis teknikal dapat memberikan pandangan tentang pergerakan harga di masa depan. Grafik, indikator teknikal, dan sinyal trading dapat membantu investor mengidentifikasi titik masuk dan keluar yang potensial.
    * **Informasi tentang sentimen pasar terkini** seperti berita ekonomi, perkembangan geopolitik, dan pandangan analis, dapat membantu investor memahami bagaimana pasar merespons peristiwa tertentu. Sentimen pasar dapat berdampak besar pada harga emas, dan pemahaman yang lebih baik tentang hal ini dapat membantu mengurangi ketidakpastian.
    * **Prediksi harga emas** yang disediakan dengan tingkat akurasi yang tinggi melalui model ML atau analisis statistik dapat memberikan pandangan lebih baik tentang kemungkinan pergerakan harga emas di masa depan. Ini dapat membantu investor dalam merencanakan strategi investasi mereka.
    * **Informasi tentang pentingnya diversifikasi portofolio** dalam investasi emas. Investor perlu memahami bagaimana mengintegrasikan emas ke dalam portofolio mereka untuk mengurangi risiko.
    * **Informasi tentang Risiko dan Manajemen Risiko** yang terkait dengan investasi emas dan strategi manajemen risiko yang efektif sangat berharga. Ini termasuk pemahaman tentang volatilitas harga emas dan penggunaan instrumen derivatif untuk melindungi portofolio.
    * **Informasi tentang berbagai instrumen keuangan** yang dapat digunakan dalam investasi emas, seperti ETF emas, kontrak berjangka, atau saham perusahaan pertambangan emas, dapat membantu investor memilih instrumen yang sesuai dengan tujuan investasi mereka.
    * **Pemahaman tentang Biaya terkait dengan investasi emas** seperti biaya penyimpanan fisik emas atau biaya manajemen ETF emas, penting untuk menghitung potensi pengembalian investasi secara akurat.

### Solution Statements

1. Solusi pertama untuk meningkatkan akurasi dalam prediksi harga emas adalah dengan menggabungkan dua atau lebih algoritma Machine Learning yang berbeda. Tiap algoritma ML memiliki keunggulan dan kelemahan masing-masing, sehingga dengan mengkombinasikannya, kita dapat memanfaatkan keunggulan tiap algoritma untuk meningkatkan akurasi prediksi harga emas. Sebagai contoh, kita bisa memanfaatkan model *Linear Regression (LR)* untuk menangkap trend jangka panjang dalam data harga emas, atau menggunakan model *Support Vector Machine (SVM) Regressor* untuk melihat potensi fluktuasi jangka pendek.

2. Solusi kedua adalah melakukan perbaikan pada model dasar (*baseline*) dengan melakukan *tuning* terhadap *hyperparameter*-nya. Model dasar seringkali merupakan model yang sederhana dan belum dioptimalkan, sehingga akurasinya biasanya rendah. Dengan melakukan tuning pada hyperparameter, kita bisa mencari nilai-nilai yang optimal untuk meningkatkan akurasi model. *Hyperparameter* adalah parameter-parameter yang tidak dapat diajarkan oleh model ML dan perlu ditentukan secara manual. Melalui proses tuning ini, kita dapat mengidentifikasi kombinasi *hyperparameter* terbaik yang dapat menghasilkan prediksi harga emas yang lebih akurat dan efektif.


## Data Understanding

*Klik link untuk download Dataset*:  
https://www.kaggle.com/datasets/altruistdelhite04/gold-price-data

**Gambaran Umum Dataset**:     
Berkas data ini berformat *Comma Separated Value (CSV)* dengan 2290 baris dan 6 kolom. Berkas ini berisi 5 kolom yang memiliki tipe data numerik, dan 1 kolom dengan tipe data tanggal. Dataset dengan jelas menampilkan nilai variabel-variabel SPX, GLD, USO, SLV, EUR/USD terhadap kolom tanggal.

### Variabel-variabel pada dataset adalah sebagai berikut:
-  **SPX**    
adalah *S&P 500 Index*, yang merupakan indeks pasar saham yang mengukur kinerja 500 perusahaan terbesar yang terdaftar di bursa saham Amerika Serikat. SPX adalah salah satu indeks pasar saham paling berpengaruh di dunia.

- **GLD**   
adalah *SPDR Gold Shares*, yang merupakan *exchange-traded fund (ETF)* yang berinvestasi pada emas fisik. GLD adalah salah satu ETF emas terbesar di dunia.

- **USO**   
adalah *United States Oil Fund*, yang merupakan ETF yang berinvestasi pada kontrak berjangka minyak mentah *West Texas Intermediate (WTI)*. USO adalah salah satu ETF minyak terbesar di dunia.

- **SLV**    
adalah *iShares Silver Trust*, yang merupakan ETF yang berinvestasi pada perak fisik. SLV adalah salah satu ETF perak terbesar di dunia.

- **EUR/USD**   
adalah pasangan mata uang euro terhadap dolar AS. EUR/USD adalah salah satu pasangan mata uang paling likuid di dunia.

- **DATE**    
adalah tanggal yang menjadi patokan pengukuran harga emas. Tanggal ditulis dalam format *mm/dd/yyyy*.

### Melihat sekilas pada dataset

Sebelum melakukan *modeling* dan *evaluation* dengan algoritma *Machine Learning* pada Notebook "Google Colaboratory", mari kita melihat sekilas pada *dataset* yang digunakan. Di bawah ini akan ditampilkan cuplikan dari dataset, deskripsi statistik dan korelasi antar variabel beserta penjelasannya.


                  Tabel 1 : Cuplikan Dataset   
|Index  |    Date   |   SPX   |   GLD   |  USO  |  SLV  | EUR/USD |
|-------|-----------|---------|---------|-------|-------|---------|
|  0    |  1/2/2008 | 1447.16 |   84.86 | 78.47 | 15.18 |  1.47   |
|  1    |  1/3/2008 | 1447.16 |   85.57 | 78.37 | 15.29 |  1.47   |
|  2    |  1/4/2008 | 1411.63 |   85.13 | 77.30 | 15.17 |  1.48   |
|  3    |  1/7/2008 | 1416.18 |   84.77 | 75.50 | 15.05 |  1.47   |
|  4    |  1/8/2008 | 1390.19 |   86.78 | 76.06 | 15.59 |  1.56   |
| ......| ..........| ........| ........| ......| ......| ........|
|  2285 |  5/8/2018 | 2671.92 |  124.59 | 14.06 | 15.51 |  1.19   |
|  2286 |  5/9/2018 | 2697.79 |  124.33 | 14.37 | 15.53 |  1.18   |
|  2287 | 5/10/2018 | 2723.07 |  125.18 | 14.41 | 15.74 |  1.19   |
|  2288 | 5/14/2018 | 2730.13 |  124.49 | 14.38 | 15.56 |  1.19   |
|  2289 | 5/16/2018 | 2725.78 |  122.54 | 14.41 | 15.45 |  1.18   |

Pada Tabel 1, kita dapat melihat 5 baris pertama dan 5 baris terakhir pada dataset yang belum dilakukan *preprocessing*.


         Tabel 2 : Deskripsi Statistik Dataset      
| Desc  |   SPX   |   GLD   |   USO   |   SLV   | EUR/USD |
|-------|---------|---------|---------|---------|---------|
| count | 2290.00 | 2290.00 | 2290.00 | 2290.00 | 2290.00 |
|  mean | 1654.32 |  122.73 |   31.84 |   20.85 |    1.28 |
|  std  |  519.11 |   23.28 |   19.52 |    7.09 |    0.13 |
|  min  |  676.53 |   70.00 |    7.96 |    8.85 |    1.04 |
|  25%  | 1239.87 |  109.73 |   14.38 |   15.57 |    1.17 |
|  50%  | 1551.43 |  120.58 |   33.87 |   17.27 |    1.30 |
|  75%  | 2073.01 |  132.84 |   37.83 |   22.88 |    1.37 |
|  max  | 2872.87 |  184.59 |  117.48 |   47.26 |    1.60 | 

Tabel 2 memberikan informasi mengenai statistik *dataset* yaitu *count*(jumlah data), *mean*(nilai rata-rata), *std*(standard deviasi), *min*(nilai terendah), *25%*(quartil 1), *50%*(median), *75%*(quartil 3) dan *max*(nilai tertinggi).


         Tabel 3 : Korelasi Antar Variabel       
|         |   SPX   |   GLD   |   USO   |   SLV   | EUR/USD |
|---------|---------|---------|---------|---------|---------|
| SPX     |    1,00 |   0.05  |   -0.59 |  -0.27  |   -0.67 |
| GLD     |    0.05 |   1.00  |   -0.19 |   0.87  |   -0.02 |
| USO     |   -0.59 |  -0.19  |    1.00 |   0.17  |    0.83 |
| SLV     |   -0.27 |   0.87  |    0.17 |   1.00  |    0.32 |
| EUR/USD |   -0.67 |  -0.02  |    0.83 |   0.32  |    1.00 | 

Mari kita analisis korelasi antar variabel dalam dataset seperti yang ditampilkan tabel 3:
1. SPX (*S&P 500 Index*) dengan Variabel Lainnya:
    * Korelasi antara SPX dan GLD adalah 0.05, yang menunjukkan hubungan yang sangat lemah atau bahkan tidak ada hubungan antara S&P 500 Index dan harga emas (GLD). Pergerakan harga emas tidak secara signifikan dipengaruhi oleh pergerakan pasar saham. 
    * Korelasi antara SPX dan USO adalah -0.59, yang menunjukkan hubungan negatif yang cukup kuat antara S&P 500 Index dan harga minyak (USO). Ini berarti ketika S&P 500 Index naik, harga minyak cenderung turun, dan sebaliknya ketika pasar saham (SPX) turun, harga minyak (USO) cenderung naik.
    * Korelasi antara SPX dan SLV adalah -0.27, yang menunjukkan hubungan negatif yang lemah antara S&P 500 Index dan harga perak (SLV), yang berarti bahwa pergerakan harga perak tidak terlalu dipengaruhi oleh pergerakan pasar saham.
    * Korelasi antara SPX dan EUR/USD adalah -0.67, yang menunjukkan hubungan negatif yang kuat antara S&P 500 Index dan nilai tukar EUR/USD. Ini berarti ketika S&P 500 Index naik, nilai tukar EUR/USD cenderung turun dan sebaliknya, karena EURO/USD sering dianggap sebagai *"safe haven asset"* saat pasar saham mengalami tekanan.
    
2. GLD (*SPDR Gold Shares*) dengan Variabel Lainnya:
    * Korelasi antara GLD dan USO adalah -0.19, yang menunjukkan hubungan negatif yang lemah antara harga emas (GLD) dan harga minyak (USO), di mana ini berarti pergerakan harga minyak tidak terlalu dipengaruhi oleh pergerakan harga perak.
    * Korelasi antara GLD dan SLV adalah 0.87, yang menunjukkan hubungan positif yang kuat antara harga emas (GLD) dan harga perak (SLV). Harga emas dan perak sering bergerak sejalan karena keduanya dianggap sebagai logam mulia dan sering menjadi pilihan investasi yang serupa.
    * Korelasi antara GLD dan EUR/USD adalah -0.02, yang menunjukkan hubungan yang sangat lemah atau bahkan tidak ada hubungan antara harga emas (GLD) dan nilai tukar EUR/USD.
    
3. USO (*United States Oil Fund*) dengan Variabel Lainnya:
    * Korelasi antara USO dan SLV adalah 0.17, yang menunjukkan hubungan positif yang lemah antara harga minyak (USO) dan harga perak (SLV). Hal ini berarti pergerakan harga minyak tidak terlalu dipengaruhi oleh pergerakan harga perak.
    * Korelasi antara USO dan EUR/USD adalah 0.83, yang menunjukkan hubungan positif yang kuat antara harga minyak (USO) dan nilai tukar EUR/USD. Ketika harga minyak naik, nilai tukar EUR/USD cenderung naik juga.
    
4. SLV (*iShares Silver Trust*) dengan EUR/USD:
    * Korelasi antara SLV dan EUR/USD adalah 0.32, yang menunjukkan hubungan positif yang lemah antara harga perak (SLV) dan nilai tukar EUR/USD.
    
Penjelasan di atas dapat memberikan pemahaman yang lebih baik tentang data. Misalnya, jika investor ingin berinvestasi di SPX, maka investor perlu mempertimbangkan risiko turunnya USO dan EUR/USD. Demikian pula, jika investor ingin berinvestasi di GLD atau SLV, maka investor perlu mempertimbangkan risiko turunnya SPX.
  
Grafik 1 : Menampilkan korelasi antar variabel dengan heatmap
![Heatmap](https://raw.githubusercontent.com/ERIKABUDIARTI/Gold-Predict/main/heatmap.png)

Grafik 2 : Menampilkan pola korelasi antar variabel dengan pairplot
![Pairplot](https://raw.githubusercontent.com/ERIKABUDIARTI/Gold-Predict/main/pair%20plot.png)

Pada grafik 1, korelasi antar variabel divisualisasikan dengan gradasi warna yang berbeda dalam bentuk heatmap, sedangkan Grafik 2 memvisualisasikan pola korelasi dari semua variabel numerikal dengan pairplot.


## Data Preparation

**Tahapan dalam Persiapan Data**
1. **Impor library dan dataset**:   
    * Tahapan ini penting karena kita perlu memuat *library Python* dan *dataset* ke dalam *environment* (seperti Jupyter Notebook atau IDE lainnya) sebelum memulai analisis data.
    * Proses: impor *library Python* seperti *pandas*, *numpy*, dan lainnya yang dibutuhkan untuk mengolah data, kemudian impor *dataset* dari sumbernya (misalnya, *file CSV*, *file XLS*, atau *database*) ke *environment*.

2. **Pemeriksaan data**:   
    * Pemeriksaan data membantu kita untuk memahami dataset, mengidentifikasi masalah awal, dan memastikan kualitas data.
    * Proses: melihat struktur data, menampilkan beberapa sampel data, memeriksa tipe data kolom, mengidentifikasi nilai yang hilang, dan melakukan analisis statistik deskriptif.

3. **Eksplorasi data**:
    * Eksplorasi data melibatkan analisis lebih mendalam terhadap dataset, termasuk visualisasi data, pemahaman distribusi data, identifikasi pola, dan analisis korelasi antar variabel.
    * Proses: Membuat visualisasi seperti *histogram*, *scatter plot*, atau *box plot* untuk memahami distribusi dan hubungan antar variabel. Melakukan analisis statistik tambahan untuk menemukan pola atau tren yang mungkin relevan dengan tujuan analisis.

4. **Pembersihan data**:   
    * Data seringkali memiliki nilai yang hilang, *outlier*, atau kesalahan lain yang dapat mempengaruhi hasil analisis. Tahapan ini diperlukan untuk membersihkan data dari masalah-masalah tersebut.
    * Proses: Pembersihan data dapat melibatkan pengisian nilai yang hilang, menghapus baris atau kolom yang tidak relevan, menangani *outlier*, dan melakukan transformasi data jika diperlukan.

5. **Pembagian data**:   
    * Data perlu dibagi menjadi set pelatihan (*training set*) dan set pengujian (*testing set*) untuk melatih dan menguji model machine learning.
    * Proses: data dibagi secara acak menjadi dua bagian, misalnya 70% untuk pelatihan dan 30% untuk pengujian atau 80% untuk pelatihan dan 20% untuk pengujian. Pembagian data ini penting untuk menghindari *overfitting* (model yang terlalu cocok dengan data pelatihan) dan memastikan evaluasi yang obyektif.

6. **Normalisasi data**:   
    * Normalisasi data diperlukan ketika berbagai fitur (kolom) dalam dataset memiliki skala yang berbeda yang bisa mempengaruhi kinerja beberapa algoritma *machine learning*. Normalisasi data mengubah skala fitur-fitur sehingga nilai-nilai mereka berada dalam rentang yang serupa. Ini penting karena banyak algoritma *machine learning*, seperti *linear regression* atau *k-means clustering*, sangat sensitif terhadap skala data. Tanpa normalisasi, variabel dengan skala besar dapat mendominasi hasil analisis, sementara variabel dengan skala kecil mungkin diabaikan. Dengan normalisasi, kita memastikan bahwa semua variabel memiliki kontribusi yang setara dalam analisis, sehingga hasilnya lebih andal dan akurat. 
    * Proses: Normalisasi melibatkan proses mengubah skala data. Metode yang umum digunakan termasuk *Min-Max Scaling*, *Standard Scaling*, *Z-Score Scaling*, atau menggunakan teknik seperti PCA (*Principal Component Analysis*) jika diperlukan.


## Modeling

### 1. Linear Regression
**Cara Kerja**: 
*Linear Regression* adalah salah satu algoritma yang digunakan dalam pembelajaran mesin untuk memodelkan hubungan linier antara variabel input (fitur) dan variabel output (target). Algoritma ini mencoba untuk menemukan garis lurus (dalam kasus regresi linear sederhana) atau permukaan datar (dalam regresi linear berganda) yang terbaik menggambarkan hubungan antara fitur dan target.

**Kelebihan**:
1. Sederhana dan Interpretatif: Linear Regression adalah salah satu algoritma yang paling mudah dipahami dan diinterpretasikan. Hasilnya berupa persamaan linear yang dapat memberikan wawasan tentang hubungan antara variabel input dan output.
2. Ketajaman: Algoritma ini cocok untuk masalah di mana hubungan antara variabel input dan output bersifat linier. Ketika hubungan antara variabel cukup linear, *Linear Regression* dapat memberikan prediksi yang akurat.
3. Komputasi Ringan: Pelatihan model *Linear Regression* relatif cepat, dan prediksi juga efisien dari segi waktu.

**Kekurangan**:
1. Sensitif terhadap *Outlier*: *Linear Regression* dapat sangat sensitif terhadap data *outlier*, yang dapat memengaruhi hasil prediksi secara signifikan.
2. Mengabaikan Non-linearitas: *Linear Regression* hanya cocok untuk masalah dengan hubungan linear antara variabel input dan output. Jika hubungan bersifat non-linear, maka model ini tidak akan memberikan hasil yang baik.

**Parameter yang dapat digunakan**:
1. *'copy_X'*
    Ini adalah parameter yang menentukan apakah data input (X) harus disalin sebelum digunakan dalam pelatihan model. Nilai *default* adalah *True*, yang berarti data akan disalin.

2. *'fit_intercept'*
    Parameter ini menentukan apakah model harus memperhitungkan intercept (bias) dalam persamaan regresi. Nilai *default* adalah *True*, yang berarti intercept akan dihitung.

3. *'n_jobs'*
    Ini adalah parameter yang mengontrol jumlah pekerjaan paralel yang digunakan dalam pelatihan model. Nilai *default* adalah *None* berarti hanya satu pekerjaan yang digunakan. Jika kita ingin menggunakan paralelisasi, dapat mengatur nilai ini ke jumlah inti *CPU* yang ingin Anda gunakan.

4. *'positive'*
    Parameter ini mengatur apakah model harus memastikan bahwa koefisien regresi yang dihasilkan harus bernilai positif. Nilai *default* adalah *False*, yang berarti model tidak membatasi koefisien menjadi positif.

5. *'coefficients'*
    Parameter ini adalah bobot yang diberikan kepada setiap fitur dalam model regresi, yang mengindikasikan seberapa kuat fitur tersebut mempengaruhi prediksi.

### 2. Support Vector Machine Regressor
**Cara Kerja**: 
*SVM Regressor* adalah algoritma yang digunakan untuk membangun model yang dapat memprediksi nilai kontinu (bukan kategori). Algoritma ini mencoba untuk menemukan garis atau permukaan yang dapat memaksimalkan margin (jarak) antara titik data yang dihasilkan dan garis/permukaan tersebut. *SVM Regressor* mencari model yang memiliki kesalahan prediksi yang paling sedikit.

**Kelebihan**:
1. Robust terhadap *Outlier*: *SVM Regressor* cenderung lebih tahan terhadap *outlier* daripada *Linear Regression*. Ini berarti hasil prediksi dapat lebih stabil dalam kehadiran data yang tidak biasa.
2. Mengatasi Non-linearitas: *SVM Regressor* dapat dengan mudah diubah menjadi model regresi non-linear dengan menggunakan kernel yang sesuai. Ini memungkinkan *SVM Regressor* untuk mengatasi masalah dengan hubungan yang lebih kompleks antara variabel *input* dan *output*.
3. Generalisasi Baik: *SVM Regressor* biasanya memiliki kemampuan untuk menggeneralisasi dengan baik, bahkan dalam kasus di mana jumlah fitur sangat besar dibandingkan dengan jumlah sampel.


**Kekurangan**:
1. Kompleksitas Parameter: *SVM Regressor* memiliki beberapa parameter yang harus diatur dengan benar, seperti jenis kernel, parameter regulasi, dan lainnya. Menentukan parameter-optimal dapat memerlukan pengetahuan tambahan dan percobaan yang intensif.
2. Komputasi Intensif: Pelatihan model *SVM Regressor* biasanya memerlukan waktu yang lebih lama daripada Linear Regression, terutama dalam kasus data yang besar.
3. Keterbatasan dalam Data Besar: *SVM Regressor* dapat mengalami kesulitan dalam menangani data yang sangat besar karena memerlukan perhitungan matriks kernel yang intensif. 

**Parameter yang dapat digunakan**:
1. *'C' (Penalization Parameter)*:   
    'C' adalah parameter yang mengontrol tingkat regularisasi dalam *SVM Regressor*. Nilai C yang lebih tinggi cenderung menghasilkan model yang lebih ketat dengan menghukum pelanggaran margin yang lebih besar. Sebaliknya, nilai C yang lebih rendah cenderung menghasilkan model yang lebih toleran terhadap pelanggaran margin.

2. *'cache_size' (Ukuran Cache)*:   
    Parameter ini mengatur ukuran *cache* dalam megabita yang digunakan untuk menyimpan hasil komputasi dalam pelatihan *SVM Regressor*. Menggunakan *cache* dapat meningkatkan kecepatan pelatihan jika memori yang cukup tersedia.

3. *'coef0' (Konstanta dalam Kernel)*:  
    'coef0' adalah konstanta yang digunakan dalam beberapa fungsi kernel, seperti kernel sigmoid dan polinomial. Ini memungkinkan penyesuaian bentuk fungsi kernel.

4. *'degree' (Derajat dalam Kernel Polinomial)*:    
    Parameter ini digunakan jika kernel yang digunakan adalah kernel polinomial. Ini mengatur derajat polinomial yang akan digunakan dalam fungsi kernel.

5. *'epsilon' (Toleransi Epsilon)*:   
    'epsilon' adalah nilai toleransi kesalahan dalam *SVM Regressor*. Ini mengontrol sejauh mana prediksi model dapat berjarak dari nilai target tanpa dianggap sebagai pelanggaran.

6. *'gamma' (Koefisien Kernel)*:    
    Parameter 'gamma' mengatur seberapa banyak pengaruh setiap titik data individu terhadap pembentukan margin. Nilai yang tinggi menghasilkan margin yang lebih ketat.

7. *'kernel' (Fungsi Kernel)*:   
    'kernel' adalah jenis fungsi kernel yang akan digunakan dalam SVM Regressor, seperti 'linear', 'poly' (polinomial), 'rbf' (*radial basis function*), dll.

8. *'max_iter' (Jumlah Iterasi Maksimum)*:   
    Parameter ini mengatur jumlah iterasi maksimum yang akan dilakukan dalam proses pelatihan *SVM Regressor*.

9. *'shrinking' (Pengecilan)*:   
    Ini adalah parameter boolean yang mengontrol apakah pengecilan margin akan diaktifkan atau dinonaktifkan. Pengecilan dapat meningkatkan kecepatan pelatihan.

10. *'tol' (Toleransi Kesalahan)*:   
    'tol' mengatur toleransi kesalahan untuk menghentikan pelatihan jika perubahan dalam solusi *SVM Regressor* lebih kecil.

11. *'verbose' (Keluaran Verbose)*:    
    Jika diatur ke *True*, parameter ini akan menghasilkan output yang lebih banyak selama pelatihan, yang dapat digunakan untuk pemantauan pelatihan.


## Evaluation
 
### Metrik Evaluasi dan penjelasannya
 Untuk mengevaluasi akurasi prediksi harga emas, sejumlah metrik evaluasi yang dapat digunakan adalah:
1. **Mean Absolute Error (MAE)**:    
    * *Formula*: MAE = (1/n) * Σ |*actual - predicted*|
    * MAE mengukur rata-rata dari selisih absolut antara nilai aktual dan nilai prediksi oleh model.
    * Semakin rendah nilai MAE, semakin baik kinerja model karena prediksi lebih mendekati nilai aktual.  
    * MAE berguna ketika outlier (nilai yang jauh dari rata-rata) dalam data tidak memiliki dampak yang besar pada evaluasi model.
    

2. **Mean Squared Error (MSE)**:
    * *Formula*: MSE = (1/n) * Σ (*actual - predicted*)^2
    * MSE mengukur rata-rata dari kuadrat selisih antara nilai aktual dan nilai yang diprediksi oleh model.
    * Seperti MAE, tujuan utama adalah mengukur sejauh mana prediksi model dari nilai aktual. Namun, MSE memberi bobot lebih besar pada perbedaan yang lebih besar seperti outlier.
    * Nilai MSE selalu positif, dan semakin rendah nilainya semakin baik kinerja model.
    

3. **Coefficient of Determination (R2)**:
    * *Formula*: R2 = 1 - (MSE(*model*) / MSE(*mean*))
    * R2 dikenal sebagai koefisien determinasi, mengukur variasi dalam data yang dapat dijelaskan oleh model. Nilai R2 berkisar antara 0 dan 1.
    * R2 = 0 berarti model tidak menjelaskan variasi sama sekali, sedangkan R2 = 1 berarti model menjelaskan semua variasi dengan sempurna.
    * Nilai R2 yang positif menunjukkan bahwa model lebih baik daripada menggunakan nilai rata-rata sederhana untuk memprediksi data.
    
Perbandingan dari ketiga metrik:
- MAE lebih mudah diinterpretasikan karena memiliki satuan yang sama dengan variabel target dan memberikan gambaran tentang besarnya kesalahan prediksi dalam satuan yang dimengerti.
- MSE lebih sensitif terhadap kesalahan besar, yang dapat membuatnya lebih cocok untuk kasus di mana kesalahan besar adalah masalah serius.
- R2 memberikan gambaran tentang sejauh mana model cocok dengan data, dan semakin tinggi nilainya, semakin baik modelnya. Namun, R2 dapat memberikan hasil yang kurang informatif jika model regresi tidak sesuai dengan data dengan baik.

### Memilih model yang terbaik berdasarkan metrik evaluasi

            Tabel 4 : Skor MAE, MSE dan R2 dengan parameter cv=5      
|                   | MAE *Train*| MAE *Test*|MSE *Train*|MSE *Test*|R2 *Train*|R2 *Test*|
|-------------------|------------|-----------|-----------|----------|----------|---------|
| Linear Regression |   8.343    |    8.018  |   132.806 |  126.818 |   0.683  |   0.691 | 
| SVM Regressor     |  14.057    |   14.128  |   370.107 |  369.564 |   0.116  |   0.099 |

Tabel 4 memberikan *summary* hasil evaluasi model *machine learning* dengan menggunakan metrik MAE, MSE dan R2. Skor metrik MAE dan MSE dengan algoritma *Linear Regression* lebih rendah daripada *SVM Regressor*, sedangkan metrik R2 dengan algoritma *SVM Regressor* lebih rendah daripada *Linear Regression*.

**Kesimpulan**:
1. **MAE (Mean Absolute Error)**:    
    MAE yang *lebih rendah* adalah yang lebih baik. Semakin rendah nilai MAE, semakin baik model dalam melakukan prediksi.

2. **MSE (Mean Squared Error)**:    
    MSE yang *lebih rendah* adalah yang lebih baik. Semakin rendah nilai MSE, semakin baik model dalam mengurangi kesalahan prediksi.

3. **R-squared (R2)**:   
    R2 yang *lebih tinggi* adalah yang lebih baik. Nilai R2 yang semakin tinggi menunjukkan bahwa model lebih cocok dengan data.

Berdasarkan hasil permodelan dan evaluasi, model terbaik untuk diterapkan pada dataset prediksi emas adalah **Support Vector Machine Regressor**

---

**Referensi**:
[1] Anisa Aulia, "Prediksi Harga Emas dengan Menggunakan Algoritma Support Vector Regression (Svr) dan Linear Regression (LR)", Jurnal Ilmiah Wahana Pendidikan, Vol.8 No.5, 2022. 



**---Ini adalah bagian akhir laporan---**

