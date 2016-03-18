Handing Penawaran dan Sale Order
================================


Membuat Penawaran (RFQ)
-----------------------

Untuk membuat penawaran terhadap produk dan jasa terdapat langkah-langkah yang harus dilakukan, dimana pembuatan penawaran dilakukan melalui ERP pada modul menu RFQ. Berikut merupakan tahap-tahap pembuatan penawaran :

- Masuk pada OpenERP dengan melakukan login telebih dahulu, jika login sukses maka akan masuk pada tampilan utama dari OpenERP

.. image:: /img/mp-tampilanutama.png

- Masuk pada menu **Sales**, pada bagian sidebar pilih modul **RFQ** yang terdapat pada kategori **Sales**. berikut merupakan tampilan dan isi dari modul RFQ.

.. image:: /img/mp-masukrfq.png

- Pada modul RFQ berisi list penawaran penjualan ke Customer, Untuk membuat penawaran penjualan baru tekan tombol **Create** dan masuk pada tampilan form **Quotation**  

.. image:: /img/formquotation.png 

- Form **Quotation** berfungsi untuk melakukan proses penginputan penawaran penjualan ke Customer. 

- Pada form **Quotation**, terdapat field Customer yaitu field yang berisi pelanggan yang melakukan pemesanan barang. Untuk mencari nama CV yang bersangkutan tekan tombol dropdown pada field Customer dan pilih **Search More**.

.. image:: /img/mp-searchmore.png

- Maka akan masuk pada tampilan form **Searh: Costomer**, kemudian input nama CV atau perusahaan yang dicari. 

 .. image:: /img/mp-mp-searchcustomer.png 

 - Selanjutnya terdapat field Delivery Address yang berisi alamat pengiriman penawaran penjualan, untuk field ini telah tersedia dengan daftar alamat pengiriman dari perusahaan yang bersangkutan. Namun, jika tidak tersedia dapat meng-create alamat dari perusahaan tersebut.

 .. image:: /img/mp-deliveryadd.png    

- Selanjutnya pada terdapat field Attention yang berisi orang yang dituju untuk penawaran, untuk field ini telah tersedia dengan daftar nama orang yang dituju untuk penawaran. Namun, jika tidak tersedia dapat meng-create nama orang yang dituju tersebut.

.. image:: /img/mp-attention.png

- Selanjutnya terdapat field Invoice Address yang berisi alamat faktur, untuk field ini telah tersedia dengan daftar alamat faktur yang dituju untuk penawaran. Namun, jika tidak tersedia dapat meng-create alamat faktur yang dituju tersebut. 

.. image:: /img/mp-invoiceadd.png

- Selanjutnya terdapat field Currency yaitu merupakan tipe mata uang yang akan digunakan, didalamnya telah tersedia dengan tipe-tipe mata uang. 

.. image:: /img/mp-currency.png

- Selanjutnya terdapat field Date yang berisi tanggal dari penawaran penjualan. 

.. image:: /img/mp-date.png

- Selanjutnya terdapat field Salesperson yang berisi nama sales yang akan melakukan proses penawaran penjualan. Untuk mencari nama sales yang bersangkutan tekan tombol dropdown pada field Salesperson dan pilih **Search More**. 

.. image:: /img/mp-salessearch.png

- Maka akan masuk pada tampilan form **Searh: Sales**, kemudian input nama Sales. 

.. image:: /img/mp-salessearch1.png

- Selanjutnya pada field Sale Group berisi grup dari sales. Untuk mencari nama Group Sale tekan tombol dropdown pada field Sales Group dan pilih **Search More**.  

.. image:: /img/mp-searchsalesgr.png

- Maka akan masuk pada tampilan form **Searh: Sale Group**, kemudian input Sale Group. 

.. image:: /img/mp-searchsalesgr1.png

- Selanjutnya terdapat tab Sale Items yang berisi list item yang akan dijual, untuk menambahkan item yang akan dijual tekan **Add an item**

.. image:: /img/mp-tabsaleitem.png

- Maka akan masuk pada tampilan form Order Lines dimana pada form ini dapat diisi dengan item yang akan dijual. 

.. image:: /img/mp-formorderline.png

- Pada form Order Lines terdapat field Product yag berisi produk yang ditawarkan pada Customer. Untuk mencari nama Product yang diinginkan tekan tombol dropdown pada field Product dan pilih **Search More**.

- Maka akan masuk pada tampilan form **Searh: Product**, kemudian input nama Product. 

.. image:: /img/mp-searchproduct.png

- Selanjutnya terdapat field Description yang berisi deksripsi item yang ditawarkan dan material item yang ada didalamnya.

.. image:: /img/mp-desc.png

- Selanjutnya terdapat field Quantity yang berisi jumlah dari produk yang akan dijual dan tepat dibawah field tersebut terdapat satuan pengukuran dari product tersebut. 

.. image:: /img/mp-qty.png

- Selanjutnya terdapat field Unit Price yang merupakan harga dari produk yang dijual. 

.. image:: /img/mp-unitprice.png

- Selanjutnya terdapat field Discount yang berisi potongan harga dari produk dan Taxes atau pajak yang dikenakan pada produk tersebut.

.. image:: /img/mp-disandtax.png 

- Selanjutnya terdapat tab Material Line yang berisi daftar material yang termasuk dari item tersebut. Untuk menambah material item yang menjadi paket dari item dapat memilih **Add an item**.   

.. image:: /img/mp-material.png 

- Setelah semua field diisi maka tampilan form akan menjadi seperti dibawah ini. 

.. image:: /img/mp-formorderlineisi.png 

- Kemudian simpan hasil inputan Form dengan menekan tombol **Save & Close**.

- Masuk kembali pada tampilan form **Quotation**, terdapat tab Revision History yang berisi catatan apabila ada revisi dari penawaran penjualan.

 .. image:: /img/mp-revision.png

- Selanjutnya terdapat tan Scope Of Work yang berisi lingkup kerja.

  .. image:: /img/mp-scope.png

- Pada bagian bawah dari form terdapat field Payment Term yang menunjukkan batas waktu dari pembayaran.
  
.. image:: /img/mp-payment.png

- Selanjutnya terdapat field Create Invoice atau pembuatan faktur untuk menunjukkan kapan faktur dibuat.

.. image:: /img/mp-invoice.png

- Selanjutnya terdapat field Terms and Condition yang berisi ketentuan dan syarat yang akan digunakan.

.. image:: /img/mp-termcond.png

- Terdapat field Note untuk memberikan catatan dari penawaran penjualan.



Membuat Penawaran Material Include Jasa
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Contoh Kasus :
Pada kasus ini dilakukan penawaran 82 Set SACI (Self Aligning Carry Idler) include jasa pemasangan.  

 .. image:: /img/mp-includejasa1.png

 Untuk menambahkan jasa pada penawaran material. Masuk pada form order line dan pilih product yang akan dipesan dimana pada kasus ini Customer memesan 82 set SACI (Self Aligning Carry Idler). Pada bagian tab material line telah terisi dengan material item yang ter-include dengan item yang dipesan yaitu tiap 1 set SACI terdapat 1 Frame dan 3 set Carry Roller. Untuk menambah jasa pada penawaran material yaitu pilih **Add an item** dan masukkan jasa yang dibutuhkan.

  .. image:: /img/mp-includejasa2.png  

Melihat Picking Location berada pada daerah Pasar Kemis maka resource yang akan dipanggil akan berasal dari site Pasar Kemis.


Membuat Penawaran Jasa dengan Menetapkan Material yang akan digunakan
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Contoh Kasus :
Pada kasus ini dilakukan penawaran jasa yaitu Lining dimana pada penawarannya Customer juga memilih material yang akan digunakan.

.. image:: /img/mp-includematerial1.png

Untuk menambahkan material yang akan digunakan masuk pada form Order lines, pada bagian tab Material Item telah terisi dengan jasa yang telah dipesan. Untuk menambahkan material yang diinginkan yaitu pilih **Add an item** dan masukkan material yang dibutuhkan.

.. image:: /img/mp-includematerial2.png

Konfirmasi Penawaran
--------------------

Konfirmasi penawaran digunakan untuk mengkonfirmasi draft penawaran yang sudah di buat agar dapat di print dan dikirim ke Customer.
yaitu dengan menekan tombol Confirm.

.. image:: /img/mp-confirm.png


Print Penawaran
---------------

Print Penawaran dapat dilakukan setelah Konfirmasi Penawaran. Untuk mencetak data tekan tombol Print Quotation Web.

.. image:: /img/mp-print.png

Hasil data akan berbentuk file PDF dan siap untuk dicetak.

.. image:: /img/mp-hasilprint.png

Dengan begitu hasil cetak tersebut dapat digunakan sebagai penawaran penjualan pada Customer. Pada tahap berikutnya terjadi kembali negosiasi dengan Custommer.


Revisi Penawaran
----------------

Pada suatu kasus Costomer meminta perubahan pada penawaran penjualan. Dengan begitu, hal yang harus dilakukan adalah melakukan revisi penawaran. langkah-langkah yang harus dilakukan yaitu 

- Masuk kembali pada modul RFQ dan pilih draft penawaran penjualan untuk perusahaan bersangkutan. Untuk melakukan revisi tekan Revise.

.. image:: /img/mp-revise.png

- Maka akan masuk pada Form Reason / Explanation yang berisi catatan alasan perubahan penawaran penjualan.  

.. image:: /img/mp-revisereason.png

- Barulah setelah itu data penawaran kembali diubah sesuai dengan keinginan Customer. Dan tahap selanjutnya adalah kembali melakukan penginputan seperti pada tahap sebelumnya. Untuk melihat list revisi dari penawaran dapat melihat pada tab Revision History.

.. image:: /img/mp-revisionhistory.png


Cancel Penawaran / WIN / Lost
-----------------------------


Mengkonversi Penawaran menjadi Sale Order / Membuat Sale Order
--------------------------------------------------------------