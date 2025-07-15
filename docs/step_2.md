## 📆 Setting Up a Django Project and Application

### 1. Membuat Project Django

Langkah - Langkah

```bash
django-admin startproject docmerge
```
Perintah ini akan menghasilkan direktori docmerge yang berisi struktur dasar proyek Django, seperti:

### Penjelasan Perintah
Perintah ini digunakan untuk membuat proyek Django baru. Berikut penjelasan rinciannya:
1. django-admin 
adalah alat baris perintah yang disediakan oleh Django untuk membantu dalam membuat dan mengelola proyek Django.
2. startproject 
adalah subkomando yang digunakan untuk membuat struktur direktori baru untuk proyek Django.
3. docmerge 
adalah nama proyek yang akan dibuat. Kamu bisa menggantinya dengan nama lain sesuai kebutuhan.

Perintah ini akan menghasilkan direktori docmerge yang berisi struktur dasar proyek Django, seperti:

```bash
docmerge/
    manage.py
    docmerge/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

### Penjelasan Direktori
1. manage.py 
adalah file yang digunakan untuk menjalankan berbagai perintah Django dari baris perintah.
2. Direktori kedua dengan nama yang sama (docmerge/) 
berisi file konfigurasi proyek seperti:
    - settings.py
    digunakan untuk menyimpan pengaturan (settings) proyek Django, seperti database, middleware, aplikasi yang terpasang, dan lainnya.
    - urls.py
    digunakan untuk  enyimpan konfigurasi routing URL untuk aplikasi Django.
    - asgi.py dan wsgi.py
    adalah file untuk menjalankan aplikasi Django pada server ASGI dan WSGI (masing-masing untuk aplikasi asynchronous dan synchronous).

### 2. Masuk ke Direktori Project
```bash
cd docmerge
```
Setelah proyek Django baru dibuat, kamu perlu masuk ke direktori proyek untuk mulai bekerja dengan file dan konfigurasi proyek tersebut.

### Penjelasan Perintah
- cd docmerge
adalah perintah untuk change directory yang digunakan untuk berpindah ke direktori yang sudah dibuat (dalam hal ini, direktori docmerge). Perintah ini akan memindahkan kamu ke dalam direktori docmerge, di mana kamu dapat mulai bekerja dengan pengaturan proyek Django.

### 3. Membuat Aplikasi Baru
```
python manage.py startapp merge
```

Perintah ini digunakan untuk membuat aplikasi baru di dalam proyek Django. Django memungkinkan kamu untuk membuat banyak aplikasi dalam satu proyek, yang masing-masing bertanggung jawab untuk bagian tertentu dari fungsionalitas aplikasi web.

### Penjelasan Perintah
1. python manage.py adalah cara untuk menjalankan perintah Django dari file manage.py yang sudah ada di direktori proyek.
2. startapp adalah subkomando yang digunakan untuk membuat aplikasi baru.
3. merge adalah nama aplikasi yang akan dibuat. Kamu bisa menggantinya dengan nama lain yang sesuai dengan konteks aplikasi yang sedang dibangun.

Perintah ini akan menghasilkan direktori baru dengan nama merge/ yang berisi struktur dasar aplikasi Django, seperti:

``` bash
merge/
    migrations
    __init__.py
    admin.py
    apps.py
    models.py
    tests.py
    views.py
```

Hasil Struktur Akhir

```
docmerge/
├── docmerge/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── merge/
│   ├── migrations/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── views.py
├── manage.py

```

### 4. Development Server --> runserver
Perintah 
```bash 
python manage.py runserver 
```
digunakan untuk menjalankan server pengembangan Django pada mesin lokal (localhost) untuk menguji aplikasi yang sedang dikembangkan. Berikut adalah penjelasan rinci mengenai perintah ini:

1. python
adalah interpreter Python yang digunakan untuk menjalankan program atau skrip Python. Perintah ini memberitahu sistem untuk menjalankan perintah Python menggunakan interpreter yang telah terpasang di sistem kamu.

2. manage.py
adalah sebuah file Python yang terdapat di direktori utama proyek Django. File ini adalah antarmuka baris perintah (CLI) yang digunakan untuk menjalankan berbagai tugas administratif dalam proyek Django. File ini memungkinkan kamu untuk menjalankan perintah terkait proyek Django, seperti membuat basis data, menjalankan server, membuat aplikasi baru, dan banyak tugas lainnya. Semua perintah yang dijalankan menggunakan manage.py biasanya berhubungan langsung dengan pengelolaan proyek Django.

3. runserver
runserver adalah perintah yang digunakan untuk menjalankan server pengembangan Django di localhost, sehingga kamu dapat mengakses aplikasi web yang sedang dikembangkan melalui browser. Server ini berguna untuk pengujian lokal dan pengembangan aplikasi secara langsung tanpa perlu mengonfigurasi server yang lebih kompleks (seperti Apache atau Nginx).


#### Proses yang terjadi saat menjalankan python manage.py runserver:
1. Memulai Server Pengembangan

    Ketika perintah ini dijalankan, Django akan memulai server pengembangan internal yang memungkinkan kamu untuk melihat aplikasi dalam browser web.

    Secara default, server ini berjalan pada port 8000 dan dapat diakses melalui URL: http://127.0.0.1:8000/ atau http://localhost:8000/.

2. Menampilkan Output di Terminal

    Setelah menjalankan perintah, terminal akan menampilkan informasi mengenai status server dan port yang sedang digunakan, serta alamat URL tempat server dapat diakses.

    Contoh output di terminal:
    ``` bash
    Starting development server at http://127.0.0.1:8000/
    Quit the server with CONTROL-C.
    ```

3. Mengakses Aplikasi di Browser

    Setelah server berjalan, buka browser dan masukkan URL http://127.0.0.1:8000/ (atau http://localhost:8000/).
    Kamu akan melihat halaman aplikasi Django yang sedang berjalan. Biasanya, jika belum ada pengaturan aplikasi lain, kamu akan melihat halaman default Django yang menampilkan pesan selamat datang.


### Penjelasan Direktori

- `__init__.py: Menandakan bahwa direktori ini adalah paket Python.
- admin.py: Digunakan untuk mendaftarkan model ke dalam antarmuka admin Django.
- apps.py: Menyimpan konfigurasi aplikasi yang digunakan oleh Django.
- models.py: Tempat untuk mendefinisikan model data yang berinteraksi dengan - database.
- tests.py: Digunakan untuk menulis pengujian untuk aplikasi.
- views.py: Tempat untuk mendefinisikan tampilan (views) yang menangani permintaan HTTP dan mengembalikan respons.


### Apa yang akan terjadi setelah langkah-langkah ini:
Struktur proyek Django yang dibuat memungkinkan kamu untuk memulai dengan pengembangan aplikasi Django, di mana kamu dapat menambahkan aplikasi tambahan, mengonfigurasi database, mendefinisikan URL dan views, serta mengelola model.

Aplikasi merge yang baru saja dibuat akan berfungsi sebagai bagian dari proyek Django, dan kamu dapat menambahkannya ke dalam pengaturan INSTALLED_APPS di settings.py untuk mengaktifkannya.