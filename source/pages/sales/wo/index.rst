SBM Work Order
==============


Contents:

SBM Work Order, merupakan modul untuk.....




Flow SBM Work Order

.. image:: /img/Gm50U.jpg

1. Flow dimulai dengan user Admin Support yang melakukan proses SO, setelah itu berlanjut ke proses permintaan SPK. Selanjutnya adalah melakukan konfirmasi oleh user yang bersangkutan (Admin Support).

2. Setelah konfirmasi selesai, tahap selanjutnya adalah pengecekan SPK oleh user Admin (HO). Pada tahap ini terdapai 3 (tiga) pilihan yaitu cancel, revisi dan ok. a. Cancel, berarti membatalkan semua proses sebelumnya dan proses berhenti. b. Revisi, berarti proses sebelumnya diarahkan ke proses set Draft untuk ditinjau ulang pada proses permintaan SPK oleh user Admin Support. c. Ok, berarti SPK telah lolos pengecekan dan berlanjut ke proses Validasi dan Approval oleh Supervisor.

3. Apabila sudah di approve oleh supervisor, proses selanjutnya adalah Approval Admin oleh Manager. Pada tahap ini ada 3 (tiga) pilihan yaitu revisi, cancel dan approved. a. Revisi, berarti proses sebelumnya diarahkan ke proses set Draft untuk ditinjau ulang pada proses permintaan SPK oleh user Admin Support. b. Cancel, berarti membatalkan semua proses sebelumnya dan proses berhenti. c. Approved, berarti berlanjut ke proses Resease SPK ke Workshop. Artinya SPK siap dikirim ke workshop.

4. Kemudian adalah proses penerimaan SPK, setelah SPK diterima maka selanjutnya diproses sampai SPK selesai. SPK ini berisi tentang Referensi Order, Pemakaian Material, dll.

5. Jika SPK sudah selesai maka ada pilihan Tagih dan Kirim Output. a. Tagih, berarti proses sebelumnya adalah berupa order jasa dan langsung diarahkan ke Invoicing. b. Kirim Output, berarti proses sebelumnya adalah order barang yang harus melalui proses Delivery Note. Jika proses Delivery Note Selesai baru melakukan penagihan dan langsung ke proses Invoicing.


Form SBM Work Order :

.. image:: /img/sbm-work-order-form.png

(Gambar SBM Work Order - Form / Detail)

Penjelasan field :

+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields                    | Harus Diisi     | Keterangan                                                              |
+====+===========================+=================+=========================================================================+
| 1  | Request No                | Tidak           | Nomor SPK                                                               |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Source Type               | Ya              | Tipe SPK                                                                |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Sale Order                | Ya              | Nomor SO                                                                |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Costumer                  | Tidak           | Costumer                                                                |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Costumer Work Location    | Ya              | Alamat Site Costumer                                                    |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 6  | Work Location             | Ya              | Lokasi Pekerjaan                                                        |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 7  | Internal Handler Location | Ya              | Lokasi Resource                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 8  | Due Date                  | Ya              | Due Date                                                                |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 9  | Order Date                | Tidak           | Tanggal Pemesanan                                                       |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 10 | Output Picking            | Ya              | Keluaran Yang Diambil                                                   |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 11 | Others                    | Tidak           |                                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 12 | Notes                     | Tidak           | Catatan Pengirim/Penjual dan Penerima/Costumer                          |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+


Pada form tersebut terdapat **2 Tab**, yaitu :


Output Picking
--------------

Output Picking merupakan......


.. image:: /img/sbm-work-order-output-picking.png

(Gambar Output Picking - Tree)

.. image:: /img/sbm-work-order-output-picking-raw-materials.png

(Gambar Output Picking: Raw Material - Form / Detail)

Penjelasan field:

+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields                    | Harus Diisi     | Keterangan                                                              |
+====+===========================+=================+=========================================================================+
| 1  | Products                  | Ya              | Produk Yang Ditawarkan                                                  |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Description               | Tidak           | Deskripsi Produk                                                        |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Qty                       | Ya              | Banyaknya Item Produk                                                   |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 4  | UoM                       | Ya              | Satuan Item Produk                                                      |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Attach a File             | Ya              | Dokumen Yang Berkaitan Dengan Produk                                    |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 6  | Data Material             | Ya              | Material Produk                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 7  | Output Picking            | Ya              | Keluaran Yang Diambil                                                   |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+


Pada form tersebut terdapat **2 Tab**, yaitu :


> Data Material
+++++++++++++++

Data Material merupakan......

.. image:: /img/sbm-work-order-output-picking-raw-materials-data-material.png

(Gambar Output Picking: Raw Material: Data Material - Form / Detail)

Penjelasan field:

+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields                    | Harus Diisi     | Keterangan                                                              |
+====+===========================+=================+=========================================================================+
| 1  | Products                  | Ya              | Produk Yang Ditawarkan                                                  |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Description               | Tidak           | Deskripsi Produk                                                        |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Qty                       | Ya              | Banyaknya Item Produk                                                   |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 4  | UoM                       | Ya              | Satuan Item Produk                                                      |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Costumer Materials        | Tidak           | Jika Produknya Berasal Dari Costumer                                    |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+


> Output Picking
++++++++++++++++

Output Picking merupakan.......

.. image:: /img/sbm-work-order-output-picking-raw-materials-output-picking.png

(Gambar Output Picking: Raw Material: Output Picking - Form / Detail)

Penjelasan field:

+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields                    | Harus Diisi     | Keterangan                                                              |
+====+===========================+=================+=========================================================================+
| 1  | Output                    | Ya              |                                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Work Order                | Tidak           |                                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Picking                   | Tidak           |                                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Move                      | Tidak           |                                                                         |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+



Others
------

Others merupakan......


.. image:: /img/sbm-work-order-others.png

(Gambar Others - Form / Detail)


Penjelasan field:

+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields                    | Harus Diisi     | Keterangan                                                              |
+====+===========================+=================+=========================================================================+
| 1  | Repeat Ref                | Tidak           | Repeat Referensi Order Sebelumnya                                       |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Approver                  | Tidak           | User Yang Menyetujui Pesanan/Order                                      |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Validator                 | Tidak           | User Yang Memvalidasi Pesanan/Order                                     |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+
| 4  | General Approver          | Tidak           | General User Yang Menyetujui Pesanan/Order                              |
+----+---------------------------+-----------------+-------------------------------------------------------------------------+




Print Out
---------

.. image:: /img/wo-printout-raw.png