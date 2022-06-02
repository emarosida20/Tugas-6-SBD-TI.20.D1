# Tugas-6-SBD-TI.20.D1

**Nama : Ema Rosida**

**NIM: 312010062**

**Kelas: TI.20.D1**

**Mata Kuliah: Sistem Basis Data**

# 1. Masuk ke database nama_nim
![1 (2)](https://user-images.githubusercontent.com/101863671/171443184-c84f5e53-b9a4-4605-bc5f-c2b8d28b7e9b.png)

# 2. Lakukan proses backup dan recovery dengan sql dari database tugas sebelumnya! 

- Melakukan proses penguncian/lock table.

![2 (2)](https://user-images.githubusercontent.com/101863671/171449178-470e20e1-77ea-4cd3-a908-49c1ac038d8f.png)

- Melakukan proses backup table dengan perintah : ```SELECT * INTO OUTFILE```

![2 (3)](https://user-images.githubusercontent.com/101863671/171449549-329fa603-8294-49bb-8a06-20f08d324761.png)

- Jika proses backup berhasil maka akan muncul file backup pada direktori C:\xampp\mysql\data\nama database

![3 (2)](https://user-images.githubusercontent.com/101863671/171450093-2d3e9de4-2243-4695-977c-84ce47325e75.png)

- Data yang telah di-backup dapat dikembalikan kapan saja bila diperlukan. Sintaks SQL yang digunakan adalah ```LOAD DATA INFILE```. Perintah yang dijalankan adalah ```LOAD DATA INFILE ‘Nama_backup_file’ INTO TABLE nama_table ;```

![4 (2)](https://user-images.githubusercontent.com/101863671/171452042-a5366085-e70a-4cb0-a999-0ea2fbfbc5fa.png)

# 3. Lakukan proses backup dan recovery dengan sqldump dari database tugas sebelumnya !
- Jalankan shell atau commad-prompt dan ketikkan perintah berikut untuk memulai dump database

![5 (2)](https://user-images.githubusercontent.com/101863671/171455077-e7a73565-c94d-4c57-9a02-00c3d3c091cd.png)

- Data yang telah di-backup dapat di restrore kembali ke dalam database dengan perintah

```MySQLdump -u root -p (nama_database) <c:\xampp\mysql\bin\file_backup.sql```

![5 (3)](https://user-images.githubusercontent.com/101863671/171456003-e4a8edb7-5db0-4ed2-a14e-a08c29dbe156.png)

![6 (2)](https://user-images.githubusercontent.com/101863671/171458004-f8aaa52e-73e8-44f9-8dad-91a7757fa30e.png)

![8 (4)](https://user-images.githubusercontent.com/101863671/171458288-22e984b1-25b5-429b-874a-2380e0774445.png)

# 4. Tuliskan script cron job untuk melakukan backup otomatis setiap hari minggu jam 12 malam!
```0 0 * * 7 mysqldump -u root -p ema_312010062>ema_312010062_backup.sql```






