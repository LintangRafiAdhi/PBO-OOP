# Project OOP Berbasis MVC
## $${\color{lightblue}Link-Penjelasan-Youtube}$$
[Link Penjelasan Proses Pembuatan Program | YouTube](https://youtu.be/iv3DbRFnI6I)

<br> 

| Variable           |             Isi            |
| -------------------|----------------------------|
| **Nama**           |     Lintang Rafi Adhi      |
| **NIM**            |          312310697         |
| **Kelas**          |          TI.23.A.6         |
| **Mata Kuliah**    | Pemrograman Orientasi Objek|
| **Dosen Pengampu** |Agung Nugroho S.kom., M.Kom.|


<br> 


### <b>TUGAS 1 UAS PEMROGRAMAN ORIENTASI OBJEK</b>

![img](soal1.png)

<br> <br>


### <b>TUGAS 2 UAS PEMROGRAMAN ORIENTASI OBJEK</b>

![img](soal2.png)

<br> <br>

### KONFIGURASI DATABASE DI MYSQL

**- #mysql -h127.0.0.1 -uroot**

```
CREATE DATABASE akademik;
```
```
USE akademik;
```
```
CREATE TABLE mahasiswa (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nim VARCHAR(20) NOT NULL UNIQUE,
    nama VARCHAR(100) NOT NULL,
    jurusan VARCHAR(50) NOT NULL,
    angkatan VARCHAR(100) NOT NULL
);
```
```
CREATE TABLE nilai (
    id INT PRIMARY KEY AUTO_INCREMENT,
    mahasiswa_id INT NOT NULL,
    mata_kuliah VARCHAR(100) NOT NULL,
    semester INT NOT NULL,
    nilai CHAR(2),
    FOREIGN KEY (mahasiswa_id) REFERENCES mahasiswa(id)
    ON DELETE CASCADE
);
```

### Tampilan Awal Program Saat Dijalankan / Dirunning
![img](awal.png)
Pada saat program dijalankan / di running akan menghasilkan output seperti diatas ini
- Menampilkan Form Mahasiswa utama dengan tabel yang berisi data 4 mahasiswa
- Data yang ditampilkan: ID, NIM, Nama, Jurusan, dan Angkatan
- Memiliki field kosong di atas untuk input data baru
- Terdapat 4 tombol: Save, Delete, Clear, dan Lihat Nilai

<br> <br>


### Tampilan Ketika Penambahan Data Mahasiswa
![img](tambah.png)
berikut adalah proses penambahan mahasiswa baru dengan field yang diisi adalah bagian `NIM`, `Nama`, `Jurusan`, `Angkatan`.

<br> <br>


### Tampilan Ketika Penambahan Data Mahasiswa Berhasil
![img](berhasil.png)
Pada saat setelah mengklik tombol `Save`, muncul popup dengan pesan `"Data saved successfully!"`. Menandakan data mahasiswa baru berhasil disimpan ke database.

<br> <br>


### Tampilan Ketika Menambahkan Sebuah Data Nilai Dari Mahasiswa
![img](tn.png)
- Muncul form baru Data Nilai Mahasiswa : Rahmat Cihuy (312220676).
- Mengisi field `Mata Kuliah` `Semester` `Nilai`.

<br> <br>


### Tampilan Ketika Data Nilai Berhasil Disimpan 
![img](tnb.png)
Setelah klik Save, muncul popup `Nilai berhasil disimpan!`.

<br> <br>


### Tampilan Ketika Setelah Selesai Penambahan Data Nilai
![img](tnb.png)
- Data nilai yang baru diinput muncul di tabel nilai
- Menampilkan `ID (8)`, `Mata Kuliah (Pemrograman Web 1)`, `Semester (3)`, dan `Nilai (87)`.

<br>


Program ini menggunakan konsep form management yang baik dengan validasi data dan feedback user melalui popup messages. Interface dibuat user-friendly dengan tabel untuk menampilkan data dan form input yang jelas.
