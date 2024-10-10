# Projek_KDJK_kel5_P1

# Aplikasi Web "Atomic Server"

## Sekilas Tentang

Atomic Data merupakan spesifikasi modular yang dirancang untuk berbagi informasi di web. Sebagai spesifikasi modular, pengguna dapat memilih bagian yang ingin digunakan dan mengabaikan bagian lainnya. Namun, Atomic Data Core merupakan bagian yang wajib digunakan, karena semua bagian lain bergantung pada inti ini.

Atomic Data Core memungkinkan penyampaian berbagai jenis informasi, termasuk data pribadi, kosakata, metadata, dokumen, file, dan sebagainya. Sistem ini dirancang agar mudah diserialisasikan ke dalam format JSON maupun format data terhubung (linked data). Sebagai model data yang bertipe, setiap nilai dalam Atomic Data harus divalidasi berdasarkan tipe datanya, untuk memastikan kesesuaian dan keakuratan data yang digunakan.


## Instalasi

- Prasyarat, apa saja yang harus diinstal sebelumnya.
- Langkah instalasi dalam CLI.


## Konfigurasi (opsional)

Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan
- login dengan Google/Facebook
- editor Markdown
- dll


##  Maintenance (opsional)

Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (opsional)

Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.


## Cara Pemakaian

- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot


## Pembahasan

- Pendapat anda tentang aplikasi web ini
  ## Kelebihan Atomic Data

1. **Skema Fleksibel**: Atomic Data sangat cocok untuk data yang bervariasi, seperti wiki terstruktur atau data semantik, karena memungkinkan setiap objek memiliki atribut yang berbeda. Setiap sumber daya dapat memiliki properti yang berbeda sesuai kebutuhan.

2. **Data Terbuka**: Meskipun lebih sulit dibuat dibandingkan dengan JSON biasa, Atomic Data lebih mudah digunakan kembali dan dipahami. Penggunaan URL untuk setiap properti menjadikan data terdokumentasi sendiri, sehingga lebih mudah diakses dan dipahami oleh berbagai pihak.

3. **Interoperabilitas Tinggi**: Atomic Data sangat bermanfaat jika banyak kelompok harus berbagi skema yang sama. Dengan Atomic Data, skema dapat dibatasi, divalidasi, dan tipe data dijaga keamanannya dengan lebih mudah.

4. **Data Terhubung dan Terdesentralisasi**: Atomic Data memungkinkan penggunaan URL untuk menghubungkan data dari berbagai komputer tanpa membuat salinan. Ini sangat berguna untuk jaringan sosial terdesentralisasi atau data yang tersebar di berbagai lokasi.

5. **Auditabilitas & Versi**: Dengan Atomic Commits, setiap perubahan data disimpan sebagai transaksi yang dapat diputar ulang. Ini memungkinkan adanya riwayat perubahan lengkap dan log audit yang terperinci.

## Kekurangan Atomic Data

1. **Penggunaan Internal Saja**: Jika data hanya digunakan secara internal dan tidak perlu dibagikan kepada pihak luar, menggunakan Atomic Data justru dapat mempersulit proses karena sifatnya yang lebih kompleks dibandingkan format lain seperti JSON.

2. **Big Data**: Untuk data yang sangat besar (dalam ukuran TeraBytes), Atomic Data bukan pilihan ideal. Biaya tambahan untuk validasi skema serta kurangnya alat penyimpanan berskala besar membuatnya kurang efisien untuk skala ini.

3. **Data Video, Audio, atau 3D**: Data multimedia seperti video, audio, atau 3D sebaiknya menggunakan format biner yang dioptimalkan dan skema statis. Kelebihan Atomic Data untuk data yang terhubung dan terdesentralisasi tidak terlalu relevan dalam konteks ini, kecuali hanya untuk penyimpanan metadata.
- Bandingkan dengan aplikasi web lain yang sejenis


## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
