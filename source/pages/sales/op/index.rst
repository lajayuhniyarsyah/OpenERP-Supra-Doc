.. _pages_op:

Order Preparation
=================


.. _pages_op_penjelasan:

Penjelasan
----------

Order Preparation / Delivery Order merupakan Modul dokumen Perintah Penyiapan Barang Ke Gudang di Suprabakti Mandiri.

Modul ini dapat di akses pada menu "Sales" -> "Sales" -> "Order Preparation"


.. _pages_op_flow_order_preparation:

Flow Order Preparation
----------------------

.. image:: /img/quotation.png

(Penjelasan tentang Order Preparation di skip)


.. _pages_op_interface:

Interface / Tampilan
--------------------


.. _pages_op_main_view:

Tampilan Utama
''''''''''''''

Tampilan utama ketika mengakses modul Order Preparation adalah berbentuk Tabel / Tree.
Pada tabel berisi informasi seperti Nomor dokumen, tanggal pembuatan, referensi, dll.

.. image:: /img/op-1.png


.. _pages_op_form_order_preparation:

Form Order Preparation
''''''''''''''''''''''

Pada Tampilan Utama terdapat tombol **Create** dimana tombol tersebut berfungsi untuk membuka **Form Order Preparation**.


.. _pages_op_main_form:

Form Utama
++++++++++

Berikut ini adalah tampilan form Order Preparation

.. image:: /img/op-1-edit.png


Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  | Reference            | Ya              | Nomor Dokumen PO                                                        |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Sale Order           | Ya              | Nomor SO Pesanan                                                        |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Customer Reference   | Tidak           | Nomor PO Costumer                                                       |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Delivery Address     | Tidak           | Alamat pengiriman yang akan dituju                                      |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Date Preparation     | Tidak           | Tanggal persiapan sebelum pengiriman                                    |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 6  | Customer             | Tidak           | Nama/Costumer perusahaan                                                |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 7  | Product Location     | Ya              | Lokasi produk pengirim                                                  |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 8  | Delivery Date        | Tidak           | Tanggal pengiriman                                                      |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 9  | Order Lines          | Ya              | List produk yang ditawarkan                                             |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 10 | Delivery Notes       | Tidak           | Surat pengantar                                                         |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 11 | Notes                | Tidak           | Catatan oleh penerima/costumer                                          |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 12 | Others               | Tidak           |                                                                         |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 13 | Terms and Conditions | Tidak           | Catatan oleh pengirim/penjual                                           |
+----+----------------------+-----------------+-------------------------------------------------------------------------+

Pada form tersebut terdapat **4 Tab**, yaitu :


.. _pages_op_order_lines:

Order Lines
```````````

Tab Order Lines berisikan list item yang harus di siapkan oleh Warehouse. Dalam list tersebut juga lengkap dengan quantity dan unit yang harus disiapkan.


.. image:: /img/op-order-lines.png

(Gambar Order Lines - Tree)

.. image:: /img/op-2-edit.png

(Gambar Order Lines - Form / Detail)

Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  | No                   | Tidak           | No urut                                                                 |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Quantity             | Ya              | Banyaknya item yang ditawarkan                                          |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Description          | Tidak           |                                                                         |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Detail Product       | Tidak           | Detail dari produk yang ditawarkan                                      |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Product              | Ya              | Produk yang ditawarkan                                                  |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 6  | UoM                  | Ya              | Satuan item                                                             |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 7  |                      | Ya              |                                                                         |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 8  | Sale Item            | Tidak           | Item sale dari suatu penawaran                                          |
+----+----------------------+-----------------+-------------------------------------------------------------------------+


Gambar lanjutan:

.. image:: /img/op-3-edit.png

(Gambar Order Lines - Form / Detail)

Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  | Serial Number        | Tidak           | Nomor Seri Produk                                                       |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Description          | Tidak           | Deskripsi produk                                                        |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Exp Date             | Tidak           | Tanggal habis masa produk                                               |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Stock Available      | Tidak           | Stok yang tersedia                                                      |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Qty                  | Tidak           | Banyaknya item yang di order                                            |
+----+----------------------+-----------------+-------------------------------------------------------------------------+



.. _pages_op_delivery_note:

Delivery Note
`````````````

Delivery Note merupakan surat pengantar pada pengiriman suatu produk ke Costumer.

.. image:: /img/op-delivery-note.png

(Gambar Delivery Note - Tree)

Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  | Date Created         | Tidak           | Tanggal terbuatnya DN                                                   |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 2  | Delivery Note        | Ya              | Nomor Surat Pengantar/DN                                                |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 3  | Order Packaging      | Ya              | Nomor Order Packaging                                                   |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 4  | Costumer Reference   | Tidak           | Nomor PO Costumer                                                       |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 5  | Costumer             | Tidak           | Nama/Costumer Perusahaan                                                |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 6  | Delivery Date        | Tidak           | Tanggal Pengiriman                                                      |
+----+----------------------+-----------------+-------------------------------------------------------------------------+
| 7  | State                | Tidak           | Status Pengiriman                                                       |
+----+----------------------+-----------------+-------------------------------------------------------------------------+


.. _pages_op_notes:

Notes
`````

Notes adalah catatan oleh pihak pengirim/penjual dan penerima/costumer produk.

.. image:: /img/op-notes.png


Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  |                      | Tidak           | Catatan oleh pihak penerima/costumer produk                             |
+----+----------------------+-----------------+-------------------------------------------------------------------------+

 .. _pages_op_others:

Others
``````

Others adalah...

.. image:: /img/op-others.png


Penjelasan field :

+----+----------------------+-----------------+-------------------------------------------------------------------------+
| NO | Fields               | Harus Diisi     | Keterangan                                                              |
+====+======================+=================+=========================================================================+
| 1  | Delivery Order       | Tidak           | Nomor delivery order produk                                             |
+----+----------------------+-----------------+-------------------------------------------------------------------------+


.. _pages_op_print_out:

Print Output
''''''''''''
.. image:: /img/op-printout.png