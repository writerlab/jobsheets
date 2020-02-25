# Jobsheet 4
## Membuat Apps
masuk ke folder projek ```perpus/```
```python
cd Desktop/perpus
```

buat apps: ```buku```
```python
django-admin startapp buku
```

buka projek dengan teks editor
```python
code .
```

daftarkan apps yang sudah dibuat di ```perpus/settings.py```
```python
...
INSTALLED_APPS = [
  ...
  'buku',
]
```

## Membuat Views Baru
buka file ```buku/views.py```. dan tambah beberapa syntax berikut.
```python
...
from django.http import HttpResponse

def buku(request):
  return HttpResponse('Halaman Buku')
```

buka file ```perpus/urls.py```. import modul views buku.
```python
...
from buku.views import buku

urlpatterns = [
  ...
  path('buku/', buku),
]
```

jalankan server
```python
python manage.py runserver
```

buka ```http://127.0.0.1:8000/buku``` di browser.

