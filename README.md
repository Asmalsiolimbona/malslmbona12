
# Project Akhir Pengolahan citra

Berikut ini adalah tahapan-tahapan cara menyelesaikan proyek deteksi plat nomor secara rinci:

1.) Praproses Citra (Image Preprocessing): Tahap ini bertujuan untuk mempersiapkan citra agar lebih mudah untuk dideteksi plat nomornya. Beberapa langkah praproses yang umum dilakukan meliputi:

- Konversi citra ke skala abu-abu (grayscale): Mengubah citra ke dalam skala abu-abu untuk mengurangi kompleksitas pengolahan data dan meningkatkan efisiensi.
- Reduksi noise dengan Gaussian Blur: Menggunakan filter Gaussian Blur untuk mengurangi noise pada citra agar kontur lebih jelas.
- Deteksi tepi (Edge Detection): Menggunakan algoritma Canny untuk mendeteksi tepi pada citra. Tepi akan membantu dalam mengidentifikasi kontur objek yang lebih lanjut.

2.) Deteksi Plat Nomor (License Plate Detection): Pada tahap ini, kita mencari kontur yang mungkin mewakili plat nomor pada citra. Langkah-langkah yang umum dilakukan adalah:

- Mencari kontur pada citra: Menggunakan metode seperti findContours() untuk menemukan kontur pada citra yang telah diproses. Kontur adalah kurva yang melingkari area objek pada citra.
- Memfilter dan memilih kontur yang relevan: Memfilter kontur berdasarkan beberapa kriteria, seperti ukuran dan bentuk, untuk memilih kontur yang kemungkinan merupakan plat nomor.
- Mengaproksimasi kotak pada plat nomor: Menggunakan teknik approxPolyDP() untuk mengaproksimasi kontur menjadi bentuk dengan sisi-sisi lurus. Pada umumnya, plat nomor memiliki bentuk persegi atau persegi panjang.

3.) Crop Plat Nomor (License Plate Cropping): Setelah mendapatkan kontur yang mewakili plat nomor, langkah selanjutnya adalah memotong (crop) bagian citra yang mengandung plat nomor. Langkah-langkah yang biasanya dilakukan adalah:

- Menggunakan minAreaRect(): Menggunakan metode minAreaRect() untuk mendapatkan persegi panjang terkecil yang membungkus kontur plat nomor.
- Transformasi Perspektif (Perspective Transformation): Menggunakan getPerspectiveTransform() untuk mendapatkan matriks transformasi perspektif berdasarkan sudut dan ukuran plat nomor. Matriks transformasi ini digunakan untuk mengubah perspektif citra dan mendapatkan gambar plat nomor yang rata.
- Menerapkan transformasi perspektif: Menggunakan metode warpPerspective() untuk menerapkan transformasi perspektif pada citra dan mendapatkan plat nomor yang dicrop.

4.) Binary Image dan Edges Image: Untuk memperjelas tampilan plat nomor yang telah di-crop, biasanya dilakukan konversi citra plat nomor ke dalam bentuk binary dan edges.

- Binary Image: Mengubah citra plat nomor ke dalam citra biner, di mana piksel-piksel hanya memiliki nilai hitam (0) atau putih (255). Ini dilakukan dengan menggunakan thresholding, di mana piksel dengan intensitas di atas ambang batas akan diubah menjadi putih, dan di bawah ambang batas akan diubah menjadi hitam.
- Edges Image: Menggunakan algoritma deteksi tepi, seperti Canny, pada citra plat nomor untuk menemukan tepi yang signifikan. Ini membantu dalam mengidentifikasi kontur plat nomor dengan lebih jelas.
Setelah tahapan-tahapan di atas selesai dilakukan, Anda dapat menampilkan gambar-gambar hasil deteksi dan crop plat nomor, binary image, dan edges image menggunakan library OpenCV seperti yang telah dijelaskan pada contoh source code sebelumnya.

Penting untuk dicatat bahwa proyek ini merupakan pendekatan umum dalam deteksi dan crop plat nomor, dan bisa mengalami variasi tergantung pada data dan kondisi spesifik. Dalam prakteknya, Anda mungkin perlu melakukan tuning dan eksperimen untuk mencapai hasil yang optimal.








## 🚀 About Me
I'm a full stack developer...


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://katherineoelsner.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/)

