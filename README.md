# Laporan Proyek Machine Learning - Tabita Novi Sinaga

## Domain Proyek
#### Latar Belakang
Domain proyek Medical Insurance Cost Prediction ini berada dalam ranah industri asuransi kesehatan, sebuah sektor yang berperan penting dalam memberikan perlindungan finansial terhadap risiko kesehatan individu dan keluarga. Dalam industri ini, perusahaan asuransi menetapkan biaya premi yang harus dibayarkan oleh pemegang polis sebagai imbalan atas perlindungan yang diberikan terhadap biaya medis yang mungkin timbul di masa depan.

Proyek ini memiliki relevansi yang kuat dengan industri asuransi kesehatan, terutama dalam mendukung penentuan biaya asuransi yang lebih akurat. Dengan memanfaatkan data seperti usia, jenis kelamin, indeks massa tubuh (BMI), jumlah anak tanggungan, status merokok, wilayah tempat tinggal, dan biaya medis sebelumnya, model prediktif yang dikembangkan dalam proyek ini dapat membantu perusahaan asuransi memproyeksikan biaya asuransi secara lebih tepat. Perhitungan berbasis data ini memungkinkan penetapan premi yang selaras dengan risiko kesehatan masing-masing individu.

Selain itu, model ini juga mendorong terciptanya sistem penetapan biaya yang lebih adil bagi calon pemegang polis. Dengan mempertimbangkan berbagai variabel risiko secara menyeluruh, pendekatan berbasis data ini dapat mengurangi kemungkinan diskriminasi dalam penetapan premi, sehingga menghasilkan biaya asuransi yang lebih sesuai dan proporsional dengan kondisi calon nasabah.

Dari sisi perusahaan asuransi, penggunaan model prediktif ini tidak hanya meningkatkan akurasi dalam estimasi biaya, tetapi juga membantu dalam pengelolaan risiko keuangan dan efisiensi operasional. Sementara itu, bagi calon pemegang polis, model ini dapat memberikan gambaran yang lebih transparan dan rasional mengenai biaya yang akan mereka tanggung, sehingga mereka dapat merasa lebih yakin terhadap perlindungan kesehatan yang diperoleh.

Secara keseluruhan, proyek Medical Insurance Cost Prediction ini tidak hanya berkontribusi dalam pengambilan keputusan berbasis data di sektor asuransi kesehatan, tetapi juga membuka peluang untuk menciptakan sistem asuransi yang lebih adil, efisien, dan berorientasi pada kebutuhan individu.

## Business Understanding
Proyek Medical Insurance Cost Prediction ini dikembangkan untuk mendukung perusahaan asuransi kesehatan yang memiliki komitmen terhadap pemanfaatan teknologi dan analisis data guna meningkatkan kualitas pengambilan keputusan bisnis mereka. Perusahaan seperti ini biasanya memiliki kumpulan data pelanggan yang kaya dan terstruktur, mencakup informasi penting seperti usia, jenis kelamin, indeks massa tubuh (BMI), jumlah anak tanggungan, status merokok, wilayah tempat tinggal, serta biaya medis yang telah dikeluarkan. Dengan memanfaatkan data ini, perusahaan berupaya untuk membangun model prediktif yang mampu memperkirakan biaya medis secara akurat, sehingga premi yang dikenakan kepada calon pemegang polis dapat ditentukan berdasarkan risiko yang sesungguhnya. Permasalahan utama yang ingin diselesaikan dalam proyek ini adalah bagaimana perusahaan asuransi dapat menentukan estimasi biaya asuransi kesehatan secara lebih akurat dan efisien dengan mengandalkan data historis pelanggan. Selama ini, penetapan premi sering kali dilakukan secara umum dan tidak mempertimbangkan secara mendalam faktor-faktor risiko individu, yang bisa menyebabkan ketidakadilan dalam pembebanan biaya serta ketidaktepatan dalam mengelola risiko keuangan perusahaan. Tanpa pendekatan berbasis data, perusahaan juga kesulitan dalam mengoptimalkan efisiensi proses dan menghadapi persaingan yang semakin ketat di industri asuransi.

Tujuan dari proyek ini adalah mengembangkan model analisis prediktif berbasis machine learning yang mampu memproyeksikan biaya asuransi kesehatan dengan mempertimbangkan karakteristik individu masing-masing pelanggan. Model ini diharapkan dapat memberikan estimasi yang lebih tepat terhadap biaya yang akan dikeluarkan calon pemegang polis, memungkinkan perusahaan untuk menetapkan premi yang lebih adil, informasional, dan kompetitif. Selain itu, model ini bertujuan untuk meningkatkan efisiensi operasional perusahaan dengan mengotomatisasi proses estimasi biaya, serta memperkuat posisi perusahaan dalam pasar asuransi dengan strategi penetapan harga yang lebih cerdas dan berbasis risiko nyata. Dengan pendekatan ini, perusahaan dapat mengurangi kerugian yang tidak terduga, memperkuat hubungan dengan pelanggan, dan meningkatkan daya saing jangka panjang di industri.


### Problem Statements
- Pernyataan Masalah 1
Bagaimana meningkatkan akurasi dalam memperkirakan biaya asuransi kesehatan berdasarkan karakteristik individu?

Perusahaan asuransi kesehatan sering menghadapi kesulitan dalam menetapkan biaya asuransi yang tepat bagi calon pemegang polis karena keterbatasan dalam memahami dan memanfaatkan faktor-faktor risiko yang relevan. Tanpa pendekatan berbasis data dan analisis prediktif, estimasi biaya dapat menjadi terlalu umum dan tidak mencerminkan kondisi nyata individu, sehingga menyebabkan ketidakakuratan dalam penetapan premi.

- Pernyataan Masalah 2
Bagaimana menciptakan sistem penetapan premi yang lebih transparan agar dapat dipahami oleh calon pemegang polis?

Calon nasabah sering merasa bingung dan kurang percaya terhadap sistem penetapan premi karena tidak adanya kejelasan mengenai faktor apa saja yang memengaruhi besaran premi mereka. Minimnya transparansi ini bisa menimbulkan persepsi bahwa perusahaan asuransi bersikap tidak adil dalam menentukan biaya asuransi, padahal terdapat faktor-faktor objektif seperti usia, kebiasaan merokok, dan indeks massa tubuh (BMI) yang seharusnya bisa dijelaskan secara terbuka.

- Pernyataan Masalah 3
Bagaimana mengurangi risiko keuangan perusahaan akibat penetapan premi yang tidak sebanding dengan risiko kesehatan nasabah?

Premi yang ditetapkan terlalu rendah bagi individu dengan risiko tinggi dapat menyebabkan perusahaan menanggung klaim melebihi pendapatan dari premi tersebut. Sebaliknya, premi yang terlalu tinggi dapat menurunkan minat masyarakat untuk membeli asuransi. Keduanya sama-sama menimbulkan kerugian bagi perusahaan baik dari sisi finansial maupun persaingan di pasar.

Ketiga pernyataan masalah tersebut merupakan tantangan nyata yang dihadapi oleh perusahaan asuransi kesehatan saat ini. Oleh karena itu, melalui proyek Medical Insurance Cost Prediction ini, akan dikembangkan sebuah model prediktif berbasis machine learning yang bertujuan untuk:
- Menyediakan estimasi biaya asuransi yang lebih akurat berdasarkan karakteristik individu.
- Meningkatkan transparansi dengan mengidentifikasi dan menjelaskan faktor-faktor signifikan yang memengaruhi premi.
- Membantu perusahaan mengelola risiko keuangan secara lebih efektif dengan penetapan premi yang sesuai dengan tingkat risiko masing-masing calon pemegang polis.

### Goals
- Jawaban Pernyataan Masalah 1: Mengembangkan model prediktif yang akurat dalam memperkirakan biaya asuransi kesehatan

Tujuan utama dari proyek ini adalah membangun sebuah model prediktif berbasis machine learning yang mampu memperkirakan biaya premi asuransi kesehatan secara lebih akurat. Dengan memanfaatkan data seperti usia, jenis kelamin, BMI, status merokok, jumlah anak, dan wilayah tempat tinggal, model ini akan mengidentifikasi pola yang dapat digunakan untuk membuat prediksi premi yang tepat dan sesuai dengan karakteristik masing-masing individu. Pendekatan ini diharapkan dapat mengatasi ketidakakuratan dalam penentuan premi yang selama ini terjadi karena kurangnya analisis data yang komprehensif.

-Jawaban Pernyataan Masalah 2: Meningkatkan pemahaman dan transparansi dalam penetapan premi asuransi

Proyek ini juga bertujuan untuk menjawab keresahan calon pemegang polis terhadap kurangnya transparansi dalam proses penentuan premi. Dengan menganalisis faktor-faktor yang paling berpengaruh terhadap besaran premi, proyek ini akan membantu perusahaan asuransi memberikan penjelasan yang logis dan mudah dipahami mengenai alasan di balik nilai premi yang ditetapkan. Hasil ini dapat digunakan untuk menyusun laporan atau dashboard yang informatif, sehingga membangun kepercayaan dan meningkatkan kepuasan pelanggan terhadap kebijakan penetapan premi.

- Jawaban Pernyataan Masalah 3: Mengurangi potensi risiko finansial bagi perusahaan asuransi

Proyek ini juga bertujuan membantu perusahaan asuransi dalam mengelola risiko keuangan yang muncul akibat penetapan premi yang tidak sesuai dengan tingkat risiko kesehatan individu. Dengan memperkirakan premi berdasarkan parameter yang relevan, perusahaan dapat menghindari skenario di mana premi terlalu rendah bagi individu berisiko tinggi atau terlalu tinggi bagi individu berisiko rendah. Akurasi prediksi ini akan mendukung perencanaan keuangan dan kebijakan underwriting yang lebih sehat serta menjaga keseimbangan antara pendapatan dan potensi klaim.

Metrik Evaluasi yang Digunakan
Untuk mengukur sejauh mana tujuan-tujuan di atas tercapai, proyek ini akan menggunakan:
Mean Squared Error (MSE): Digunakan untuk menilai seberapa dekat hasil prediksi premi dengan nilai aktualnya. Semakin rendah MSE, semakin baik performa model dalam memperkirakan premi secara akurat.

Dengan menetapkan tujuan yang jelas dan metrik yang relevan, proyek ini tidak hanya akan meningkatkan kualitas prediksi premi, tetapi juga membantu perusahaan asuransi membangun sistem yang lebih adil, transparan, dan berkelanjutan.

### Solution Statements
Untuk mencapai tujuan dari proyek ini, yaitu membangun model prediktif yang akurat dalam memperkirakan biaya premi asuransi kesehatan, beberapa tahapan dan pendekatan machine learning telah dirancang sebagai berikut:

1. Eksplorasi Data (Exploratory Data Analysis - EDA)
Langkah awal yang dilakukan adalah eksplorasi data secara menyeluruh guna memahami distribusi data, pola hubungan antar fitur, serta mendeteksi adanya outlier atau nilai yang hilang. EDA juga membantu dalam proses pra-pemrosesan seperti encoding fitur kategorikal, normalisasi data jika diperlukan, serta seleksi fitur yang relevan untuk proses pelatihan model. Melalui EDA, kita dapat menemukan wawasan yang akan memperkuat kualitas dan interpretabilitas model.

2. Algoritma Random Forest
Random Forest dipilih karena memiliki kemampuan dalam menangani fitur numerik dan kategorikal secara efektif, serta tahan terhadap overfitting karena menggunakan prinsip bagging (penggabungan banyak pohon keputusan). Model ini akan memprediksi biaya premi dengan membentuk banyak pohon keputusan dan menghasilkan rata-rata prediksi sebagai output akhir.
Evaluasi kinerja model akan dilakukan menggunakan metrik Mean Squared Error (MSE) untuk mengetahui seberapa akurat prediksi premi dibandingkan nilai sebenarnya. Selain itu, feature importance dari Random Forest juga dapat digunakan untuk mendukung transparansi dalam penetapan premi.

3. Algoritma AdaBoost
AdaBoost (Adaptive Boosting) digunakan sebagai pendekatan tambahan untuk meningkatkan akurasi prediksi. Dengan menggabungkan beberapa model lemah secara iteratif dan memberikan bobot lebih pada prediksi yang sebelumnya salah, AdaBoost diharapkan mampu meningkatkan performa model secara bertahap.
Penggunaan AdaBoost memungkinkan kita untuk membandingkan apakah pendekatan boosting lebih unggul dibandingkan bagging seperti pada Random Forest. Evaluasi tetap menggunakan MSE untuk memastikan pendekatan mana yang memberikan error paling rendah dalam prediksi premi.

4. K-Nearest Neighbors (KNN)
KNN dipilih sebagai baseline model yang sederhana namun dapat memberikan gambaran awal performa prediksi berdasarkan kesamaan fitur dengan individu lainnya. KNN akan memprediksi premi berdasarkan rata-rata premi dari sejumlah tetangga terdekat dalam ruang fitur.
Meskipun KNN tidak sekompleks algoritma ensemble, model ini dapat menjadi acuan untuk membandingkan efektivitas model Random Forest dan AdaBoost. Evaluasi juga dilakukan dengan MSE, dan hasilnya akan digunakan sebagai titik acuan (baseline).

Evaluasi dan Pemilihan Model Terbaik
Setiap model akan dibandingkan berdasarkan metrik Mean Squared Error (MSE), dan model dengan MSE terendah akan dipilih sebagai model final. Selain itu, metrik tambahan seperti R-squared (R²) dan MAE (Mean Absolute Error) juga dapat digunakan sebagai pendukung evaluasi.


## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Dataset: [Medical Insurance Cost Prediction](https://www.kaggle.com/datasets/rahulvyasm/medical-insurance-cost-prediction).

![Sample](sample.png)

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
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

