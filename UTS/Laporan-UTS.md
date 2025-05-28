# UTS APBO A KELOMPOK 7

Repositori ini berisi hasil Ujian Tengah Semester (UTS) mata kuliah **Analisis Pemrograman Berbasis Objek (APBO)** - Kelas A

## Dosen Pengampu
Adi Wahyu Pribadi, S.Si., M.Kom

## Anggota Kelompok 3

| No | Nama Anggota            | NPM         |
|----|-------------------------|-------------|
| 1  | Souma Ramdhani Setiawan | 4523210106  |
| 2  | Muhammad Haikal Erlana  | 4523210074  |
| 3  | Lean Ferdiansyah        | 4523210059  |
| 4  | Mohammad Fadlan         | 4523210065  |
| 5  | Muhammad Rashaqa        | 4523210078  |

## Agent Minuman Satria

### 1. Aktor/Role  
**A. Admin**

Admin dalam bisnis ini berperan sebagai pemilik usaha yang mengelola minuman dari Produsen(Supplier) dan menjual kembali kepada customer(Konsumen)
**Role**
- Memasarkan produk dari produsen kepada konsumen.  
- Mengambil keputusan, merencanakan bisnis, serta mengelola operasional usaha.  
- Melakukan layanan antar barang langsung ke alamat penerima (Door to Door).

**B. Supplier**

Supplier berperan sebagai produsen minuman yang melakukan kerja sama kepada agen untuk menjual kembali kepada usaha-usaha kecil seperti UMKM dan lainnya.
**Role**
- Melakukan pengiriman produk minuman kepada Agen untuk memasarkan dan mendistribusikan produk kepada usaha sekitar
- Menyediakan produk minuman

**C. Costumer**

Customer seperti toko-toko kecil, UMKM, dan sejenisnya berperan sebagai konsumen akhir dari proses penjualan produk minuman 
**Role**
- Konsumen atau pihak akhir yang membeli produk
- Mitra bisnis yang membeli dan menjual kembali produk air minuman


### 2. Use Case Diagram
   
   ![usecase agen satria drawio (1)](https://github.com/user-attachments/assets/ebb0c4c2-3edc-40fa-b6fd-944d4ba3daf4)
  
### 3. Entitas Utama
   **A. Admin**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_admin     | INT(PK)            | ID unik untuk admin   |
   | nama_admin   | Varchar(100)       | Nama lengkap admin    |
   | username     | Varchar(50)        | Username login admin  |
   | password     | Varchar(50)        | Password login admin  |

   **B. Pelanggan**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_pelanggan    | INT(PK)            | Primary key, ID unik untuk pelanggan   |
   | nama_pelanggan   | Varchar(100)       | Nama pemilik toko/UMKM    |
   | jenis_pelanggan     | Varchar(50)        | UMKM / Toko  |
   | alamat     | Varchar(200)        | Lokasi pelanggan  |
   | no_hp     | Varchar(20)        | Nomor telepon |
   | metode_pembayaran     | Varchar(50)        | Cash / Transfer  |
  
   **C. Supplier**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_supplier    | INT(PK)            | Primary key, ID unik untuk supplier   |
   | nama_supplier  | Varchar(100)       | Nama perusahaan brand minuman    |
   | jenis_produk    | Varchar(50)        | Jenis produk yang dikirim  |
   | alamat_supplier     | Varchar(200)        | Alamat kantor supplier  |
   | no_kontak     | Varchar(20)        | Kontak person atau CS  |
   
   **D. Produk**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_produk    | INT(PK)            | Primary key, ID unik untuk produk   |
   | nama_produk   | Varchar(100)       | Nama minuman    |
   | jenis_produk     | Varchar(50)        | Contoh: Air Minum, Soda, Kopi  |
   | harga     | INT        | Harga satuan produk  |
   | stok     | INT        | Jumlah produk yang tersedia |
   | satuan     | Varchar(20)        | Contoh: botol, dus, pcs  |
   | id_admin     | INT(FK)        | Admin yang mengelola produk  |
   | id_supplier   | INT(FK)       | Supplier penyedia produk  |
   
   **E. Transaksi**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_transaksi   | INT(PK)            | Primary key, ID unik transaksi   |
   | tanggal  | Date       | Tanggal transaksi dilakukan   |
   | id_pelanggan     | INT(FK)        | Relasi ke entitas pelanggan  |
   | id_admin     | INT(FK)        | Admin/Kasir yang melayani transaksi |
   | total_bayar     | INT        | Total Pembayaran |
   | metode_pembayaran     | Varchar(50)        | Cara Pembayaran(Cash/Tf)  |
   | status     | ENUM(‘selesai’,’pending’)       | Status transaksi apakah sudah selesai atau masih pending  |

   **F. Detail Transaksi**
   | Atribut | Tipe Data            | Keterangan         |
   |----|-------------------------  |-------------|
   | id_detail  | INT(PK)            | ID unik detail transaksi   |
   | id_transaksi   | INT(FK)       | ID transaksi utama    |
   | id_produk     | INT(FK)        | ID produk yang dibeli  |
   | jumlah     | INT        | Jumlah item yang dibeli  |
   | harga_satuan     | INT        | Harga satuan produk saat transaksi |

### 4. Relasi
   ![Relasi Benar](https://github.com/user-attachments/assets/653aea6f-c23f-4e71-991e-af9b9545257a)


### 5. Class Diagram
   
   ![Class Diagram](https://github.com/user-attachments/assets/cea3ebc6-9b32-4061-bbdf-ef5a34c7cabd)

### 6. Desain Antarmuka
   **A. WIREFRAME**
   ![Wireframe APBO](https://github.com/user-attachments/assets/eaa7d124-73fa-46a8-a6eb-1ea711dfafd2)

   **B. MOCKUP**
   ![Mockup APBO](https://github.com/user-attachments/assets/de8ee58b-81ed-4c4b-90b6-6cff87e0e1bc)

### 7. Laporan
