# Penjelasan Deteksi Tepi dengan Sobel, Prewitt, Roberts, dan Canny

## Deskripsi Kode
Kode Python yang dilampirkan menggunakan berbagai metode deteksi tepi pada citra grayscale: Sobel, Prewitt, Roberts, dan Canny. Berikut adalah penjelasan dari setiap metode:

### 1. Fungsi `apply_sobel()`
- Menggunakan operator Sobel untuk mendeteksi tepi dalam arah horizontal (x) dan vertikal (y).
- Menggabungkan gradien dari kedua arah menggunakan magnitude.
- Memberikan hasil tepi yang halus dengan penekanan pada kontur utama.

### 2. Fungsi `apply_prewitt()`
- Menggunakan operator Prewitt, yaitu filter linier untuk mendeteksi tepi horizontal dan vertikal.
- Kernel Prewitt menghitung gradien dan hasilnya digabungkan menggunakan magnitude.
- Hasilnya mirip Sobel tetapi lebih kasar.

### 3. Fungsi `apply_roberts()`
- Menggunakan operator Roberts untuk mendeteksi tepi dengan menghitung perbedaan intensitas piksel secara diagonal.
- Sensitif terhadap noise dan memberikan hasil tepi yang tajam tetapi tipis.

### 4. Fungsi `apply_canny()`
- Metode deteksi tepi Canny melibatkan langkah-langkah berikut:
  1. Gaussian blur untuk mengurangi noise.
  2. Deteksi gradien menggunakan operator Sobel.
  3. Non-maximum suppression untuk menyempurnakan garis tepi.
  4. Penggunaan threshold ganda untuk mendeteksi dan menghubungkan tepi yang signifikan.
- Memberikan hasil deteksi tepi yang akurat dan detail.

---

## Penjelasan Hasil
### 1. **Gambar Asli**
- Gambar grayscale yang menjadi input untuk deteksi tepi.

### 2. **Sobel**
- Menampilkan tepi utama dari gambar dengan hasil yang halus dan detail.
- Cocok untuk mendeteksi kontur besar, seperti tepi jembatan.

### 3. **Prewitt**
- Mirip dengan Sobel tetapi lebih sederhana. Hasilnya sedikit kurang halus.
- Kurang optimal untuk gambar dengan noise atau detail halus.

### 4. **Roberts**
- Memberikan hasil tepi yang tajam dan garis tipis.
- Efektif untuk gambar tanpa banyak noise, tetapi kurang optimal untuk detail kompleks.

### 5. **Canny**
- Memberikan hasil deteksi tepi paling presisi dan halus.
- Cocok untuk aplikasi yang memerlukan analisis tepi yang akurat, seperti pengenalan objek atau segmentasi.

---

## Kesimpulan
- **Sobel** dan **Prewitt**: Sederhana dan cocok untuk aplikasi dasar.
- **Roberts**: Memberikan tepi yang tajam tetapi rentan terhadap noise.
- **Canny**: Deteksi tepi yang paling presisi, cocok untuk analisis citra tingkat lanjut meskipun lebih kompleks.

Jika Anda memerlukan penyesuaian atau penjelasan tambahan, silakan hubungi saya!
