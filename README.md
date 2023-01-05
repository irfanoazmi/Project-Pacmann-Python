# OBJECTIVE
Pada project python ini, saya diminta oleh pacmann untuk membuat system kasir self-service menggunakan python, diharapkan system kasir yang dibuat dapat membantu siapapun yang sedang mengembangkan warung jujur yang customernya milih barang sendiri, bayar sendiri dan ambil kembaliannya sendiri.
Objective yang harus dipenuhi dari system kasir ini adalah sebagai berikut:

1. Customer dapat membuat ID transaksinya (class Transaction)
2. Customer dapat memasukan nama, jumlah dan harga barang
3. Customer dapat melakukan perubahan nama, jumlah dan harga barang
4. Customer dapat membatalkan salah satu item yang akan dibeli dan juga dapat menghapus semua pesanan dengan fitur reset transaction
5. Customer dapat melakukan pengecekan total orderan secara keseluruhan
6. Customer dapat menghitung total belanja yang akan dibeli dengan diskon yang sudah ditetapkan oleh took

# FLOWCHART
Berikut flowchart / alur system kasir online yang akan dibuat:

![flow chart](https://user-images.githubusercontent.com/119559428/210802519-2b2e6409-9995-45a2-b181-3ee2775a7c12.png)

Tahapan customer dalam menggunakan self-service cassiernya adalah sebagai berikut:
1. Customer akan memulai program dengan membuka script .py yang telah disediakan.
2. Customer akan memasukan ID atau nama customer yang digunakan sebagai ID transaksi.
3. Selanjutnya customer akan memasukan nama item, jumlah dan harganya.
4. customer akan mengecek apakah data yang dimasukan sudah benar atau tidak, jika tidak benar customer dapat melakukan reset dan datanya akan terhapus semua, atau memodifikasi individual antara nama item, jumlah atau harganya.
5. jika sudah benar data yang di input, customer akan melakukan pengecekan total harga, apakah mendapatkan diskon atau tidak.
6. customer membayar belanjaannya
7. program selesai.


# DESKRIPSI TASK
1. Modul transaksi_belanja.py berisikan class Transaction dengan method sebagai berikut :
    - menu() untuk menampilkan pilihan ke method lain
    - add_item() untuk memasukan nama, jumlah dan harga item ke dalam dictionary
    - update_item_name() untuk mengubah nama item yang terdapat dalam dictionary
    - update_item_qty() untuk mengubah jumlah item yang terdapat dalam dictionary
    - update_item_price() untuk mengubah harga item yang terdapat dalam dictionary
    - delete_item() untuk menghapus item spesifik beserta jumlah dan harganya dari dictionary
    - reset_transaction() untuk menghapus semua item dari dictionary
    - check_order() untuk memastikan kelengkapan data pada dictionary belanja, dan menampilkan summary order
    - total_price() untuk menampilkan diskon yang didapat dan total harga setelah diskon
    
2. Modul main_belanja.py merupakan tampilan awal self-service cassier yang terhubung ke modul transaksi_belanja.py

# CARA MENGGUNAKAN PROGRAM
1. Download semua file/module Python ke dalam satu direktori lokal.
2. Anda cukup menjalankan main_belanja.py saja, karena sudah transaksi_belanja.py sudah terimport di module tersebut. Perhatikan gambar dibawah ini :
![simpan kedua file dalam satu directory yang sama](https://user-images.githubusercontent.com/119559428/210802861-67f5a83f-8b32-4302-b648-ade75ceb8455.png)

# Hasil Test Case
1. **TEST 1 :** Buka file main_belanja.py, maka akan muncul tampilan menu utama program. user hanya perlu memasukan nama nya sebagai ID transaksi,

![tampilan halaman utama program, masukan ID atau nama user](https://user-images.githubusercontent.com/119559428/210803265-976c3440-f4ff-40b2-adae-19d51dafef8a.png)

![Setelah memasukan nama](https://user-images.githubusercontent.com/119559428/210803443-127689d0-21be-4f0f-b6a8-822bb49e036f.png)
***

- Pilih Y jika ingin melanjutkan menggunakan program dan N jika ingin menghentikannya.

- Setelah pilih Y, maka user akan diarahkan ke menu utama program. Pada menu ini user dapat memilih action apa yang ingin dilakukan selanjutnya. Tabel belanjaan juga ditampilkan sebagai summary dan mempermudah user untuk memilih action apa yang ingin dilakukan.
Namun pada saat pertama dibuka, tabel belanja masih kosong.

![tampilan menu utama](https://user-images.githubusercontent.com/119559428/210804144-dbe4b62c-d161-4e87-9028-da9e201153ac.png)
***

2. **TEST 2 :** Pilih menu 1 untuk menambahkan item belanja / add item. maka akan muncul perintah untuk Memasukan nama, jumlah dan harga item.

![memasukan input secara manual](https://user-images.githubusercontent.com/119559428/210804727-e378f7fe-c35b-4a75-a470-13e4b037919e.png)
***

- setelah itu maka akan terupdate automatis di tabel belanjaan user.

![setelah menambahkan 1 item](https://user-images.githubusercontent.com/119559428/210804839-242a9d99-669e-48af-adc6-3e97a2dfb52f.png)
***

3. **TEST 3 :** Pilih menu 2 untuk mengupdate / modifikasi item belanja, terdapat pilihan menu yang disediakan untuk user. 

![menu pilihan update item](https://user-images.githubusercontent.com/119559428/210805697-57c4ac90-ab8c-454d-9efb-d54c61a3c27b.png)
***

- Pilih menu 1 untuk **update nama** belanjaan, maka akan diarahkan untuk memasukan nama yang ingin diganti dan nama barunya.

![input nama sebelum d
an sesudah](https://user-images.githubusercontent.com/119559428/210806029-338a45cf-95a5-43f0-bfe5-f19ef592c89a.png)
***

setelah itu klik **ENTER**, maka nama item berhasil di update.

![setelah diganti namanya](https://user-images.githubusercontent.com/119559428/210806134-8335d86b-e758-4dd5-8105-4f77a85d53b0.png)
***

- Pilih menu 2 untuk **update jumlah** item belanjaan, dan diarahkan untuk memasukan nama item yang akan diganti jumlahnya.

![input nama dan jumah update](https://user-images.githubusercontent.com/119559428/210807214-830040a6-a075-4fa6-9cdd-6eb73dc8af4a.png)
***

setelah itu klik **ENTER**, maka nama item berhasil di update.

![tampilan setelah update jumlah](https://user-images.githubusercontent.com/119559428/210807310-9834e060-c9be-4b35-b4fd-1807968435da.png)
***

- Pilih menu 3 untuk **update harga** item belanjaan, dan diarahkan untuk memasukan nama item yang ingin diganti harganya.

![input nama dan harga update](https://user-images.githubusercontent.com/119559428/210808159-d06e38fa-1ac3-4ec2-9b84-46b8670254d4.png)
***

setelah itu klik **ENTER**, maka nama item berhasil di update.

![tampilan setelah update harga](https://user-images.githubusercontent.com/119559428/210808348-8c4c57d4-3d35-436e-b993-10cb60c6d2fa.png)
***

- Pilih menu 4 untuk **delete item** belanjaan, dan diarahkan untuk memasukan nama item yang ingin di hapus dari tabel.

![input item yang akan di delete](https://user-images.githubusercontent.com/119559428/210815337-f45d02ea-fd3d-4c6e-8a31-0b9aee50442a.png)
***

setelah itu klik **ENTER**, maka nama item berhasil di hapus.

![tampilan setelah delete item](https://user-images.githubusercontent.com/119559428/210815442-b02083cc-47df-46bc-ae7a-54dec72fe360.png)
***

4. **TEST 4 :** Pilih menu 3 untuk reset transaction, maka seluruh item yang terdapat pada tabel akan terhapus.

![halaman utama reset transaction](https://user-images.githubusercontent.com/119559428/210817502-ccf98a25-8d2e-467e-81be-08c1bcd7e6ca.png)
***

5. **TEST 5 :** Pilih menu 4 untuk check order, maka akan dilakukan pengcekan apakah input pada tabel sudah sesuai atau tidak.

![tampilan awal check order](https://user-images.githubusercontent.com/119559428/210817900-6507999c-0c85-40a0-b67f-ee20d1a47a55.png)
***

6. **TEST 6 :** Pilih menu 5 untuk menampilkan total pembayaran dan termasuk perhitungan diskon yang didapatkan.

![halaman awal total belanjaan](https://user-images.githubusercontent.com/119559428/210818304-4e037348-1fb7-409e-8962-645a42afe1f4.png)
***
