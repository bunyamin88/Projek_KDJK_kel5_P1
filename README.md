# Projek_KDJK_kel5_P1

# Aplikasi Web "Atomic Server"

## Sekilas Tentang

Atomic Data merupakan spesifikasi modular yang dirancang untuk berbagi informasi di web. Sebagai spesifikasi modular, pengguna dapat memilih bagian yang ingin digunakan dan mengabaikan bagian lainnya. Namun, Atomic Data Core merupakan bagian yang wajib digunakan, karena semua bagian lain bergantung pada inti ini.

Atomic Data Core memungkinkan penyampaian berbagai jenis informasi, termasuk data pribadi, kosakata, metadata, dokumen, file, dan sebagainya. Sistem ini dirancang agar mudah diserialisasikan ke dalam format JSON maupun format data terhubung (linked data). Sebagai model data yang bertipe, setiap nilai dalam Atomic Data harus divalidasi berdasarkan tipe datanya, untuk memastikan kesesuaian dan keakuratan data yang digunakan.


## Instalasi

instal docker beserta dpcker compose
```
apt-get update
docker-compose
docker
```
buat file docker-compose.yml
```
nano docker-compose.yml
```
```
version: '3.8'

services:
  alpha:
    image: joepmeneer/atomic-server
    container_name: alpha
    hostname: alpha
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - atomic-storage:/atomic-storage
    restart: unless-stopped

volumes:
  atomic-storage:
```

jalankan docker compose pada directory yang sama dengan file

```
docker-compose up -d
```
kemudian kunjungi domain/IP web 
	


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
1. Tampilan utama Web
   ![Halaman utama](https://github.com/bunyamin88/Projek_KDJK_kel5_P1/blob/main/Screenshot%202024-10-10%20140835.png)

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

## Perbandingan Atomic Data dengan Aplikasi Web Sejenis

### 1. **Atomic Data vs JSON-LD**

- **Kelebihan Atomic Data:**
  - **Skema Fleksibel**: Atomic Data memungkinkan penambahan properti apapun pada sumber daya, yang membuatnya lebih dinamis dalam menangani berbagai jenis data.
  - **Validasi Tipe Data**: Atomic Data menggunakan tipe data yang terstruktur dengan baik, sehingga setiap nilai harus divalidasi berdasarkan tipe datanya, memberikan keamanan yang lebih tinggi.
  - **Auditabilitas dan Versi**: Atomic Data mendukung Atomic Commits, yang memungkinkan penyimpanan setiap perubahan sebagai transaksi, memberikan kemampuan audit dan riwayat perubahan yang terperinci.

- **Kelebihan JSON-LD:**
  - **Kompatibilitas**: JSON-LD lebih populer dan didukung oleh berbagai platform seperti Google dan aplikasi web yang membutuhkan data terstruktur untuk SEO.
  - **Kemudahan Penggunaan**: JSON-LD lebih mudah digunakan dan diterapkan karena strukturnya yang lebih sederhana dan langsung dapat diintegrasikan dengan JSON biasa.
  - **Kinerja**: JSON-LD lebih ringan karena tidak memerlukan validasi tipe yang ketat seperti Atomic Data, sehingga lebih cepat dalam memproses data yang sederhana.

### 2. **Atomic Data vs RDF (Resource Description Framework)**

- **Kelebihan Atomic Data:**
  - **Kemudahan Implementasi**: Atomic Data lebih mudah diimplementasikan dibandingkan RDF, karena strukturnya lebih modular dan sederhana.
  - **Penggunaan URL untuk Dokumentasi**: Atomic Data menggunakan URL untuk mendokumentasikan properti, menjadikan data lebih mudah dimengerti tanpa memerlukan dokumentasi eksternal tambahan.
  - **Fleksibilitas**: Atomic Data memberikan fleksibilitas yang lebih tinggi dalam menentukan skema dan properti yang dapat digunakan oleh berbagai sumber data.

- **Kelebihan RDF:**
  - **Standar Terbuka**: RDF telah menjadi standar untuk data terstruktur yang terhubung di web, dengan dukungan dari berbagai organisasi dan platform.
  - **Skalabilitas untuk Dataset Besar**: RDF lebih cocok untuk skala besar, seperti Big Data dan dataset terdistribusi yang besar, karena memiliki alat-alat yang lebih matang untuk pengelolaan skala besar.
  - **Integrasi Semantik**: RDF mendukung integrasi semantik yang lebih baik, memungkinkan data dari berbagai sumber dapat dihubungkan dan dianalisis secara lebih mendalam.

### 3. **Atomic Data vs GraphQL**

- **Kelebihan Atomic Data:**
  - **Auditabilitas & Versi**: Atomic Data menyediakan fitur versioning yang kuat dengan Atomic Commits, memungkinkan setiap perubahan disimpan sebagai transaksi yang dapat diaudit.
  - **Data Terhubung dan Terdesentralisasi**: Dengan menggunakan URL, Atomic Data memudahkan untuk menghubungkan dataset yang tersebar di berbagai sumber tanpa membuat duplikasi data.

- **Kelebihan GraphQL:**
  - **Kontrol Pengguna atas Data**: GraphQL memungkinkan klien menentukan secara spesifik data apa yang mereka inginkan dari server, mengurangi pengambilan data yang berlebihan dan meningkatkan efisiensi.
  - **Komunitas dan Ekosistem yang Lebih Besar**: GraphQL memiliki komunitas pengembang yang lebih luas dan berbagai alat bantu untuk mempermudah pengembangan API.
  - **Kinerja**: GraphQL lebih cepat dalam menangani query data yang kompleks karena hanya memerlukan pengambilan data yang diminta, tanpa memvalidasi tipe atau mengikuti skema ketat seperti Atomic Data.

## Kesimpulan

Atomic Data menawarkan fleksibilitas tinggi dalam pengelolaan data terstruktur dengan skema yang fleksibel, validasi tipe yang ketat, serta kemampuan audit dan versioning yang baik. Namun, untuk kasus penggunaan tertentu seperti skala besar, data internal, atau data multimedia, aplikasi lain seperti RDF, JSON-LD, dan GraphQL mungkin lebih tepat digunakan. Atomic Data unggul dalam kasus di mana interoperabilitas, auditabilitas, dan konektivitas data terdesentralisasi sangat dibutuhkan.


## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
