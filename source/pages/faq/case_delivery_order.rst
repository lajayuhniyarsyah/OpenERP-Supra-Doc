.. _faq_do:
Mempersiapkan dan Mengirim Permintaan Barang Pesanan
====================================================

.. _faq_do_op_create:

Membuat Doc Order Preparation
-----------------------------


Dalam membuat doc order preparation, yang harus diperhatikan adalah status dari sales order yang dapat ditarik atau di proses menjadi order preparation, Yaitu status sales Order 

**WIN, Sale Order, Sale To Invoice**

setelah memastikan sales order dapat di proses maka, order preaprarion dapat di buat

Step By Step
^^^^^^^^^^^^

Click Button Create 


.. image:: /img/op-create.png


Setelah itu cari sales order yang ingin dibuatkan order preparation, 

.. image:: /img/op-select-so.png


Catatan : Sales Order yang muncul atau yang dapat di cari yang sudah dijelaskan sebelumnya 


.. image:: /img/op-data.png


- Setealah memilih sales order, data dari sales order akan terisi secara otomatis pada doc order preparation beserta dengan detail product nya 

- Product yang ditampilkan adalah product yang ada di sale order material line
- Product yang di tampilkan di order line adalah product yang masih dapat di proses secara Qty
- User juga dapat menyesuaikan barang dan Qty apa saja yang akan disiapkan dalam doc order preparation tersebut


- Pilih Item yang akan di sesuaikan, 

.. image:: /img/op-edit-line.png

- Setelah di pilih maka akan muncul form detail item 


.. image:: /img/op-detail-line.png


Pada gambar di atas user dapat menyesuaikan sesuai dengan kebutuhan 

1. Qty Product (Berfungsi untuk mendefinisikan Qty Product yang akan disiapkan, Tidak boleh lebih besar dari Qty yang ada)
2. Description (Jika Product ingin diberikan Description Tambahan)
3. Detail Product (Jika Product ingin mendetailkan product)
4. Product Batch (Jika Produt merupakan barang batch maka, batch product harus di pilih atau di definisikan)
5. Sale Item (Jika barang yang dibuat di OP bukan barang yang ada di SO, maka harus di definiskan Sale Item nya)
6. Material Ref (Jika barang yang dibuat di OP bukan barang yang ada di SO Material, maka harus di definiskan Material Ref nya)


.. image:: /img/op-edit-detail-product.png


Dari kasus di atas, adanya penyesuaian Qty, Desc, & Detail Product 


.. image:: /img/op-detail-hasil-edit.png



Product yang tidak dibutuhkan juga dapat di hapus dari list order line

- Caranya click button hapus pada product

.. image:: /img/op-delete-line.png

- Jika semua detail order line sudah di sesuikan dengan kebutuhan, maka user dapat melakukan proses SAVE 
- Setelah SAVE maka, No Doc Order Preparation akan terbentuk
- Click Button Print untuk melihat hasil print out


.. image:: /img/print-out-op.png


.. _faq_do_op_batch:

Membuat Order Preparation Untuk Product Batch / Potongan
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click Button Create 


.. image:: /img/op-create.png


- Cari sales order yang ingin dibuatkan order preparation dimana di dalamnya ada product bacth, 
- Product Batch biasanya memiliki identitas Part Number **PS**


.. image:: /img/op-so-batch.png

- Sales Order yang dipilih akan menampilkan data sales order beserta dengan material Line nya


.. image:: /img/op-line-batch.png


- Di dalam contoh di atas, ada satu product yang merupakan product batch
- User harus memilih atau mendefinisikan batch apa saja yang ingin digunakan dalam memenuhi kebutuhan product
- Cara memilih product batch dalam 
- Click Product (Lihat Pada Gambar)

.. image:: /img/pilih-product-batch.png

- Maka akan tampil form detail product order line

.. image:: /img/tambah-product-batch.png

- Point No 1, (Jumlah total Qty product Batch) 
- Click Add an Item Pilih Serial Number yang akan digunakan untuk memebuhi kebutuhan Total Product Batch
- Input Qty yang di inginkan dari Serial Number yang telah dipilih Jumlah
- Point No 1 & 2 jika ditambah harus sama dengan jumlah Total Qty Setelah
- sesuai Qty Pada point No 1, dengan jumlah Qty yang dari Qty product batch
- Click SAVE


.. image:: /img/done-op-batch.png


- Setelah semua selesai, user dapat melakukan print out 
- Click button print 
- Hasil Print Out

.. image:: /img/print-out-product-batch.png

.. _faq_do_op_other_item:

Order Preparation dengan supply barang berbeda dari permintaan PO
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Dalam kasus ini, barang yang diminta di Sales Order atau PO Customer tidak sama dengan barang yang akan disiapkan atau di kirim
- Lihat Contoh Sales Order atau PO di bawah ini 

.. image:: /img/so-contoh-op.png

- Dalam gambar di atas untuk Item No. 2, barang yang akan dikirim atau yang akan disiapkan bukanlah barang yang sesuai dengan item No.2, maka harus ada penyesuaian di Order Preparation nya
- Click Product yang ingin di sesuaikan 

.. image:: /img/pilih-product-op.png

- Maka akan tampil form detail dari order line 

.. image:: /img/op-detail-barang-supply.png

- Pada point No.1, User dapat memilih product sesuai dengan kebutuhan untuk pengganti/supply product yang telah di definisikan di sales order atau PO Customer 
- Pada Point No.2 User dapat menginput nilai Qty sesuai dengan kebutuhan pengganti/supply product yang dibutuhkan 
- Pada Point No.3 ini User harus mendefinisikan secara jelas product apa yang di ganti untuk mensupply product pada point No.1 
- Pada Point No.4 ini User harus lebih mendefinisikan secara mendetail product apa yang di ganti untuk mensupply product pada point No.1, untuk point No.4 merupakan detail product yang memiliki material line lebih dari 1


.. image:: /img/op-product-supply.png


- Dari hasil proses penyesuaian product pengganti/supply, maka akan mendapatkan hasil print out sebagai berikut 

.. image:: /img/print-out-op-supply.png


.. _faq_do_dn_create:

Membuat Dokumen Surat Jalan / Delivery Note (DN)
------------------------------------------------

Untuk membuat document surat Jalan user harus mengisi form Delivery Note seperti yang sudah di jelaskan pada :ref:`pages_dn_form`.


Postpone Pengiriman / Menahan Pengiriman
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Mengirim Surat Jalan Postpone
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


Re Packing Barang
^^^^^^^^^^^^^^^^^


Retur Barang
^^^^^^^^^^^^