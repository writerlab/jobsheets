# Jobsheet 5
## Templates Bagian 2: Django Template Language

Bahasa template pada django terbagi menjadi 3:
#### 1. Substitusi variable: mencetak sebuah variable dari view
Bentuk umum: 

    {{ nama }}

Buka ```views.py```, tambahkan beberapa variable  didalam view ```buku()``` seperti berikut.
```python
def buku(request):
  template = "buku.html"

  books = ['Belajar Django 2.2.9', 'Belajar Python 3', 'Belajar Bootstrap']

  context = {
    'judul' : "data buku",
    'books' : books,
  } 

  return render(request, template, context)
```
buka ```buku.html``` dan ubah baris judul **DATA BUKU** dengan variable ```judul``` dari views ```buku()```.

```html
...
<body>
  
  <h1>{{ judul }}</h1>

</body>
...
```

Jalankan server dan lihat perubahannya.


### 2. Filter: Memodifikasi variable
Bentuk umum: 

    {{ nama|upper }}

Buka kembali ```buku.html``` dan tambahkan filter ```upper``` pada variable judul seperti berikut.

```html
...
<body>

  <h1>{{ judul|upper }}</h1>

</body>
```

Refresh/F5 halaman dan lihat perubahannya.

### 3. Tag: untuk logic, looping, dan lain-lain.
Bentuk umum: 

    { % tag %}

Buka kembali ```buku.html``` dan tambahkan baris berikut.

```html
...
<body>

  ...

  <ol>
    {% for buku in books %}
      <li>{{ buku }}</li>
    {% endfor %}
  </ol>

</body>
...
```

Tag ```for``` diatas digunakan untuk mengambil data ```books``` dari views ```buku()```.

Save dan refresh halaman. Lihat perubahannya.

---

**TERUSLAH MENGULANG SAMPAI MENDARAH DAGING, KAMU AKAN TERBIASA DAN BISA.**
