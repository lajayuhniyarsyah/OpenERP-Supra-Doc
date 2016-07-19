.. _pages_order:

SALES ORDER
===========

.. _pages_order_penjelasan:

Penjelasan
----------


Quotation/RFQ (Request For Quotation), merupakan modul untuk input penawaran penjualan ke Customer.
Modul ini dapat di akses pada menu "Sales" -> "Sales" -> "RFQ"


.. _pages_order_flow_quotation:

Flow Quotation
--------------

.. image:: /img/quotation.png


#. Flow dimulai dengan user menginput penawaran , dimana pada flow state ini form penawaran diinput oleh Sales melaui ERP pada modul menu RFQ.
#. Selanjutnya setelah inputan sudah lengkap maka user dapat mencetak penawaran di kertas dengan meng-konfirm dokumen terlebih dahulu. Pada state ini dokumen sudah fix dan tidak dapat diubah. Atau user dapat meng-cancel dokumen tersebut jika dokumen benar-benar tidak akan digunakan
#. Selanjutnya setelah penawaran diterima oleh Customer maka akan ada proses negosiasi, dari proses tersebut ada beberapa kemungkinan yaitu Revisi Penawaran, Deal, dan Tidak Deal / Lose a. Jika ingin merevisi penawaran maka user dapat merevisi penawaran di sistem lalu mengkonfirm kembali untuk mencetak revisi penawaran b. Jika pada saat negosiasi menghasilkan kesepakatan Jual Beli maka ketika turun PO dari Customer user dapat mengubah status penawaran menjadi Sale Order. Jika tidak ada kesepakatan atas penawaran tersebut maka user dapat mengubah status dokumen menjadi **lose** pada penawaran tersebut


.. _pages_order_interface:

Tampilan / Interface
--------------------

.. _pages_order_form_quotation:

Form quotation
''''''''''''''

.. image:: /img/order-rfq.png



Penjelasan Field: 

+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Customer              | Ya            |Nama / Data Customer, nama perusahaan Customer                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | Delivery Address      | Ya            |Nama Site / Alamat tempat Pengiriman yang akan dituju                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Attention             | Tidak         |Nama Orang yang dituju untuk penawaran                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | Invoice Address       | Tidak         |Alamat yang akan digunakan untuk Cetak Invoice                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | Currency              | Ya            |Mata uang yang digunakan dalam transaksi                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|6  | Date                  | Ya            |Tanggal Penawaran                                                                         |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|7  | Sales Person          | Ya            |Nama sales yang menawarkan                                                                |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|8  | Sale Group            | Ya            |Group Sales yang menawarkan                                                               |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|9  | Payment Term          | Ya            |Term Payment Sistem yang diberlakukan                                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|10 | Create Invoice        | Ya            |Trigger untuk membuat invoice :                                                           |
|   |                       |               |   1. On Demand - Invoice akan dibuat sesuai permintaan                                   |
|   |                       |               |   2. On Delivery Order - Invoice akan dikirim setelah barang dikirim / diterima          |
|   |                       |               |   3. Before Delivery - Invoice akan dikirim bersamaan dengan pengiriman barang           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|11 | Term and Conditions   | Tidak         |Group Sales yang menawarkan                                                               |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|12 | Base Total            | Tidak         |Informasi Total nilai Sebelum Discount                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|13 | Discount              | Tidak         |Informasi nilai total discount dalam penawaran                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|14 | Sub Total             | Tidak         |Informasi Total nilai setelah Discount / Dasar Pengenaan Pajak (DPP)                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|15 | Tax                   | Tidak         |Informasi nilai pajak yang dikenakan dalam penawaran                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|16 | Total                 | Tidak         |Total nilai transaksi                                                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|17 | Sale Items            | Ya            |List item / produk yang di tawarkan                                                       |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|18 | Revision History      | Tidak         |List Data Revisi yang pernah dilakukan, terisi otomatis pada saat dilakukan revisi pada   |
|   |                       |               |dokumen                                                                                   |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|19 | Scope Of Work         | Tidak         |Berisi Scope of work baik dari sisi Customer maupun Suprabakti Mandiri                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


Pada form tersebut terdapat **3 Tab**, yaitu :

.. _pages_order_sale_items:

Sale Items
``````````


Sale items merupakan item sale dari suatu penawaran.
Item yang dimaksud adalah merupakan **Produk, ataupun Jasa** yang ditawarkan kepada Customer.
Item yang ditawarkan bisa saja dalam satuan kumulatif seperti SET, LOT, dll.



.. image:: /img/order-sale-items.png

(Gambar Sale Item - Tree)



.. image:: /img/order-sale-items-baru.png

(Gambar Sale Item - Form / Detail)


Field yang ada pada **Sale Item**: 

+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Product               | Ya            | Item yang akan ditawarkan                                                                                          |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Description           | Tidak         | Deskripsi item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Qty                   | Ya            | Banyaknya item yang ditawarkan, berserta satuannya (Satuan bisa dalam 1 satuan kumulatif, seperti lot, set dll)    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Unit Price            | Ya            | Harga item per satuan                                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Discount              | Tidak         | Field Sebelah kiri merupakan discount dalam persentase (%), di sebelah kanan merupakan disocunt dalam angka nilai  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Base Total            | Tidak         | Harga total kotor, yaitu harga unit price x qty sale                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Subtotal              | Tidak         | Total harga setelah dikurangi discount,                                                                            |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Taxes                 | Tidak         | Pajak yang dikenakan untuk suatu item                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | Tax Amount            | Tidak         | Total nilai pajak yang dikenakan pada 1 sale item tersebut                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|10 | Material Line         | Ya            | Berisi list material yang akan di aplikasikan kepada order tersebut, material line melingkupi material apa saja    |
|   |                       |               | yang akan di berikan ke customer baik berupa barang maupun jasa                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_order_material_line:

Material Line
`````````````

Material line merupakan data Material yang akan di supply pada suatu order baik material berupa barang maupun barang.
Pada material line harus di deskripsikan material penyusun / consist of / including material yang akan di berikan kepada customer.

.. image:: /img/order-material-line.png

(Gambar Material Item pada Quotation)

Contoh : 

- Terdapat permintaan penawaran item Super Screw 65 BW 100. Dalam penawaran disertakan juga bahwa material include nya adalah spacer, screw dan belt Super Screw nya sendiri maka pada material item harus di input semua material yang di include kan dalam 1 sale item tersebut yaitu SS 65, Spacer dan Screw sebanyak jumlah yang dibutuhkan.

Field yang ada pada **Material Line** :

+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Material Item         | Ya            | Item yang akan di supply untuk suatu order                                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Description           | Tidak         | Deskripsi item                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Qty                   | Ya            | Qty yang akan dikirim dari material                                                                                |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Unit                  | Ya            | Satuan unit dari material yang akan dikirim                                                                        |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Picking Location      | Ya            | Sumber Tempat/Site/Warehouse stock material tersebut berada                                                        |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_order_revision_history:

Revision History
````````````````

Berisi log history revisi yang pernah dilakukan, log berisi alasan mengapa dilakukan revisi dan nilai yang di revisi


.. image:: /img/rfq-revision-history.png

(Gambar Tab Revision History)


Field yang ada pada **Revision History** :

+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | No#                   | Tidak         | Nomor Quotation                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Total (Tax Exclude)   | Tidak         | Total nilai penawaran yang direvisi                                                                                |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Reason of Revision    | Tidak         | Alasan / Penjelasan mengapa penawaran tersebut di revisi                                                           |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Date                  | Tidak         | Tanggal Revisi                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_order_scope_of_work:

Scope Of Work
`````````````

Pada tab **Scope of Work** terdapat field Detail scope of work baik dari Sisi Suprabakti maupun sisi Customer. Field ini diisi untuk menjelaskan scope lingkup pekerjaan yang dilakukan baik di sisi Customer maupun Suprabakti Mandiri.



Contoh Kasus


-. Membuat penawaran Jasa Include Material

1. Dilakukan Penawaran ke PT. Indocement Persero, Tbk untuk item Super Screw 65 BW 1200



-. Membuat penawaran Penjualan Material include dengan Jasa (Pemasangan/Instalasi)
-. Membuat penawaran Penjualan Material yang material berasal dari Site


