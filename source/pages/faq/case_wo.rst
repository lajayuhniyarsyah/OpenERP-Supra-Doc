Membuat SPK - Work Order (WO)
=============================

Untuk membuat SPK (Surat Perintah Kerja), berikut langkah-langkahnya:

1. Setelah login, klik tab menu Sales yang ada diatas

.. image:: /img/wo_2.png

2. Kemudian pada menu sebelah kiri, scroll ke bawah, pilih menu Work Order -> SBM Work Order

.. image:: /img/wo_4.png

3. Setelah itu akan tampil seperti dibawah ini, klik tombol Create

.. image:: /img/wo_5.png

4. Maka akan tampil form-nya. Untuk field yang berwarna biru maksudnya adalah itu harus diisi.

.. image:: /img/wo_6.png

5. Pilih Source Type-nya. Source Type adalah tipe dari SPK yang akan dibuat.

.. image:: /img/wo_7.png

6. Pilih Sale Order-nya. Sale Order adalah nomor dari SO yang sudah dibuat pada menu Sales -> Sales Orders

.. image:: /img/wo_8.png

Apabila sudah dipilih maka beberapa field akan otomatis terisi dari data yang sudah ada pada SO terpilih.

.. image:: /img/wo_9.png

7. Field Costumer digunakan untuk menentukan costumer/pelanggan yang akan dituju. Anda dapat merubahnya jika diperlukan, dengan meng-klik dropdown yang sejajar dengan label costumer. Rubah jika diperlukan.

.. image:: /img/wo-costumer.png

8. Selanjutnya adalah mengisi Work Location. Work Location adalah lokasi dimana pekerjaan itu dilakukan.

.. image:: /img/wo_10.png

9. Setelah itu, isi Internal Handler Location-nya. Internal Handler Location adalah lokasi asal dimana resource berada.

.. image:: /img/wo_11.png

10. Due Date maksudnya adalah due date pemesanan pekerjaannya. Sedangkan Order Date adalah tanggal order dari pemesanan pekerjaannya. Rubah jika diperlukan.

.. image:: /img/wo-due-n-order-date.png

11. Selanjutnya adalah Output Picking. Pada tahap ini terlihat bahwa ada dua barang yang sudah diorder dari SO.

.. image:: /img/wo_12.png

Apabila Anda ingin menghapus data yang ada, klik icon recycle. Apabila Anda ingin menambah order-an barang/material ataupun jasa, klik Add an Item, maka akan muncul tampilan form seperti dibawah ini.

.. image:: /img/wo_13.png

Seperti keterangan sebelumnya bahwa field yang berwarna biru adalah yang harus diisi.

12. Pada field Product, klik dropdown-nya, pilih product yang ingin ditambahkan. Product ini dapat berupa barang maupun jasa.

.. image:: /img/wo_14.png

14. Pada field Description, Anda dapat menambahkan keterangan tentang produk yang terpilih diatas.

.. image:: /img/wo_15.png

15. Pada field Qty, adalah berapa quantity produk yang dipesan. Sedangkan UOM adalah satuan dari produknya, dapat berupa set, ea, dan lain-lain.

.. image:: /img/wo_16.png

16. Attach a File adalah field yang digunakan untuk meng-upload dokumen yang berkaitan dengan produk terpilih. Anda dapat menambahkannya jika diperlukan.

.. image:: /img/wo_17.png

17. Pada tab Data Material, Anda dapat menambahkan item yang berkaitan dengan produk terpilih.

.. image:: /img/wo_18.png

Jika sudah semuanya, Anda dapat meng-klik Save & New untuk membuat order material produk baru atau klik Save & Close untuk kembali ke menu sebelumnya. Jika sudah maka akan tampil seperti dibawah ini.

.. image:: /img/wo_19.png

Terlihat bahwa item pada tab Output Picking bertambah.

18. Selanjutnya adalah mengisi catatan pada field Notes jika diperlukan, karena field ini tidak harus diisi.

.. image:: /img/wo_20.png

19. Selanjutnya adalah meng-klik tombol Confirm. Ini bertujuan bahwa SPK sudah dikonfirmasi oleh user.

.. image:: /img/wo_22.png

Jika sudah maka akan tampil seperti pada gambar.

.. image:: /img/wo_23.png

20. Selanjutnya adalah mengklik tombol Save untuk menyimpan SPK.

.. image:: /img/wo_24.png

Jika sudah maka akan tampil seperti gambar dibawah ini.

.. image:: /img/wo_25.png




Berikut ini ada 3 contoh kasus pada pembuatan SPK:


SPK Fabrikasi Barang
--------------------

.. image:: /img/wo_fabrikasi_barang.png

Ada beberapa hal yang harus diperhatikan dalam membuat SPK Fabrikasi Barang, yaitu:

1. Field: Source Type. Source Type digunakan untuk menentukan sumber SPK yang akan dibuat. Field ini bersifat required.

2. Field: Sale Order. Sale Order adalah nomor SO yang telah dibuat sebelumnya pada menu Sales -> Sales Orders. Perlu diperhatikan bahwa jika sudah mengisi field ini, bebepa field lainnya akan otomatis terisi, dan pastikan Output Picking untuk produknya berupa barang. Field ini bersifat required. 

3. Field: Work Location. Work Location adalah tempat dimana pekerjaan dilakukan. Pemilihan Work Location harus Work Shop. Field ini bersifat required.

4. Field: Internal Handler Location. Internal Handler Location adalah tempat resource yang akan ikut serta dalam SPK. Field ini bersifat required.




SPK Manpower
------------

Berikut hal-hal yang harus diperhatikan dalam membuat SPK Manpower, yaitu:

1. Seperti pada penjelasan sebelumnya bahwa field yang berwarna biru adalah required atau harus diisi.

.. image:: /img/wo-man-power-1.png

2. Pada contoh kasus ini, SO diambil dari nomor 00185 yang didalamnya terdapat produk Carry Roller, Frame, dan Instalasi/Pemasangan.

.. image:: /img/print-so-1.png

(Gambar Printout SO 00185 - Hal 1)

.. image:: /img/print-so-2.png

(Gambar Printout SO 00185 - Hal 2)

Produk yang digunakan untuk membuat SPK Manpower adalah yang bertanda MERAH.

3. Kembali ke form Work Order, Product Out Picking yang ditandai MERAH adalah yang harus Anda perhatikan. Produk tersebut bukan berupa barang, melainkan berupa jasa.

.. image:: /img/wo-man-power-2.png

Produk yang terdapat pada tab Output Picking tersebut berasal dari SO 00185.

4. Selanjutnya adalah klik produk Instalasi/Pemasangan untuk menambahkan detail produk. Maka akan tampil seperti dibawah ini.

.. image:: /img/wo-man-power-3.png

Pada tab Data Material, isi masing-masing fieldnya. a. Product-nya adalah MANPOWER. b. Description, pada field ini tambahkan keterangan tentang manpower pada SPK yang sedang dibuat. c. Qty, jumlah manpower. d. UoM, satuan manpower-nya adalah orang. e. Costumer Materials, jika material yang digunakan berasal dari Costumer.

Jika selesai klik Save.



SPK Site Workshop
-----------------

Berikut ini adalah cara membuat SPK untuk contoh kasuk Work Location pada Work Shop.

.. image:: /img/wo-work-location-work-shop.png

Isi semua field pada form-nya. Hal yang perlu diperhatikan adalah pada field Work Location, pilih Work Shop. Artinya lokasi tempat kerja berada di Workshop.