.. _pages_adhoc:

ADHOC ORDER REQUEST
===================


.. _pages_adhoc_penjelasan:

Penjelasan
----------

Adhoc Order merupakan modul Pemesanan yang dilakukan tanpa P.O diawal namun telah mendapat kesepakatan  antar Suprabakti dan Customer.

.. _pages_adhoc_flow_adhoc_order_request:

Flow Adhoc Order Request
------------------------

.. image:: /img/adhoc-flow.png


#. Flow dimulai setelah SALES mendapatkan perintah kerja oleh customer
#. Perintah Kerja telah di setujui oleh atasan untuk di proses 
#. Sales Menerima Doc atau sesuatu bukti bahwa customer menyuruh mengerjakan kerjaan dengan PR (Purchase Requisition) atau jika tidak bisa, dapat menggunakan Email yang telah di setujui
#. Selanjutnya sales /admin support melakukan penginputan Adhoc Order Request melalui ERP pada modul menu Adhoc Order Request.
#. Setelah proses penginputan sudah lengkap maka sales / admin support dapat melakukan submit dan print out doc Adhoc.
#. Jika dalam proses berjalan akan adanya revisi doc Adhoc yang sudah di submit, maka doc dapat di rubah ke draft dan di edit kembali.
#. Selanjutnya sales / admin support terlebih dahulu meminta approve (persetujuan) dan tanda tangan dari manager atau bagian lain yang bersangkutan.
#. Setelah doc sudah di approve (di ACC), maka secara system doc adhoc harus di approve untuk di proses menjadi SPK (Surat Perintah Kerja)
#. Setelah status dari doc Adhoc Order Request sudah sudah approve, maka adhoc sudah dapat dibuatkan SPK(Surat Perintah Kerja)


Action Adhoc Order Request
--------------------------

Input Adhoc Order Request
'''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Sales/Admin Support mendapatkan approve untuk memproses permintaan customer              |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | 1. Adanya customer                                                                       |
|                                 |   | 2. Adanya Attention                                                                      |
|                                 |   | 3. Adanya Customer Ref                                                                   |
|                                 |   | 4. Adanya Cust Ref No                                                                    |
|                                 |   | 5. Adanya Sales                                                                          |
|                                 |   | 6. Adanya Sales Group                                                                    |
|                                 |   | 7. Adanya Due Sate                                                                       |
|                                 |   | 8. Adanya Term Of Payment                                                                |
|                                 |   | 9. Adanya Detail Item                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Create", Form Adhoc Order Request                                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | Muncul Form, Data tersimpan jika sudah mengklik tombol "Save", status dokumen = 'Draft', |
|                                 |   | dan mendapatkan No Adhoc Order Request                                                   |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Input Doc Adhoc Berdasarkan permintaan customer yang telah di approve oleh manager       |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Submit Adhoc Order Request
''''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Input Doc Adhoc Order Request Success                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Submit", Form Adhoc Order Request status 'Draft'                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Submited"                                                 |
|                                 |   | 2. Doc Adhoc Order Request tidak dapat di edit / update / ubah                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Mensubmit doc Adhoc Order Request dari Draft agar dapat di proses ke flow selanjutnya    |
+---------------------------------+---+------------------------------------------------------------------------------------------+

Submit adalah action untuk mensubmit doc Adhoc Order Request yang telah diinput. Jika doc telah di submit maka doc tidak dapat di modifikasi. Submit digunakan untuk merubah state dari draft menjadi submited. Ketika dokumen berstatus "Submited" maka artinya dokumen siap di proses ke step selanjutnya untuk di review



Set To Draft Adhoc Order Request
''''''''''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Submit doc Adhoc Order Request                                                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Submit","Set To Draft", Form Adhoc Order Request status 'Submit'                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Draft"                                                    |
|                                 |   | 2. Doc Adhoc Order Request dapat di edit / update / ubah                                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Melakukan set to draft doc Adhoc Order Request dari submit agar dapat di edit kembali    |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Approve Adhoc Order Request
'''''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Submit doc Adhoc Order Request                                                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Submit","Set To Draft" Form Adhoc Order Request status 'Submit'                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Submited"                                                 |
|                                 |   | 2. Doc Adhoc Order Request tidak dapat di edit / update / ubah                           |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Mensubmit doc Adhoc Order Request dari Draft agar dapat di proses ke flow selanjutnya    |
+---------------------------------+---+------------------------------------------------------------------------------------------+


Validate Adhoc Order Request
''''''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approve doc Adhoc Order Request                                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | Isi Doc sudah sesuai dengan kebutuhan system                                             |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Validate","Print Adhoc","Create Quotation" Form Adhoc Order status Approve       |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Status doc berubah menjadi "Done"                                                     |
|                                 |   | 2. Doc Adhoc sudah selesai di proses                                                     |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Pop Up Message Warning                                                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Menvalidate doc adhoc order request, menandakan doc adhoc sudah selesai di proses        |
+---------------------------------+---+------------------------------------------------------------------------------------------+



Print Adhoc Order Request
'''''''''''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approve doc Adhoc Order Request                                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | -                                                                                        |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Print Adhoc Order Request"                                                       |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | Muncul pada display Print Output yang dapat di cetak                                     |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Error Pada Layar                                                                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Action untuk print adhoc order request yang sudah di approve pada sistem                 |
+---------------------------------+---+------------------------------------------------------------------------------------------+



Create Quotation
''''''''''''''''

+---------------------------------+---+------------------------------------------------------------------------------------------+
| Flow Sebelumnya                 | : | Approve doc Adhoc Order Request                                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Validasi                        | : | 1.Isi Doc sudah sesuai dengan kebutuhan system                                           |
|                                 |   | 2.Sudah adanya doc Work Order yang sudah terbentuk dari adhoc                            |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Interface                       | : | Tombol "Create Quotation"                                                                |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Sukses              | : | 1. Terbentuk doc draft quotation                                                         |
|                                 |   | 2. Akan di arahkan ke form draft quotation                                               |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Jika Action Gagal               | : | Muncul Error Pada Layar                                                                  |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| User                            | : | Sales / Admin Support                                                                    |
+---------------------------------+---+------------------------------------------------------------------------------------------+
| Deskripsi                       | : | Action untuk membuat draft quotation dari adhoc                                          |
+---------------------------------+---+------------------------------------------------------------------------------------------+
.. _pages_adhoc_interface:

Tampilan / Interface
--------------------

.. _pages_adhoc_form_adhoc_order_request:

Form Adhoc Order Request
''''''''''''''''''''''''

.. image:: /img/adh-form.png



Penjelasan Field:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Name                  | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | Customer              | Ya            | Nama / Data Customer, nama perusahaan                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Attention             | Ya            | Nama Orang yang dituju untuk penawaran                                                   |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | Customer Ref          | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | Sales                 | Ya            | Nama sales                                                                               |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|6  | Due Date              | Ya            | Batas tanggal                                                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|7  | Customer Site         | Tidak         | Lokasi Pelanggan                                                                         |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|8  | Cust Ref No           | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|9  | Sales Group           | Ya            | Kelompok dari sales                                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|10 | Detail Item           | Ya            | List yang berisi detail dari item                                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|11 | Work Order            | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|12 | Term Of Payment       | Ya            | Jangka waktu pembayaran                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|13 | Scope Of Work         | Ya            | Lingkup pekerjaan                                                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|14 | Term Condition        | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|15 | Notes                 | Tidak         | Catatan                                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


Pada form tersebut terdapat **5 Tab**, yaitu :

.. _pages_adhoc_detail_item:

Detail Item
```````````

Detail item merupakan Item yang menjadi master pengerjaan atau permintaan customer yang harus di input oleh user untuk mendefinisikan kebutuhan product atau pengerjaan customer, 



.. image:: /img/adh-detail-item.png

(Gambar Detail Item - Form / Detail)


Field yang ada pada **Detail Item**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Product               | Ya            | Item yang akan ditawarkan                                                                |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | Description           | Tidak         | Deskripsi item yang ditawarkan                                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Qty                   | Ya            | Banyaknya item                                                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | UOM                   | Ya            | Satuan Pengukuran dari unit                                                              |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | DATA MATERIAL         | Ya            | Berisi list material                                                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+



.. _pages_adhoc_data_material:

DATA MATERIAL
+++++++++++++

Data Material merupakan detail dari Item yang telah dipilih, biasanya data material adalah penjelasan lebih detail apa saja yang dibutuhkan dalam melakukan pekerjaan atau memasang product, semua dapat di detailkan satu persatu di data material



.. image:: /img/adh-detail-item-material.png

(Gambar Date Material - Form / Detail)


Field yang ada pada **Data Material**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Product               | Ya            | Item yang akan ditawarkan                                                                |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | Description           | Tidak         | Deskripsi item yang ditawarkan                                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Qty                   | Ya            | Banyaknya item                                                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | UOM                   | Ya            | Satuan Pengukuran dari unit                                                              |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


.. _pages_adhoc_work_order:

Work Order
``````````

Work Order merupakan doc lanjutan dari adhoc order request yang sudah di approve, dalam hal ini adhoc order request dapat memiliki lebih dari satu doc work order, work order dibuat untuk melakukan pekerjaan yang telah dijelaskan di adhoc order request



.. image:: /img/adh-work-order.png

(Gambar Work Order - Form / Detail)


Field yang ada pada **Work Order**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Request No            | Ya            | Nomor permintaan                                                                         |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | SPK No                | Ya            | Nomor surat perintah kerja                                                               |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Work Location         | Ya            | Lokasi kerja                                                                             |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | Internal Handler Loc  | Ya            |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | Customer              | Ya            | Nama / Data Customer, nama perusahaan                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|6  | Status                | Ya            | Status                                                                                   |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


.. _pages_adhoc_term_of_payment:

Term Of Payment
```````````````

Term Of Payment merupakan kondisi atau cara pembayaran yang akan dilakukan oleh customer dalam permintaan pekerjaan atau product dimana dalam hal ini dalam pembuatan adhoc order request.



.. image:: /img/adh-term-of-payment.png

(Gambar Term Of Payment - Form / Detail)


Field yang ada pada **Term Of Payment**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Term Of Payment       | Ya            | Jangka waktu pembayaran                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


.. _pages_adhoc_scope_of_work:

Scope Of Work
`````````````

Scope Of Work merupakan batasan-batasan dalam melakukan pekerjaan yang dilakukan oleh perusahaan atau oleh customer, dimana dalam hal ini dibutuhkan untuk menjelaskan pekerjaan dan tanggung jawab masing masing



.. image:: /img/adh-scope-of-work.png

(Gambar Scope Of Work - Form / Detail)


Field yang ada pada **Scope Of Work**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Scope Of Work         | Tidak         | Lingkup pekerjaan                                                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


.. _pages_adhoc_term_condition:

Term Condition
``````````````

Term Condition merupakan penjelasan kondisi kondisi yang ada di dalam permintaan customer dalam mengerjakan kerjaan atau pembelian product dan juga informasi-informasi tambahan yang harus di ketahui sebagai dasar pengerjaan 



.. image:: /img/adh-term-condition.png

(Gambar Term Condition - Form / Detail)


Field yang ada pada **Term Condition**:


+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Term Condition        | Tidak         |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+