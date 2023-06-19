Context


Pada era modern seperti saat ini, penggunaan mobil sebagai alat mobilitas sangat dibutuhkan untuk menunjang mobilisasi bahkan pengiriman barang. Tidak hanya itu, mobil juga memiliki manfaat lain yang dapat dimanfaatkan sesuai dengan keperluan. Mobil juga menjadi salah satu moda transportasi yang paling populer di Arab Saudi. Arab Saudi merupakan negara terbesar di Timur Tengah. Terdapat banyak pabrik mobil yang berada di Arab Saudi. Pabrik mobil sangat diminati di Arab Saudi diantaranya disebabkan oleh harga bahan bakar disana yang rendah. Bahkan, harga bahan bakar di Arab Saudi merupakan salah satu yang terendah di dunia. Suhu yang tinggi juga membuat sepeda motor kurang diminati dan cenderung membuat mobil lebih diminati. Beberapa artikel memaparkan bahwa pasar mobil bekas di Arab Saudi memiliki perbandingan pembelian mobil bekas sebesar 2 kali lipat terhadap mobil baru.

Permintaan yang cukup besar terhadap mobil bekas menghasilkan beberapa platform di situs web untuk jual beli mobil bekas, seperti syarah.com. Pelanggan dapat memilih mobil yang sesuai dengan keinginan mereka. Harga yang ada bergantung pada spesifikasi mobil yang dimiliki. Terdapat begitu banyak jenis mobil yang berbeda berdasarkan spesifikasinya. Penentuan harga terbaik diperlukan saat menjual atau membeli mobil agar tidak membuat keputusan yang salah. Hal ini diperlukan karena apabila harga terlalu tinggi mobil akan sulit terjual, sebaliknya apabila harga terlalu rendah keuntungan yang didapatkan akan lebih kecil. 

Problem Statement


Dengan terus berkembangnya pasar mobil bekas di Arab Saudi, penentuan harga mobil bekas ini memiliki tantangan yang perlu diatasi. Sulitnya menentukan harga mobil bekas yang akurat dan kompetitif karena banyaknya variasi dan spesifikasi mobil. Tidak terjadi underprice maupun overprice dalam penentuan harga. Tantangan untuk mengoptimalkan pengalaman jual beli mobil bekas melalui platform online dengan menyediakan harga yang kompetitif dan transparan. Dengan mengatasi tantangan tersebut, diharapkan dapat memberikan manfaat bagi semua pihak yang terlibat dalam pasar mobil bekas di Arab Saudi, termasuk perusahaan, calon pembeli, dan penjual potensial. 


Goals

Berdasarkan pernyataan masalah di atas, pasar jual beli mobil bekas membutuhkan sebuah alat tools yang dapat memprediksi harga mobil bekas yang akurat dan kompetitif. Hal ini tentu menjadi suatu tantangan bagi para pelaku kepentingan atau pelaku pasar karena terdapat banyak jenis, variasi, dan spesifikasi mobil yang berbeda. 

Dengan adanya tools ini, diharapkan dapat menentukan prediksi harga terbaik sehingga meningkatkan efisiensi dan kecepatan dalam menentukan harga mobil bekas dengan mengurangi waktu yang dihabiskan untuk penelitian dan perbandingan harga. Memberikan solusi yang komprehensif dan terpercaya dalam menentukan harga mobil bekas yang beragam, sehingga meningkatkan kepercayaan pembeli dan penjual potensial terhadap platform jual beli mobil bekas. Meningkatkan keuntungan dan pengalaman pengguna bagi perusahaan atau platform jual beli mobil bekas dengan menawarkan harga kompetitif yang sesuai dengan nilai pasar. Menarik minat lebih banyak pelanggan potensial untuk belanja di platform tersebut melalui harga yang akurat dan kompetitif dalam jual beli mobil bekas. Kemudian, meningkatkan kepuasan pelanggan dengan memberikan kemudahan dan kepastian dalam menentukan spesifikasi dan harga mobil bekas yang diinginkan.

Analytic Approach

Dalam menghadapi permasalahan tersebut, yang perlu kita lakukan adalah melakukan analisis terhadap data untuk mengidentifikasi pola-pola pada fitur-fitur yang membedakan satu mobil dengan mobil lainnya. Selanjutnya, kita akan membuat model regresi sebagai 'tool' untuk membantu marketplace dalam mengambil keputusan yang akurat dalam memprediksi harga mobil bekas. Hal ini tentunya agar dapat menciptakan model yang baik guna membantu marketplace dan memberikan kepuasan kepada pelanggan dalam melakukan pembelian melalui platform tersebut dan perusahaan memperoleh keuntungan yang optimal.

Metric Evaluation

Penghapusan data outlier pada model ini hanya dilakukan oleh data outlier dengan nilai ekstrem yang tidak realistis. Oleh karena itu, data masih akan memiliki beberapa outlier yang tertinggal. Hal ini membuat metrik evaluasi model yang akan digunakan tidak sensitif terhadap outlier. Sehingga, beberapa metrik yang digunakan dalam model ini diantaranya adalah:

1. MAE (Mean Absolute Error): Metrik ini menggambarkan selisih rata-rata absolut antara hasil prediksi dan hasil aktual. Metrik ini direkomendasikan karena data yang digunakan memiliki beberapa outlier. Karena menggunakan nilai absolut, metrik ini tidak peduli dengan selisih yang menghasilkan hasil negatif. Semakin kecil nilai metrik ini, semakin baik hasil prediksi yang diperoleh. 

2. MAPE (Mean Absolute Percentage Error): Metrik ini menggambarkan persentase rata-rata selisih absolut antara hasil prediksi dan hasil aktual. MAPE memiliki perbedaan dengan MAE, yaitu metrik ini perlu mengubah selisih menjadi persentase saja. Karena merupakan persentase, nilai metrik ini berkisar antara 0 hingga 1.

3. RMSLE(Root Mean Squared Log Error): Metrik ini digunakan saat data memiliki skewness yang tinggi dengan variasi yang berkisar dari kecil hingga sangat besar. Perbedaan varians yang besar dapat diatasi karena perhitungan RMSLE adalah dengan mengonversi data ke skala logaritmik terlebih dahulu, kemudian dihitung rata-ratanya dan diakar pangkat dua. Dataset yang memenuhi persyaratan tersebut sehingga metrik ini cocok digunakan untuk mengevaluasi hasil dari model.

4. R- square: Metrik ini menggambarkan persentase sejauh mana semua fitur mempengaruhi target. Semakin tinggi nilai persentasenya, semakin besar pengaruh feature terhadap target. Metrik ini hanya digunakan saat memilih model dasar karena dari setiap model dapat terlihat dengan jelas seberapa besar persentase pengaruh feature terhadap target.

Metrik seperti MSE(Mean Squared Error), RMSE(Root Mean Squared Error), dan RMPSE(Root Mean Square Percentage Error) tidak cocok digunakan dalam data ini karena sensitif terhadap adanya outlier. Outlier merujuk pada data yang jauh berbeda atau ekstrim dari sebagian besar data lainnya. Outlier dapat memiliki dampak yang signifikan pada hasil metrik seperti MSE, RMSE, dan RMSPE karena metrik-metrik tersebut menghitung perbedaan kuadrat atau persentase perbedaan antara nilai aktual dan nilai prediksi. Outlier dengan nilai yang ekstrem dapat memberikan kontribusi yang tidak proporsional terhadap perhitungan metrik, sehingga hasil evaluasi menjadi bias dan tidak akurat. 

Dalam konteks ini, metrik evaluasi yang lebih tahan terhadap outlier, seperti MAE dapat lebih sesuai untuk digunakan. Metrik-metrik ini mengukur perbedaan absolut antara nilai aktual dan nilai prediksi, sehingga lebih stabil terhadap keberadaan outlier dalam data. Dengan menggunakan metrik evaluasi yang lebih tahan terhadap outlier, evaluasi kualitas prediksi model akan lebih akurat dan dapat memberikan informasi yang lebih relevan.

Data Understanding
- Dataset merupakan data Mobil Bekas di Arab Saudi.
- Setiap baris data merepresentasikan informasi terkait mobil bekas, harga, dan beberapa spesifikasinya.
