# Jobsheet 5
## Templates Bagian 1

Atur direktori default Template. Buka file ```perpus/settings.py```.
Tambahkan ```'templates'``` kedalam list ```DIRS```.
```python
...
TEMPLATES = [
        ...
        'DIRS': ['templates'],
        ...
]
...
```

Buat folder ```templates/``` di root folder.
Didalam folder templates inilah dokumen-dokumen HTML disimpan.
```python
-perpus/
  |- buku/
  |- perpus/
  |- templates/ # folder templates harus satu level dengan yang lain
  |- manage.py
```

Buat file ```buku.html``` difolder ```templates/```. Contoh isinya seperti berikut.
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <title>PERPUSTAKAAN SMK NEGERI 4 TASIKMALAYA</title>
</head>
<body>
  
  <h1>DATA BUKU</h1>

</body>
</html>
```

Ubah Views ```buku()``` di file ```buku/views.py``` agar me-render dokumen HTML. Persis seperti berikut.
```python
from django.shortcuts import render

def buku(request):
  template = "buk.html"
  return render(request, template)
```

Jangan lupa *save* dan jalankan *server*-nya.
```python
python manage.py runserver
```

Buka [http://127.0.0.1:8000/buku](http://127.0.0.1:8000/buku).

### Belum selesai 😃
Silakan buat Views dan Template untuk menampilkan halaman:
- Penulis
- Penerbit
- Laporan

---

**TERUSLAH MENGULANG SAMPAI MENDARAH DAGING, KAMU AKAN TERBIASA DAN BISA.**