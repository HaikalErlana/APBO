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
**A. Admin (Agent Minuman Satria)**

Admin dalam bisnis ini berperan sebagai pemilik usaha yang mengelola minuman dari Produsen(Supplier) dan menjual kembali kepada customer(Konsumen)

**Role**
- Memasarkan produk dari produsen kepada konsumen.  
- Mengambil keputusan, merencanakan bisnis, serta mengelola operasional usaha.  
- Melakukan layanan antar barang langsung ke alamat penerima (Door to Door).

**B. Supplier (Brand Minuman)**

Supplier berperan sebagai produsen minuman yang melakukan kerja sama kepada agen untuk menjual kembali kepada usaha-usaha kecil seperti UMKM dan lainnya.

**Role**
- Melakukan pengiriman produk minuman kepada Agen untuk memasarkan dan mendistribusikan produk kepada usaha sekitar
- Menyediakan produk minuman

**C. Costumer (Konsumen)**

Customer seperti toko-toko kecil, UMKM, dan sejenisnya berperan sebagai konsumen akhir dari proses penjualan produk minuman 

**Role**
- Konsumen atau pihak akhir yang membeli produk
- Mitra bisnis yang membeli dan menjual kembali produk air minuman


### 2. Use Case Diagram
   
   ![Use Case Diagram (Agent Satria)](https://github.com/user-attachments/assets/ae5fedd6-819f-44fb-a2ce-a18280c80bc3)

  
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

### 4. Relasi (ERD)
   ![Relasi ERD](https://github.com/user-attachments/assets/e762780d-51e5-428f-a673-852d36181ba2)

### 5. Class Diagram
   
   ![ut](https://github.com/user-attachments/assets/f5e3dce9-7af9-4c15-b22c-4425c1133949)

### 6. Desain Antarmuka
   **A. WIREFRAME**
   ![Wireframe APBO](https://github.com/user-attachments/assets/eaa7d124-73fa-46a8-a6eb-1ea711dfafd2)

   **B. MOCKUP**
   ![Mockup APBO](https://github.com/user-attachments/assets/de8ee58b-81ed-4c4b-90b6-6cff87e0e1bc)

### 7. Foto Dokumentai
![WhatsApp Image 2025-05-28 at 20 49 20](https://github.com/user-attachments/assets/f1659df2-b30a-4137-a8f1-3fdb2f74a93c)
![WhatsApp Image 2025-05-28 at 20 49 20 (1)](https://github.com/user-attachments/assets/efadfc75-800c-418e-bc0c-b61fd8d1bfca)

