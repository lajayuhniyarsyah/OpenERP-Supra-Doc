.. _pages_wo:

Work Order
==========


.. _pages_wo_penjelasan:

Penjelasan
----------

Work Order, merupakan modul untuk membuat doc surat perintah kerja yang dilakukan oleh Admin HO sebagai dasar doc untuk melakukan pekerjaan dengan mendetailkan segala informasi yang dibutuhkan



.. _pages_wo_flow_sbm_work_order:

Flow Work Order
-------------------

.. image:: /img/Gm50U.jpg

1. Flow dimulai dengan user Admin Support yang melakukan proses SO, setelah itu berlanjut ke proses permintaan SPK. Selanjutnya adalah melakukan konfirmasi oleh user yang bersangkutan (Admin Support).

2. Setelah konfirmasi selesai, tahap selanjutnya adalah pengecekan SPK oleh user Admin (HO). Pada tahap ini terdapai 3 (tiga) pilihan yaitu cancel, revisi dan ok. a. Cancel, berarti membatalkan semua proses sebelumnya dan proses berhenti. b. Revisi, berarti proses sebelumnya diarahkan ke proses set Draft untuk ditinjau ulang pada proses permintaan SPK oleh user Admin Support. c. Ok, berarti SPK telah lolos pengecekan dan berlanjut ke proses Validasi dan Approval oleh Supervisor.

3. Apabila sudah di approve oleh supervisor, proses selanjutnya adalah Approval Admin oleh Manager. Pada tahap ini ada 3 (tiga) pilihan yaitu revisi, cancel dan approved. a. Revisi, berarti proses sebelumnya diarahkan ke proses set Draft untuk ditinjau ulang pada proses permintaan SPK oleh user Admin Support. b. Cancel, berarti membatalkan semua proses sebelumnya dan proses berhenti. c. Approved, berarti berlanjut ke proses Resease SPK ke Workshop. Artinya SPK siap dikirim ke workshop.

4. Kemudian adalah proses penerimaan SPK, setelah SPK diterima maka selanjutnya diproses sampai SPK selesai. SPK ini berisi tentang Referensi Order, Pemakaian Material, dll.

5. Jika SPK sudah selesai maka ada pilihan Tagih dan Kirim Output. a. Tagih, berarti proses sebelumnya adalah berupa order jasa dan langsung diarahkan ke Invoicing. b. Kirim Output, berarti proses sebelumnya adalah order barang yang harus melalui proses Delivery Note. Jika proses Delivery Note Selesai baru melakukan penagihan dan langsung ke proses Invoicing.



Action Work Order
-----------------

Input Work Order
''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Admin HO mendapatkan Notifikasi / Informasi Bahwa harus membuat doc Work Order (SPK)     |
|                                 |   | Dimana dasar pembuatan Work Order                                                        |
|                                 |   | 1. Project                                                                               |
|                                 |   | 2. Sales Order                                                                           |
|                                 |   | 3. Adhoc Order Request                                                                   |
|                                 |   | 4. Internal Request                                                                      |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | 1. Adanya Source Type                                                                    |
|                                 |   | 2. Adanya Work Location                                                                  |
|                                 |   | 3. Adanya Internal Handler Location                                                      |
|                                 |   | 4. Adanya Output Picking                                                                 |
|                                 |   | 5. Adanya Raw Material                                                                   |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Create", Form Work Order                                                         |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | Muncul Form, Data tersimpan jika sudah mengklik tombol "Save", status dokumen = 'Draft'  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin HO / Admin Support                                                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Input Doc Work Order Berdasarkan permintaan  yang telah di approve oleh manager          |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Confirm Work Order
''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Input Doc Work Order Success                                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Confirm" Form Work Order status 'Draft'                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Confirmed"                                                |
|                                 |   | 2. Doc Work Order tidak dapat di edit / update / ubah                                    |
|                                 |   | 3. Terbentuknya Request No Doc Work Order                                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin HO / Admin Support                                                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Menconfirm doc Work Order dari Draft agar dapat di proses ke flow selanjutnya            |
+---------------------------------+---+------------------------------------------------------------------------------------------+




Set To Draft Work Order
'''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Confirm doc Work Order / Approve Work Order                                              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | -                                                                                        |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Set To Draft","Check WO", "Cancel" Form Work Order status 'Confirmed'            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Draft"                                                    |
|                                 |   | 2. Doc Work Order dapat di edit / update / ubah                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin Supervisor                                                                         |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan set to draft doc Work Order dari confirmed agar dapat di edit kembali          |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Check Work Order
''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Confirm doc Work Order / Approve Work Order                                              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Set To Draft","Check WO", "Cancel" Form Work Order status 'Confirmed'            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Approved"                                                 |
|                                 |   | 2. Doc Work Order Tidak dapat di edit / update / ubah                                    |
|                                 |   | 2. Terbentuk nya SPK No                                                                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin HO                                                                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan Check Work Order dari Confirmed ke Approved agar dapat di proses ke next flow  |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Cancel Work Order
'''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Confirm doc Work Order / Approve Work Order                                              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Work Order sudah di Approve untuk di cancel di system                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Set To Draft","Check WO", "Cancel" Form Work Order status 'Confirmed'            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "cancel"                                                   |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Doc Tidak dapat ter cancel                                                               |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin Supervisor / Admin Manager                                                         |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan Cancel Work Order Confirmed ke Cancel                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Validate Work Order
'''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approve doc Work Order                                                                   |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Set To Draft","Validate WO", "Cancel", "Print Work order"                        |
|                                 |   | Form Work Order status 'Approved'                                                        |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Second Approved"                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning / Doc Tidak Dapat di Validate                              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin Supervisor / Admin Manager                                                         |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan Validate Work Order Approved ke Second Approved                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Print Work Order
''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approve doc Work Order                                                                   |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | -                                                                                        |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Print Work Order"                                                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | Muncul pada display Print Output yang dapat di cetak                                     |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Error Pada Layar                                                                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin HO / Admin Support / Admin Supervisor / Admin Manager / Admin Workshop             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Action untuk print Work Order yang sudah di approve / Validate pada sistem               |
+---------------------------------+---+------------------------------------------------------------------------------------------+



Process Work Order
''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approved doc Work Order                                                                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Process Work Order"                                                              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Validate"                                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning / Doc Tidak Dapat di process                               |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin Manager                                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan Process Work Order, Second Validate ke Validate                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Finish Work Order
''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Second Approved doc Work Order                                                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Finish Work Order"                                                               |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Done"                                                     |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning / Doc Tidak Dapat di Finish process                        |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Admin Workshop                                                                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan Finish Work Order, Validate ke Done                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+


.. _pages_wo_interface:

Interface / Tampilan
--------------------

.. _pages_wo_main_view:

Tampilan Utama / Tabel / Tree
'''''''''''''''''''''''''''''

.. _pages_wo_form_sbm_work_order:

Form SBM Work Order
'''''''''''''''''''

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

.. _pages_wo_output_picking:

Output Picking
``````````````

Output Picking merupakan Informasi data pekerjaan dan product yang akan dijadikan dasar pengerjaan atau pembuatan product pada SPK 


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

.. _pages_wo_data_material:

Data Material
+++++++++++++


Data Material merupakan Detail Item yang menjalaskan lebih detail apa saja yang dibutuhkan dalam satu pekerjaan atau dalam menyiapkan barang, semua dapat dijelaskan dalam detail material

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


.. _pages_wo_output_picking:

Output Picking
++++++++++++++

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


.. _pages_wo_others:

Others
``````

Others merupakan informasi tambahan untuk users siapa yang Approve, Validate dan General Approver


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




Print Output
''''''''''''

.. image:: /img/wo-printout-raw.png
