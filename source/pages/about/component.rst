Komponen Tampilan ERP
=====================

Tampilan Halaman Login
----------------------

Berikut ini adalah tampilan halaman Login ERP

.. figure:: /img/module/login/login.png
   :scale: 50%
   :alt: Tampilan Login


Panel-Panel Tampilan ERP
------------------------

Ketika user sudah berhasil login, maka user akan melihat halaman utama dari ERP. Berikut ini adalah tampilan halaman utama ERP Suprabakti Mandiri.

.. figure:: /img/module/component/main_view.png
   :scale: 50%
   :alt: Panel panel dalam Tampilan ERP



.. list-table:: Penjelasan Panel
   :widths: 15 30
   :header-rows: 1

   * - Nama Komponen
     - Penjelasan
   * - Panel Menu Utama
     - Berisi modul modul utama yang dapat diakses pada ERP
   * - Panel Menu Modul
     - Berisi menu menu sub modul yang dapat diakses pada ERP
   * - Panel Konen
     - Area untuk menampilkan konten, baik data, tabel, form, dll.
   * - Panel Action
     - Berisi tombol-tombol navigasi untuk action yang dapat dilakukan pada modul yang sedang di akses (misal: create, edit, delete, dll)
   * - Filter Input
     - Merupakan area yang dapat diketik yang berguna untuk melakukan pencarian suatu dokumen di ERP yang sedang di akses oleh user.

Jenis Konten
------------

Terdapat beberapa jenis konten yang akan biasa dijumpai pada ERP.

1. Tabel / List View
^^^^^^^^^^^^^^^^^^^^

Berikut ini merupakan contoh tampilan List View yang terdapat pada menu Customer.


.. figure:: /img/module/component/list_view.png
   :scale: 50%
   :alt: Salah Satu Contoh List View

2. Form / Form View
^^^^^^^^^^^^^^^^^^^

Berikut ini merupakan contoh salah satu tampilan Form View yang terdapat pada menu Customer.

.. figure:: /img/module/component/form_view.png
   :scale: 50%
   :alt: Salah Satu Contoh List View


.. list-table:: Penjelasan Komponen yang Terdapat Pada List View
   :widths: 15 30
   :header-rows: 1

   * - Nama
     - Penjelasan
   * - Field
     - Merupakan informasi attribut berserta isinya. (Contoh: Address : Jl. Danau Sunter Utara) artinya Kolom Address berisi "Jl. Danau Sunter Utara"
   * - Tabular
     - Merupakan panel yang berisi suatu sub konten (Sesuai dengan nama tabular).
   * - Next and Prev
     - Tombol Next dan Prev digunakan untuk melihat dokomen dengan nomor urut selanjut nya ataupun sebelumnya
   * - Switch View Mode
     - Tombol untuk mengganti mode tampilan baik List View, Form View, dll
   * - Log History
     - Merupakan panel yang berisi informasi catatan dari user lain maupun catatan perubahan dokumen. Panel ini dapat digunakan untuk mentracking apa saja yang dilakukan user tertentu terhadap suatu dokumen pada ERP.
   * - Document Followers
     - List user terkait dengan suatu dokumen.