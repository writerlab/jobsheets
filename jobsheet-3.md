# Jobsheet 3
## Mengenal URLs dan Views
Buka projek menggunakan Text editor. Dalam *jobsheet* ini menggunakan [Visual Studio Code](https://code.visualstudio.com/) (Lihat persiapan kebutuhan di *Jobsheet 1*).

Buka terminal.
```bash
cd Desktop\perpus
```

```bash
code .
```

## Membuat Pola URL
Mulai menulis syntax sederhana dengan membuat pola URL.
Buka file ```urls.py``` difolder **perpus/urls.py** pada Text editor.

Buat pola URL baru, misal untuk mengakses halaman **buku/**.
```python
...
urlspatterns = [
  ...
  path('buku/', buku),
]
```

## Membuat View
Masih di file ```urls.py```. Buat view untuk menangani *request* dari URL **buku/** dengan membuat method **buku()**.

```python
...
from django.http import HttpResponse

def buku(request):
  return HttpResponse('Halaman Buku')
...
```

Kode lengkapnya seperti berikut.

```python
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse

def buku(request):
  return HttpResponse('Halaman Buku')

urlspatterns = [
  path('admin/', admin.site.urls),
  path('buku/', buku),
]
```

Jangan lupa **Save** dan jalankan *server*-nya.
```bash
python manage.py runserver
```

Cek di browser [http://127.0.0.1:8000/buku](http://127.0.0.1:8000/buku)

---

### Penting!
Pembuatan Views pada **jobsheet 3** ini bersifat sementara/sebatas pengenalan alur kerja sistem Django:

```Client request URL``` --> ```URL Conf``` --> ```Views``` ---> ```Client```

Di Jobsheet selanjutnya akan dibahas langkah pembuatan Views pada Apps yang kita buat didalam projek, artinya pembuatan Views terpisah dengan URL.