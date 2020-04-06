# Jobsheet 2
**APLIKASI PERPUSTAKAAN** akan menjadi judul projek dalam menempuh materi ini. Judul projek ini bersifat lanjutan dan akan terus digunakan sampai materi selesai.

## Membuat Projek
Kita akan simpan projek di ```Desktop```.
Buka terminal dan masuk ke Desktop.

```bash
cd Desktop
```

Buatlah projek dengan nama ```perpus``` menggunakan ```django-admin```.

```bash
django-admin startproject perpus
```

## Menjalankan Projek
Masuk ke direktori projek.

```bash
cd perpus
```

Jalankan projek dengan perintah berikut.

```bash
python manage.py runserver
```

## Lihat di Browser
Buka alamat [http://127.0.0.1:8000](http://127.0.0.1:8000) di browser.

Sampai disini, projek sudah siap dibangun.

## Struktur Projek
Saat membuat projek dengan **django-admin startproject perpus**, maka django akan
membuat sebuah folder yang bernama **perpus**. Didalamnya akan terlihat seperti berikut.

```python
perpus/                       # project root
  |--- perpus/                # django root
  |      |--- __init__.py
  |      |--- settings.py
  |      |--- urls.py
  |      |--- wsgi.py
  |--- manage.py
```

Keterangan:
- Project root : direktori root projek yang dihasilkan dari django-admin startproject
- Django root : direktori untuk koneksi projek dengan django
- ```__init__.py``` : file yang memberitahu python bahwa direktori ini adalah package
- ```settings.py``` : file pengaturan/konfigurasi projek
- ```urls.py``` : file yang berisi pola URL
- ```wsgi.py``` : berfungsi untuk deployment projek yang akan melibatkan web server
 yang kompatibel dengan WSGI (Web Server Gateway Interface)
- ```manage.py``` : command-line untuk berinteraksi dengan projek