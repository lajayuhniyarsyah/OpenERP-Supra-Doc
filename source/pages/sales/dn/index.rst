.. _pages_dn:

DELIVERY NOTE
=============

.. _pages_dn_penjelasan:

Penjelasan
----------

Merupakan modul untuk melakukan input surat jalan oleh sales.
Modul ini dapat di akses pada menu "Sales" -> "Sales" -> "Delivery Note"

.. _pages_dn_flow_delivery_note:

Flow Delivery Note
------------------

.. _pages_dn_flow:

Flow
''''

.. image:: /img/dn-normal-flow.png


#. Flow dimulai setelah melewati proses **Order Preparation** dimana barang telah dipacking oleh warehouse staff. 
#. Selanjutnya sales melakukan penginputan surat jalan melalui ERP pada modul menu Delivery Note. 
#. Setelah proses penginputan sudah lengkap maka sales dapat mencetak draft surat jalan di kertas dengan meng-submit dokumen terlebih dahulu. 
#. Selanjutnya sales terlebih dahulu meminta approve (persetujuan) dan tanda tangan dari manager atau bagian lain yang bersangkutan.
#. Selanjutnya setelah surat jalan disetujui maka akan ada proses negosiasi dengan customer, dari proses tersebut ada beberapa kemungkinan yaitu meng-cancel surat jalan karena adanya pembatalan pemesanan, meng-postpone surat jalan karena customer meminta barang untuk di tunda pengirimannya terlebih dahulu, atau validasi surat jalan kepada bagian warehouse yang berarti barang telah keluar dari gudang dan dikirim pada customer. 

.. _page_dn_action:

Action
''''''

.. _pages_dn_action_input:

Input Surat Jalan
`````````````````

==================== === =================================================================================================
Flow Sebelumnya      :   Admin Warehouse mendapat notfikasi Bahwa Barang sudah disiapkan melalui Dokumen Order Preparation
Validasi             :   - Dokumen OP sudah berstatus "Done"
                         - Qty Sesuai Dokumen OP
Interface            :   Tombol "Create", Form Delivery Note
Jika Action Sukses   :   Muncul Form, Data tersimpan jika sudah mengklik tombol "Save", status dokumen = 'Draft'
Jika Action Gagal    :   Muncul Pop Up Message Warning
User                 :   Admin Warehouse
Deskripsi            :   Menginput Surat Jalan berdasarkan Dokumen Order Preparation yang sudah Siap.
==================== === =================================================================================================

.. _pages_dn_action_submit:

Submit
````````

==================== = ===================================================================================================================================
Flow Sebelumnya      : Input Surat Jalan
Validasi             : Isi Dokumen Cocok dengan dokumen Order Preparation
Interface            : Tombol "Submit"
Jika Action Sukses   : - Status berubah menjadi "Submited"
                       - Dokumen tidak dapat di edit / update / ubah
Jika Action Gagal    : Muncul Pop Up Message Warning
User                 : Admin Warehouse
Deskripsi            : Mensubmit dokumen surat jalan dari Draft agar dapat di proses ke flow selanjutnya, selain itu agar draft surat jalan dapat di print
==================== = ===================================================================================================================================


Submit adalah action untuk mensubmit dokumen yang telah diinput. Jika dokumen telah di submit maka dokumen tidak dapat di modifikasi.
Submit digunakan untuk merubah state dari draft menjadi submited.
Ketika dokumen berstatus "Submited" maka artinya dokumen siap di print dan di akan direview oleh Admin Manager

.. _pages_dn_action_set_draft:

Set Draft
`````````

==================== = =======================================================================================
Flow Sebelumnya      : Submit
Validasi             : - Qty
Interface            : Tombol "Set Draft"
Jika Action Sukses   : - Status dokumen menjadi "Draft"
                       - Dokumen dapat di edit / update / revisi
Jika Action Gagal    : - Status dokumen tidak berubah
                       - Muncul Pesan Error
User                 : Admin SPV/Manager
Deskripsi            : Action untuk merevisi surat jalan yang sudah di submit pada sistem
==================== = =======================================================================================


.. _pages_dn_action_print_surat_jalan:

Print Surat Jalan
`````````````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Submit
Validasi             : 
Interface            : Tombol "Print"
Jika Action Sukses   : - Muncul pada display Print Output yang dapat di cetak ke template Surat Jalan
Jika Action Gagal    : - Muncul Error pada Layar
User                 : Admin Warehouse
Deskripsi            : Action untuk print surat jalan yang sudah di submit pada sistem
==================== = ==============================================================================================================================

.. _pages_dn_action_approval:

Approval Surat Jalan
````````````````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Print Surat Jalan
Validasi             : - Manual
Interface            : Manual
Jika Action Sukses   : -
Jika Action Gagal    : -
User                 : Admin SPV & Manager
Deskripsi            : Action ini menunjukkan proses approval surat jalan. Approval dilakukan secara manual. Dokumen  surat Jalan yang sebelumnya sudah di print oleh "Admin Warehouse" di ajukan ke Admin SPV dan Manager untuk di tandatangani. Selama proses tanda tangan maka SPV dan Manager akan memvalidasi ke absahan surat jalan yang akan di proses dengan hasil print out. Jika surat jalan sudah valid maka user Admin SPV dan Manager akan mentandatangani Surat Jalan dan memberi stempel bahwa barang sudah dapat di deliver ke Customer. Namun jika barang belum dapat dikirim ke Customer dengan beberapa alasan (menunggu barang complete / menunggu pembayaran/ dll) maka Admin SPV dan Manager dapat mentandatangani dan memberi Cap Label "Postpone" pada Surat Jalan
==================== = ==============================================================================================================================



.. _pages_dn_postpone:

Postpone
````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Menerima Dokumen Surat Jalan
Validasi             : Dokumen Surat Jalan telah ditandatangani / disetujui untuk di Tahan pengirimannya.
Interface            : Tombol "Postpone"
Jika Action Sukses   : - Status berubah menjadi "Postpone"
                       - Stock item sudah berkurang
Jika Action Gagal    : - Muncul Pop Up Message Warning
                       - Status dokumen tidak berubah menjadi "Postpone"
User                 : Warehouse Staff
Deskripsi            : Action ini digunakan untuk menahan dokumen pengiriman, sehigga pengiriman tidak dilakukan namun stock tetap tertahan sehingga tidak bisa di ambil untuk memenuhi permintaan lain. Dalam action ini user Warehouse Staff akan menerima dokumen surat jalan yang di beri label "Postpone" yang menandakan bahwa item delivery tersebut sudah di proses surat jalan namun ditahan pengirimannya atas perintah Admin Manager.
==================== = ==============================================================================================================================


Untuk proses kelanjutan pengiriman maka diberlakukan flow :


.. image:: /img/dnpostponeflow.png



.. _pages_dn_action_print_surat_jalan:

Validate Surat Jalan
````````````````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Menerima Dokumen Surat Jalan
Validasi             : - Surat jalan dapat di validate **jika surat jalan telah ditandatangani dan di beri keterangan bahwa item / package sudah diijinkan untuk keluar / dikirim.
Interface            : Tombol "Validate"
Jika Action Sukses   : Status dokumen menjadi "Done"
Jika Action Gagal    : - Muncul Pesan Error pada Layar
User                 : Warehouse Staff
Deskripsi            : Action ini digunakan saat Staff Warehouse menerima surat jalan printah untuk pengiriman barang.
==================== = ==============================================================================================================================


.. _pages_dn_action_cancel:

Cancel Surat Jalan
````````````````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Menerima Dokumen Surat Jalan
Validasi             : - Surat jalan dapat di validate **jika surat jalan telah ditandatangani dan di beri keterangan bahwa item / package **tidak diijinkan untuk dikirim dan untuk di bongkar packingnya sehingga dapat digunakan order lain**
Interface            : Tombol "Cancel"
Jika Action Sukses   : Status dokumen menjadi "Cancel"
Jika Action Gagal    : - Muncul Pesan Error pada Layar
User                 : Warehouse Staff
Deskripsi            : Action ini digunakan saat Staff Warehouse menerima surat jalan printah untuk cancel surat jalan.
==================== = ==============================================================================================================================


.. _pages_dn_action_repacking:

Repacking Surat Jalan
````````````````````````

==================== = ==============================================================================================================================
Flow Sebelumnya      : Postpone Surat Jalan
Validasi             : Dokumen Surat Jalan telah ditandatangani / disetujui untuk di Tahan pengirimannya dan diperintahkan untuk re packing order item untuk mengurangi/menambah/memodifikasi item yang ada di packing.
Interface            : Tombol "Cancel"
Jika Action Sukses   : Status dokumen menjadi "Cancel"
Jika Action Gagal    : - Muncul Pesan Error pada Layar
User                 : Warehouse Staff
Deskripsi            : Action ini dijalankan ketika sebelumnya terdapat perintah dari Manager Admin untuk membongkar packing untuk ditambahkan/dikurangkan/dimodifikasi item dalam packing tersebut. 
==================== = ==============================================================================================================================



.. _pages_dn_interface:

Interface / Tampilan
--------------------

.. _pages_dn_main_view:

Tampilan Utama / Tabel / Tree
'''''''''''''''''''''''''''''

.. _pages_dn_form:

Form Delivery Note
''''''''''''''''''

Berikut ini adalah tampilan Form Delivery Note :
 .. image:: /img/dn-1-edit.png



Penjelasan Field:

+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Delivery Note         | Ya            |Dokumen yang digunakan untuk Surat Jalan                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | SPK                   | Ya            |Nomor SPK (Surat Perintah Kerja)                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Order Packaging       | Ya            |Pemesanan pengemasan                                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | Customer Reference    | Ya            |Nomor PO                                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | Delivery Date         | Ya            |Tanggal Pengiriman Barang                                                                 |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|6  | Note Return           | Tidak         |Informasi Pengembalian Barang                                                             |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|7  | Special WO            | Tidak         |Informasi yang menunjukkan  Special Order                                                 |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|8  | SPK Internal          | Tidak         |Nomor SPK Internal                                                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|9  | Customer              | Ya            |Nama / Data Customer, nama perusahaan Customer                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|10 | Delivery Address      | Ya            |Nama Site / Alamat tempat Pengiriman yang akan dituju                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|11 | Attention             | Tidak         |Nama Orang yang dituju untuk penawaran                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|12 | Note Line             | Ya            |Dokumen mengenai item sell yang telah disiapkan                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|13 | Packing Lines         | Ya            |Dokumen mengenai detail kemasan item                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|14 | Notes                 | Tidak         |Dokumen catatan internal                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|15 | Others                | Tidak         |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|16 | Proses Return Products| Tidak         |Dokumen mengenai pengembalian barang                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|17 | Terms and Condition   | Tidak         |Catatan mengenai Ketentuan dan Syarat yang berlaku                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


Pada form tersebut terdapat **5 Tab**, yaitu :

.. _pages_dn_note_lines:

Note Lines
``````````

Note Lines merupakan item sale yang telah disiapkan dari suatu penawaran.
Pada Note Lines berisi pula informasi mengenai material tambahan yang merupakan paket dari item tersebut.
Item yang dimaksud adalah merupakan **Produk, ataupun Jasa** yang ditawarkan kepada Customer.



.. image:: /img/dn-2-edit.png

(Gambar Note Lines - Form / Detail)


Field yang ada pada **Note Lines**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | No                    | Ya            | Id dari item                                                                                                       |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Quantity              | Ya            | Banyaknya item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Packaging             | Ya            | Pengemasan                                                                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | UoM                   | Tidak         | Satuan pengukuran unit                                                                                             | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Description           | Tidak         | Deksripsi item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Refunded Item         | Tidak         | Pengembalian item                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Note Line Material    | Tidak         | List dari material yang merupakan paket dari item                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_dn_notes_lines_material:

Note Lines Material
```````````````````

Note Lines Material berisi daftar material yang merupakan paket dari item.



.. image:: /img/dn-3-edit.png

(Gambar Note Lines Material - Tree)



.. image:: /img/dn-note-lines-material.png

(Gambar Note Lines Material - Form / Detail)


Field yang ada pada **Note Line Material**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Refunded Item         | Ya            | Pengembalian Item                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | UoM                   | Ya            | Satuan pengukuran unit                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Serial Number         | Tidak         | No Batch Stock                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | State                 | Tidak         | Status                                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Stock Move            | Tidak         | Perpindahan Stock                                                                                                  | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Description           | Tidak         | Deksripsi item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Delivery Note Line    | Ya            | Catatan pemesanan                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | Qty                   | Ya            | Banyaknya item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|10 | OP Line               | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|11 | unknown               | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+

.. _pages_dn_packing_lines:

Packing Lines
`````````````

Packing Lines merupakan list mengenai detail kemasan.

.. image:: /img/dn-packaging-list.png

(Gambar Packing Lines - Form / Detail)


Field yang ada pada **Packing Lines**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Package               | Ya            | Paket                                                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Color Code            | Ya            | Kode Warna                                                                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Urgent                | Tidak         | Menunjukkan tingkat urgent dari paket                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | No                    | Ya            | Id dari item                                                                                                       |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Description           | Ya            | Deksripsi item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Quantity              | Ya            | Banyaknya item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Uom                   | Ya            | Satuan pengukuran unit                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | measurement           | Ya            | Banyaknya item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|10  | Weight               | Ya            | Berat dari item                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+

.. _pages_dn_notes:

Notes
`````

Notes berisi catatan internal.

.. image:: /img/dn-notes.png

(Gambar Packing Lines - Form / Detail)


Field yang ada pada **Notes**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Note                  | Ya            | Catatan internal                                                                                                   |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_dn_others:

Others
``````

.. image:: /img/dn-others.png

(Gambar Others - Form / Detail)


Field yang ada pada **Others**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Stock Picking         | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Postpone Picking      | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_dn_proses_return_products:

Proses Return Products
``````````````````````

Proses Return Products berisi informasi mengenai pengembalian barang.

.. image:: /img/dn-proses-return-products.png

(Gambar Proses Return Products - Form / Detail)


Field yang ada pada **Proses Return Products**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Reference             | Ya            | Referensi                                                                                                          |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Supplier              | Ya            | Penyedia produk                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Back Order of         | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Source Document       | Ya            | Sumber Dokumen                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Creation Date         | Ya            |                                                                                                                    | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Scheduled Time        | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Invoice Control       | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Stock Journal         | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | Status                | Ya            | Status                                                                                                             | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


.. _pages_dn_print_output:

Print Output
''''''''''''

.. image:: /img/dn-printout-raw.png