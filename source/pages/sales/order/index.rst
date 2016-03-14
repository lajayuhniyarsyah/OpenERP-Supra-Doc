ORDER
=====


Quotation / RFQ
---------------
Contents:

Quotation/RFQ (Request For Quotation), merupakan modul untuk input penawaran penjualan ke Customer.
Modul ini dapat di akses pada menu "Sales" -> "Sales" -> "RFQ"


Flow Quotation

.. image:: /img/quotation.png


#. Flow dimulai dengan user menginput penawaran , dimana pada flow state ini form penawaran diinput oleh Sales melaui ERP pada modul menu RFQ.
#. Selanjutnya setelah inputan sudah lengkap maka user dapat mencetak penawaran di kertas dengan meng-konfirm dokumen terlebih dahulu. Pada state ini dokumen sudah fix dan tidak dapat diubah. Atau user dapat meng-cancel dokumen tersebut jika dokumen benar-benar tidak akan digunakan
#. Selanjutnya setelah penawaran diterima oleh Customer maka akan ada proses negosiasi, dari proses tersebut ada beberapa kemungkinan yaitu Revisi Penawaran, Deal, dan Tidak Deal / Lose a. Jika ingin merevisi penawaran maka user dapat merevisi penawaran di sistem lalu mengkonfirm kembali untuk mencetak revisi penawaran b. Jika pada saat negosiasi menghasilkan kesepakatan Jual Beli maka ketika turun PO dari Customer user dapat mengubah status penawaran menjadi Sale Order. Jika tidak ada kesepakatan atas penawaran tersebut maka user dapat mengubah status dokumen menjadi **lose** pada penawaran tersebut



Form Quotation :

Diisi gambar form Quotation



Penjelasan Field: 

+---+-------------------+---------------+-----------------------------------+
|NO | Fileds            | Harus Diisi   | Keterangan                        |
+===+===================+===============+===================================+
|1  | Customer          | Ya            |                                   |
+---+-------------------+---------------+-----------------------------------+
|2  | Delivery Address  | Ya            |                                   |
+---+-------------------+---------------+-----------------------------------+
|3  | Attention         | Tidak         |                                   |
+---+-------------------+---------------+-----------------------------------+






SALE ORDER
----------


ADHOC ORDER
-----------
