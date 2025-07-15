
## 📆 Create a Virtual Environment

Pertama-tama, buat virtual environment dan install semua dependencies yang diperlukan.

```bash
# Membuat virtual environment
python -m venv env
source env/bin/activate  # Untuk Linux/macOS
env\Scripts\activate  # Untuk Windows
```

Mengecek Dependecies yang telah terinstall
```bash
pip list
```
Tampilan Output
```bash
Package Version
------- -------
pip     24.2
```

Membuat File yang berisi depencies yanng telah terinstal
```bash
pip freeze > requirements.txt 
```
Perintah pip freeze > requirements.txt digunakan untuk membuat file requirements.txt yang berisi daftar semua dependensi Python beserta versi yang terpasang di dalam lingkungan virtual (virtual environment)

- pip: Merupakan manajer paket untuk Python, yang digunakan untuk menginstal dan mengelola paket (library) Python.
- freeze: Opsi freeze digunakan untuk menghasilkan daftar paket yang terpasang di lingkungan Python, lengkap dengan versi spesifiknya. Hasilnya adalah output yang menunjukkan paket dan versinya dalam format yang dapat digunakan untuk instalasi ulang dengan perintah pip install.

Misalnya, jika di dalam lingkungan Python Anda ada paket numpy versi 1.21.0, maka perintah pip freeze akan mengeluarkan output seperti ini:
```bash
numpy==1.21.0

```


## 📆 Install Dependencies

```bash
pip install django pillow pypdf2
```

### Penjelasan Perintah

Penjelasan Perintah:
- django: framework web Python yang populer untuk membangun aplikasi web. Django menyediakan struktur dan alat untuk membangun aplikasi web yang cepat dan efisien, dengan banyak fitur seperti manajemen basis data, autentikasi pengguna, dan lainnya.
- pip: Merupakan manajer paket Python yang digunakan untuk menginstal pustaka pihak ketiga.
- install: Merupakan perintah untuk menginstal pustaka atau paket tertentu.
- Pillow dan PyPDF2: Merupakan nama-nama paket yang akan diinstal. Kamu dapat menginstal lebih dari satu paket dalam satu perintah, cukup pisahkan nama-nama paket dengan spasi, seperti pada contoh ini.

Perintah pip install Pillow PyPDF2 digunakan untuk menginstal dua paket Python, yaitu Pillow dan PyPDF2. Berikut adalah penjelasan detail mengenai kedua paket tersebut dan perintah instalasinya:

#### 1. Pillow
Pillow adalah pustaka (library) Python yang digunakan untuk memproses gambar. Pillow adalah fork dari Python Imaging Library (PIL), yang sudah tidak lagi dipelihara. Pillow menyediakan berbagai fungsi untuk membuka, memodifikasi, dan menyimpan gambar dalam berbagai format, seperti JPEG, PNG, GIF, BMP, TIFF, dll. Dengan Pillow, kamu dapat melakukan operasi seperti:
- Mengubah ukuran gambar
- Memotong gambar
- Mengonversi format gambar
- Mengubah warna dan saturasi gambar
- Menambahkan teks atau elemen grafis ke gambar
- Melakukan manipulasi gambar lainnya (filter, efek, dll.).

Cara Install Pillow:
Dengan menjalankan perintah pip install Pillow, pip akan mengunduh dan menginstal pustaka Pillow pada lingkungan Python yang aktif. Setelah instalasi selesai, kamu dapat mengimpor dan menggunakan Pillow di skrip Python dengan cara berikut:

```bash
from PIL import Image

# Membuka gambar
image = Image.open('gambar.jpg')

# Menampilkan gambar
image.show()
```
#### 2. PyPDF2
PyPDF2 adalah pustaka Python yang digunakan untuk memanipulasi file PDF. Dengan PyPDF2, kamu dapat:
- Membaca, menggabungkan, memisahkan, atau memodifikasi file PDF
- Mengambil metadata file PDF (seperti judul, penulis, dan banyak lagi)
- Memutar, memotong, atau mengonversi halaman PDF
- Menggabungkan beberapa file PDF menjadi satu
- Menambahkan atau menghapus halaman dari file PDF
- Membaca teks dari file PDF

Cara Install PyPDF2:
Perintah pip install PyPDF2 akan mengunduh dan menginstal pustaka PyPDF2 ke lingkungan Python yang aktif. Setelah instalasi, kamu dapat menggunakannya untuk memanipulasi file PDF dengan cara berikut:

```bash
import PyPDF2

# Membuka file PDF
with open('file.pdf', 'rb') as file:
    reader = PyPDF2.PdfReader(file)
    
    # Mengambil jumlah halaman
    print(len(reader.pages))

    # Mengambil teks dari halaman pertama
    page = reader.pages[0]
    print(page.extract_text())
```

### 📆 Hasil Akhir
Mengecek Dependecies yang telah terinstall
```bash
pip list
```
Tampilan Output
```bash
Package Version
------- -------
asgiref  3.8.1
Django   5.2.2
pillow   11.2.1
pip      24.2
PyPDF2   3.0.1
sqlparse 0.5.3
```

### 📆 Mengupdate File yang berisi depencies yang telah terinstal
```bash
pip freeze > requirements.txt 
```
Tampilan Output
```bash
asgiref==3.8.1
Django==5.2.2
pillow==11.2.1
PyPDF2==3.0.1
sqlparse==0.5.3
```