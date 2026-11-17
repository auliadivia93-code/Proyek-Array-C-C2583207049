# UTS-ALGORITMA-PEMROGRAMAN-DASAR_DIVIA-AULIA
# Sistem Monitoring Stok dan Penjualan Kantin Kampus

**Mata Kuliah:** Algoritma dan Pemrograman Lanjutan  
**Program Studi:** Pendidikan Teknologi Informasi (PTI)  
**Fakultas Keguruan dan Ilmu Pendidikan, Universitas Muhammadiyah Tasikmalaya** 

---

## Identitas Mahasiswa
- **Nama Lengkap:** Divia Aulia
- **NIM:** C2583207049
- **Kelas:** PTI-3A
- **Mata Kuliah:** Algoritma dan Pemrograman Lanjutan
- **Nama Proyek:** Sistem Monitoring Stok dan Penjualan Kantin Kampus

---

## Deskripsi Singkat
**Sistem Monitoring Stok dan Penjualan Kantin Kampus** adalah aplikasi berbasis console (terminal) yang dibangun menggunakan bahasa pemrograman C untuk menggantikan pencatatan stok dan transaksi manual di lingkungan kantin kampus. Aplikasi ini membantu pengelola kantin memantau ketersediaan barang secara *real-time*, memproses transaksi pembelian beberapa jenis produk sekaligus dengan perhitungan otomatis, mendeteksi produk dengan stok menipis, serta menyajikan laporan pendapatan dan produk terlaris. Seluruh pengelolaan data selama program berjalan memanfaatkan struktur data **Array** (array satu dimensi dan array karakter dua dimensi) tanpa menggunakan database eksternal, dengan kapasitas maksimal 50 jenis produk.

---

## Daftar Fitur
1. **Lihat Daftar Produk:** Menampilkan nomor, nama, harga satuan, sisa stok, dan jumlah terjual seluruh produk.
2. **Tambah Produk:** Menambahkan data produk baru ke dalam array (kapasitas maksimal 50 produk).
3. **Ubah Produk:** Memperbarui harga dan jumlah stok produk yang sudah terdaftar.
4. **Transaksi Penjualan:** Memproses pembelian beberapa jenis produk dalam satu transaksi, menghitung subtotal & total pembayaran, serta mengurangi stok dan menambah jumlah terjual secara otomatis.
5. **Tambah Stok:** Menambahkan jumlah stok pada produk tertentu.
6. **Cari Produk:** Mencari data produk berdasarkan kata kunci nama produk.
7. **Urutkan Produk:** Mengurutkan daftar produk berdasarkan harga termurah (*ascending*) dan jumlah terjual terbanyak (*descending*).
8. **Laporan Penjualan:** Menghitung dan menampilkan jumlah terjual per produk, total unit terjual, total pendapatan kantin, serta produk paling laris.
9. **Cek Stok Menipis:** Menampilkan peringatan daftar produk yang memiliki sisa stok kurang dari 5 unit.

---

## Penjelasan Penggunaan Array
Program menggunakan struktur data array sebagai media penyimpanan utama selama program dijalankan:
- `char namaProduk[50][50];` — **Array karakter dua dimensi** untuk menyimpan maksimal 50 nama produk dengan panjang hingga 49 karakter per nama.
- `int hargaProduk[50];` — **Array satu dimensi** untuk menyimpan harga satuan setiap produk berdasarkan indeksnya.
- `int stokProduk[50];` — **Array satu dimensi** untuk menyimpan jumlah ketersediaan stok setiap produk.
- `int terjualProduk[50];` — **Array satu dimensi** untuk mencatat total unit yang telah terjual pada setiap produk.

---

## Petunjuk Kompilasi dan Menjalankan Program

Pastikan compiler C (seperti GCC / MinGW) sudah terpasang pada perangkat, lalu jalankan perintah berikut melalui terminal/CMD:

```bash
# 1. Kompilasi kode sumber
gcc main.c -o kantin

# 2. Jalankan program (Windows)
kantin.exe

# 3. Jalankan program (Linux/macOS)
./kantin
```

---

## Dokumentasi Pengujian Skenario

### 1. Skenario 1: Tambah Produk Baru
Menambahkan produk baru melalui menu 2 dan memastikan produk langsung muncul pada daftar produk.
<img width="953" height="1016" alt="1" src="https://github.com/user-attachments/assets/40d7560d-58ac-4200-9cd4-66d995b278d2" />


### 2. Skenario 2: Transaksi Penjualan Multi-Item
Melakukan pembelian beberapa jenis produk sekaligus melalui menu 4 dengan perhitungan subtotal dan total pembayaran yang tepat.
<img width="951" height="1015" alt="2" src="https://github.com/user-attachments/assets/463ea094-72cf-4cd5-8a1d-6d7027e7bb81" />


### 3. Skenario 3: Pembaruan Stok dan Jumlah Terjual
Mengecek daftar produk setelah transaksi selesai untuk memastikan stok otomatis berkurang dan jumlah terjual bertambah.
<img width="942" height="1012" alt="3" src="https://github.com/user-attachments/assets/d3edc6df-6990-4c5f-899a-c41aea8515c4" />

### 4. Skenario 4: Penanganan Stok Tidak Cukup
Mencoba melakukan pembelian melebihi sisa stok yang tersedia; sistem menolak transaksi dan stok tetap tidak berubah.
<img width="950" height="1011" alt="4" src="https://github.com/user-attachments/assets/1efb2c3a-0bdd-4952-99a5-96b90e556177" />


### 5. Skenario 5: Laporan Penjualan dan Produk Terlaris
Menampilkan laporan penjualan melalui menu 8 untuk memverifikasi total unit terjual, total pendapatan, dan produk terlaris.
<img width="936" height="1006" alt="5" src="https://github.com/user-attachments/assets/e4ec40be-4862-4a57-9532-b64ea9f56791" />

### 6. Skenario 6: Pengurutan Produk
Mengurutkan produk berdasarkan harga dari termurah dan jumlah terjual dari terbanyak melalui menu 7.
<img width="947" height="1015" alt="6" src="https://github.com/user-attachments/assets/d2b2bb76-5eea-4e4f-b4ff-9da69426831a" />


### 7. Skenario 7: Pencarian Produk dan Cek Stok Menipis (< 5)
Mencari produk berdasarkan nama (menu 6) serta menampilkan peringatan produk dengan stok kurang dari 5 (menu 9).
<img width="943" height="1010" alt="Screenshot 2026-11-17 203241" src="https://github.com/user-attachments/assets/fe79f447-79ee-4eb0-96b7-e6f1d68191bb" />
