
# TEORI DAN PENJELASAN CODINGAN

OpenCV (Open Source Computer Vision Library):
> Image Loading and Conversion: OpenCV menyediakan fungsi untuk memuat gambar dari berbagai format file seperti JPEG, PNG, dll. Kemudian, gambar dapat diubah dari ruang warna default BGR (Blue-Green-Red) OpenCV menjadi RGB (Red-Green-Blue) yang umum digunakan dalam kebanyakan perpustakaan pemrosesan gambar seperti Matplotlib.

> Geometric Transformations: OpenCV memungkinkan untuk melakukan transformasi geometris seperti rotasi, penskalaan, pemotongan, pemutaran, dan translasi pada gambar. Transformasi ini menggunakan matriks transformasi affine atau matriks rotasi untuk mengubah posisi dan orientasi piksel dalam gambar.

> Image Manipulation: Selain transformasi geometris, OpenCV juga mendukung manipulasi gambar lain seperti mengubah ukuran (resize), memanipulasi nilai piksel secara langsung, dan berbagai operasi seperti filter, deteksi tepi, dan segmentasi.

Matplotlib:
>Visualization: Matplotlib adalah perpustakaan yang sangat populer untuk visualisasi data di Python. Dalam konteks pengolahan gambar, Matplotlib digunakan untuk menampilkan gambar-gambar hasil dari operasi yang dilakukan dengan OpenCV.

>Subplotting: Fungsi subplot dari Matplotlib memungkinkan pengaturan tata letak gambar-gambar dalam grid. Hal ini sangat berguna untuk membandingkan hasil dari berbagai transformasi atau operasi pada gambar yang sama.

PENJELASAN CODINGAN
1. Mengimport library yang diperlukan (cv2 untuk OpenCV, numpy untuk operasi array, matplotlib.pyplot untuk plotting).
2. Membaca gambar dari path "PA-PC_202231064_AISYAH TRI NURFAJRI_B.jpg" menggunakan cv2.imread() dan mengubah warna dari BGR (default OpenCV) ke RGB menggunakan cv2.cvtColor().
3. Menghitung dimensi gambar (h untuk tinggi, w untuk lebar) menggunakan original_image.shape.
Menghitung titik pusat rotasi di tengah gambar.
Membuat matriks transformasi rotasi sebesar 45 derajat menggunakan cv2.getRotationMatrix2D().
Melakukan rotasi gambar menggunakan cv2.warpAffine() dengan matriks transformasi M.
4. Meresize gambar menjadi ukuran baru (50, 100) menggunakan cv2.resize().
5. Melakukan pemotongan (cropping) pada gambar asli dari baris 200 sampai 370 dan kolom 100 sampai 250 menggunakan indeks array NumPy.
6. Membalik gambar secara horizontal menggunakan cv2.flip() dengan parameter flipCode=1.
7. Membuat matriks transformasi translasi sebesar (50, 50) menggunakan np.float32().
Melakukan translasi gambar menggunakan cv2.warpAffine() dengan matriks transformasi M.
8. Membuat list titles yang berisi judul-judul untuk setiap gambar transformasi.
Membuat list images yang berisi hasil transformasi gambar.
Membuat plot grid subplot 2x3 dengan plt.subplot() untuk menampilkan setiap gambar transformasi beserta judulnya.
Menampilkan plot menggunakan plt.show().

