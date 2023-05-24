TUGAS PRAKTIKUM  3
1.	Lakukan penambahan data pada tabel mahasiswa dengan mengisi kd_ds yang belum  ada pada data dosen.
2.	Hapus satu record dat pada tabel dosen yang telah dirjuk pada tabel mahasiswa.
3.	Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT.
4.	Lakukan perubahan data pada tabel dosen (kd_ds).
5.	Lakukan penghapusan data pada tabel dosen.
6.	Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL.
7.	Lakukan penghapusan data pada tabel dosen.

### 1. Lakukan penambahan data pada tabel mahasiswa dengan mengisi kd_ds yang belum  ada pada data dosen.
*Untuk melakukan penambahan data pada tabel Mahasiswa dengan mengisi kd_ds yang belum ada pada tabel Dosen, Anda dapat menggunakan pernyataan SQL INSERT INTO dan subquery untuk memeriksa keberadaan kd_ds pada tabel Dosen

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/8eb5d9cb-8515-4deb-9991-71f7ae9e73cb)

### 2. Hapus satu record data pada table dosen yang telah dirujuk pada table mahasiswa.
*Untuk menghapus satu record data pada tabel Dosen yang telah dirujuk pada tabel Mahasiswa, perhatikan bahwa penghapusan tersebut harus dilakukan dengan hati-hati karena jika kd_ds yang dihapus masih digunakan oleh Mahasiswa, hal itu akan menyebabkan masalah integritas data. Jika Anda ingin menghapus record pada tabel Dosen yang tidak memiliki referensi di tabel Mahasiswa, Anda dapat  menggunakan pernyataan SQL DELETE dengan klausa NOT IN 

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/b42baf0b-25b6-4cb6-b011-f9ba62f6dd04)

### 3.	Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT
*Untuk mengubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT pada relasi antara tabel Mahasiswa dan Dosen, Anda perlu menggunakan pernyataan ALTER TABLE dan menentukan constraint yang ingin diubah.

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/574f0afb-5d9c-414a-94d1-432fc5e823d3)

### 4.	Lakukan perubahan data pada table dosen (kd_ds)
Untuk melakukan perubahan data pada tabel Dosen (kd_ds), Anda dapat menggunakan pernyataan SQL UPDATE.

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/11d00796-a2de-4bbd-8ff0-2205f93fceda)

### 5.	Lakukan penghapusan data pada table dosen
*Untuk melakukan penghapusan data pada tabel Dosen, Anda dapat menggunakan pernyataan SQL
DELETE. Namun, penting untuk memastikan bahwa penghapusan tersebut tidak akan menyebabkan
masalah integritas data. Jika ada tabel lain yang merujuk ke kd_ds di tabel Dosen, Anda harus	
menghapus atau mengubah data tersebut terlebih dahulu sebelum menghapus data di tabel Dosen.

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/08df38b6-6945-40aa-a3da-227b359ee517)

### 6.	Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL
Untuk mengubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL pada relasi antara tabel Mahasiswa dan Dosen, Anda perlu menggunakan pernyataan ALTER TABLE dan menentukan constraint yang ingin diubah.

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/c165196c-784a-4d89-aabb-ae971a1ce2e7)

###  7.	Lakukan penghapusan data pada table dosen
*Untuk melakukan penghapusan data pada tabel Dosen, dengan mode ON UPDATE CASCADE ON
DELETE SET NULL, Anda dapat menggunakan pernyataan SQL DELETE. Namun, perhatikan bahwa
penghapusan tersebut akan mengubah nilai kd_ds di tabel Mahasiswa menjadi NULL.	

![image](https://github.com/Akramfarrasanto/Praktikum-3-Basis-Data/assets/115552876/c0e6cb2a-4d58-40f6-a8ed-5a7a7e594001)

## Evaluasi dan Pertanyaan
### Apa bedanya pengguna RESTRICT dan CASCADE ?
•	Penggunaan RESTRICT dan CASCADE adalah dua jenis aturan referential integrity (keutuhan referensial) yang dapat diterapkan pada kunci asing (foreign key) di basis data relasional. RESTRICT berarti bahwa ketika ada sebuah baris data di tabel induk (parent table) yang ingin dihapus atau diubah, maka sistem basis data akan memeriksa apakah ada baris data di tabel anak (child table) yang masih merujuk ke baris data tersebut. Jika ada, maka sistem basis data akan mencegah penghapusan atau perubahan data pada baris data di tabel induk yang berdampak pada baris data di tabel anak yang masih merujuk ke baris data tersebut. Sementara itu, CASCADE adalah sebuah baris data di tabel induk dihapus atau diubah, maka sistem basis data akan secara otomatis menghapus atau mengubah baris data di tabel anak yang merujuk ke baris data yang dihapus atau diubah tersebut.

### Berikan Kesimpulan
•	RESTRICT dan CASCADE adalah aturan refential intrgrity Yang dapat diterapkan pada kunci asing yang basis data relasional. RESTRICT mencegah penghapusan atau perubahan data pada tabel induk yang berdampak pada tabel anak yang masih merujuk ke data yang di hapus atau di ubah. Sementara CASCADE dengan secara otomatis menghapus atau mengubah data pada tabel anak yang merujuk ke data yang di apus atau di ubah pada tabel induk. Kedua aturan tersebut memiliki kelebihan dan kekurangan msing-masing dan harus dipilih secara bijak sesuai dengan kebutuhan dan konteks penggunaannya agar dapat memastikan keutuhan data didalam system basis data

