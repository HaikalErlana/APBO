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


### 1. Flowchart
![Flowchart Agen Satria](https://github.com/user-attachments/assets/ea3006d6-1063-48a0-8612-d2c0f6098f17)

### 2. Aktor/Role  
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


### 3. Use Case Diagram
   
   ![Use Case Diagram (Agent Satria)](https://github.com/user-attachments/assets/ae5fedd6-819f-44fb-a2ce-a18280c80bc3)

  
### 4. Entitas Utama
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

### 5. Relasi (ERD)
   ![ERD Agent Satria](https://github.com/user-attachments/assets/4a92dd58-ccd3-4459-9d35-ec13d6458088)

### 6. Class Diagram
   
   ![Class Diagram (Agent Satria)](https://github.com/user-attachments/assets/475385fc-49b5-4e44-ae70-9be2fcf24f06)

### 7. Sequence Diagram
![Editor _ Mermaid Chart-2025-06-22-125111](https://github.com/user-attachments/assets/e21f6182-a4f2-4570-89dd-dfc4bcc768e4)

### 8. Activity Diagram
![activity](https://github.com/user-attachments/assets/3365e3a6-a507-4c75-a07a-7ed050094cfd)



### 9. Desain Antarmuka 
   **A. WIREFRAME**
   **1. USER DASHBOARD**
   Register Page
   ![Register](https://github.com/user-attachments/assets/7a5661ea-5371-4fa9-9345-7e9ac943deea)
   Login Page
   ![Login](https://github.com/user-attachments/assets/8f68c8bd-db61-42e7-9e69-5352d8bdcc84)
   Lupa Password Page
   ![Lupa Password](https://github.com/user-attachments/assets/bd52971b-7e28-4882-a3e0-61eafd73530e)

   Beranda
   ![Beranda-Daftar](https://github.com/user-attachments/assets/9e9954d3-2f89-4256-9d3d-ab9be3a1572c)
   Produk
   ![Produk](https://github.com/user-attachments/assets/bbf14776-7a1f-4854-89d7-9ee47d290898)
   Tentang Kami
   ![Tentang Kami](https://github.com/user-attachments/assets/7ca73965-7a95-4953-80d2-745278470913)
   
   **2. ADMIN DASHBOARD**
   Dashboard
   ![image](https://github.com/user-attachments/assets/8eb18201-83db-46f7-a0cd-f175e795ca2a)
   Register Page
   ![Register-admin](https://github.com/user-attachments/assets/53f03f8c-64b2-4a6c-b05e-42ac91226a0b)
   Login Page
   ![Login-admin](https://github.com/user-attachments/assets/ea1b727a-a86c-414c-a15e-50066ec590a5)
   Wrongpass Page
   ![WrongPass-admin](https://github.com/user-attachments/assets/2d5755ba-b893-47b7-96ae-56b51c953d8d)
   
   Dashboard utama
   ![image](https://github.com/user-attachments/assets/f8b3aa2b-168a-4dd8-8e61-64295275cc44)
   Produk
   ![image](https://github.com/user-attachments/assets/e0864204-6007-4eb7-92a3-9bf5477f528d)
   Pesanan
   ![image](https://github.com/user-attachments/assets/1c382441-3a18-481b-b31a-8b8394f6d1ed)
   Pelanggan
   ![image](https://github.com/user-attachments/assets/71bd9f9c-9ff9-4371-9a73-0c6ebf9ca78f)
   Laporan
   ![image](https://github.com/user-attachments/assets/9a41602f-643a-45c9-8f99-00b40571e1a5)

### 10. Foto Dokumentai
![WhatsApp Image 2025-05-28 at 20 49 20](https://github.com/user-attachments/assets/f1659df2-b30a-4137-a8f1-3fdb2f74a93c)
![WhatsApp Image 2025-05-28 at 20 49 20 (1)](https://github.com/user-attachments/assets/efadfc75-800c-418e-bc0c-b61fd8d1bfca)
