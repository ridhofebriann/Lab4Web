# Lab4Web
# Praktikum 4: CSS Layout
### NAMA : M. Ridho Febrian
### NIM : 312410500
### KELAS : TI.24.A5

## 📍LANGKAH - LANGKAH PRAKTIKUM

### 1. MEMBUAT DOKUMEN HTML
Persiapan membuat dokumen HTML dengan nama file `lab4_box.html` seperti berikut.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Box Element</title>
  </head>
  <body>
    <header>
      <h1>Box Element</h1>
    </header>
  </body>
</html>
```
### Membuat Box Element
```html
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
</section>
```
### CSS Float Property
```css
<style>
div {
float:left;
padding: 10px;
}
.div1 {
background: red;
}
.div2 {
background: yellow;
}
.div3 {
background: green;
}
</style>
```
### Mengatur Clearfix Element
```html
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
<div class="div4">Div 4</div>
</section>
```
```css
.div4 {
background-color: blue;
clear: left;
float: none;
}
```
**Tampilan**
<img src="membuat box and clearfix element.png" width="700">


### Membuat Layout Web Sederhana

Buat folder baru  `lab4_layout`, di dalamnya buat dua file:

`home.html`

`style.css`

**berikut isi file home.html:**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div id="container">
      <header>
        <h1>Layout Sederhana</h1>
      </header>
      <nav>
        <a href="home.html" class="active">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html">About</a>
        <a href="kontak.html">Kontak</a>
      </nav>
      <section id="hero"></section>
      <section id="wrapper">
        <section id="main"></section>
        <aside id="sidebar"></aside>
      </section>
      <footer>
        <p>&copy; 2021 - Universitas Pelita Bangsa</p>
      </footer>
    </div>
  </body>
</html>
```
**Tampilan**
<img src="layout sederhana.png" width="700">


**berikut style.css:**
```css
/* import google font */
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap");
/* Reset CSS */
* {
  margin: 0;
  padding: 0;
}
body {
  line-height: 1;
  font-size: 100%;
  font-family: "Open Sans", sans-serif;
  color: #5a5a5a;
}
#container {
  width: 980px;
  margin: 0 auto;
  box-shadow: 0 0 1em #cccccc;
}
/* header */
header {
  padding: 20px;
}
header h1 {
  margin: 20px 10px;
  color: #b5b5b5;
}
```
**Membuat Navigasi**
```css
/* navigasi */
nav {
display: block;
background-color: #1f5faa;
}
nav a {
padding: 15px 30px;
display: inline-block;
color: #ffffff;
font-size: 14px;
text-decoration: none;
font-weight: bold;
}
nav a.active,
nav a:hover {
background-color: #2b83ea;
}
```
**Tampilan**
<img src="navigasi layout sederhana.png" width="700">

**Membuat Hero Panel dan Sidebar**
```html
<section id="hero">
  <h1>Hello World!</h1>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo
    fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
    nec pretium nunc pretium ac.
  </p>
  <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
**tambahkan css**
```css
/* Hero Panel */
#hero {
  background-color: #e4e4e5;
  padding: 50px 20px;
  margin-bottom: 20px;
}
#hero h1 {
  margin-bottom: 20px;
  font-size: 35px;
}
#hero p {
  margin-bottom: 20px;
  font-size: 18px;
  line-height: 25px;
}
```
**Mengatur Layout Main dan Sidebar**
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
```css
/* main content */
#wrapper {
  margin: 0;
}
#main {
  float: left;
  width: 640px;
  padding: 20px;
}
/* sidebar area */
#sidebar {
  float: left;
  width: 260px;
  padding: 20px;
}
```

**Membuat Sidebar Widget**
Kemudian selanjutnya menambahkan element lain dalam sidebar.
```html
<aside id="sidebar">
  <div class="widget-box">
    <h3 class="title">Widget Header</h3>
    <ul>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
    </ul>
  </div>
  <div class="widget-box">
    <h3 class="title">Widget Text</h3>
    <p>
      Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.
      Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
      pharetra est nunc, nec pretium nunc pretium ac.
    </p>
  </div>
</aside>
```

kemudiann tambahkan css
```css
/* widget */
.widget-box {
  border: 1px solid #eee;
  margin-bottom: 20px;
}
.widget-box .title {
  padding: 10px 16px;
  background-color: #428bca;
  color: #fff;
}
.widget-box ul {
  list-style-type: none;
}
.widget-box li {
  border-bottom: 1px solid #eee;
}
.widget-box li a {
  padding: 10px 16px;
  color: #333;
  display: block;
  text-decoration: none;
}
.widget-box li:hover a {
  background-color: #eee;
}
.widget-box p {
  padding: 15px;
  line-height: 25px;
}
```
**Tampilan**
<img src="membuat panel dan sidebar.png" width="700">

**Mengatur Footer**
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
```css
/* footer */
footer {
  clear: both;
  background-color: #1d1d1d;
  padding: 20px;
  color: #eee;
}
```

**Menambahkan Elemen lainnya pada Main Content**
```html
<section id="main">
  <div class="row">
    <div class="box">
      <img
        src="https://dummyimage.com/120/db7d25/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
    <div class="box">
      <img
        src="https://dummyimage.com/120/3e73e6/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
    <div class="box">
      <img
        src="https://dummyimage.com/120/71e6d4/fff.png"
        alt=""
        class="image-circle"
      />
      <h3>Heading</h3>
      <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
      <a href="#" class="btn btn-default">View detail</a>
    </div>
  </div>
</section>
```
dan tambahkan css

```css
/* box */
.box {
  display: block;
  float: left;
  width: 33.333333%;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  padding: 0 10px;
  text-align: center;
}
.box h3 {
  margin: 15px 0;
}
.box p {
  line-height: 20px;
  font-size: 14px;
  margin-bottom: 15px;
}
box img {
  border: 0;
  vertical-align: middle;
}
.image-circle {
  border-radius: 50%;
}
.row {
  margin: 0 -10px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.row:after,
.row:before,
.entry:after,
.entry:before {
  content: "";
  display: table;
}
.row:after,
.entry:after {
  clear: both;
}
```

**Tampilan**
<img src="main content.png" width="700">

**Menambahkan Content Artikel**
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
```html
<hr class="divider" />
<article class="entry">
  <h2>First featurette heading.</h2>
  <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" />
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo
    fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
    nec pretium nunc pretium ac.
  </p>
</article>
<hr class="divider" />
<article class="entry">
  <h2>First featurette heading.</h2>
  <img
    src="https://dummyimage.com/150/7b8a70/fff.png"
    alt=""
    class="right-img"
  />
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo
    fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc,
    nec pretium nunc pretium ac.
  </p>
</article>
```
kemudian tambahkan css
```css
.divider {
  border: 0;
  border-top: 1px solid #eeeeee;
  margin: 40px 0;
}
/* entry */
.entry {
  margin: 15px 0;
}
.entry h2 {
  margin-bottom: 20px;
}
.entry p {
  line-height: 25px;
}
.entry img {
  float: left;
  border-radius: 5px;
  margin-right: 15px;
}
.entry .right-img {
  float: right;
}
```

**Tampilan**
<img src="content artikel.png" width="700">


### Pertanyaan dan Tugas

1. Tambahkan Layout untuk menu About
   
=> buat single layout yang berisi deskripsi, portfolio, dll

2. Tambahkan layout untuk menu Contact

=> yang berisi form isian: nama, email, message, dll

### jawab

**1. about.html**
   langkah awal membuat file baru about.html
   
   Simpan file ini di dalam folder:

Lab4Web/lab4_layout/about.html
isi kode :
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>About - Layout Sederhana</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div id="container">
    <!-- HEADER -->
    <header>
      <h1>Tentang Kami</h1>
    </header>

    <!-- NAVIGATION -->
    <nav>
      <a href="home.html">Home</a>
      <a href="about.html" class="active">About</a>
      <a href="contact.html">Contact</a>
    </nav>

    <!-- MAIN CONTENT -->
    <section id="wrapper">
      <section id="main">
        <h2>Deskripsi Singkat</h2>
        <p>
          Website ini dibuat sebagai latihan pada <strong>Praktikum 4 CSS Layout</strong>,
          dengan tujuan memahami konsep dasar layout menggunakan <em>float</em>, <em>box model</em>,
          dan <em>clearfix</em>. Halaman ini berfungsi untuk menjelaskan latar belakang, tujuan,
          serta informasi singkat mengenai pembuat atau tim pengembang website.
        </p>

        <p>
          Kami merupakan mahasiswa <strong>Teknik Informatika Universitas Pelita Bangsa</strong>
          yang sedang mempelajari dasar-dasar pemrograman web. Dalam praktikum ini, kami belajar
          membangun struktur layout sederhana yang terdiri dari <em>header</em>, <em>navigasi</em>,
          <em>konten utama</em>, <em>sidebar</em>, dan <em>footer</em> dengan tampilan yang seragam.
        </p>

        <h2>Tujuan dan Manfaat</h2>
        <ul>
          <li>Melatih kemampuan menggunakan CSS untuk mengatur tata letak (layout).</li>
          <li>Mengenal konsep float dan pengaruhnya pada struktur elemen.</li>
          <li>Membuat halaman web dengan tampilan yang konsisten antar halaman.</li>
        </ul>

        <h2>Portfolio / Proyek</h2>
        <div class="row">
          <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
            <h3>Proyek Web Profil</h3>
            <p>Website profil pribadi menggunakan HTML dan CSS murni.</p>
          </div>
          <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
            <h3>Mini Blog</h3>
            <p>Latihan membuat halaman artikel dengan struktur blog sederhana.</p>
          </div>
          <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
            <h3>Desain UI Layout</h3>
            <p>Eksperimen pembuatan layout dengan kombinasi warna dan grid.</p>
          </div>
        </div>

      </section>

      <!-- SIDEBAR -->
      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Informasi Tambahan</h3>
          <p>
            Praktikum ini menggunakan HTML5 dan CSS3 dengan fokus pada pembuatan
            struktur layout statis. Semua halaman menggunakan stylesheet yang sama
            agar tampilan web terlihat seragam.
          </p>
        </div>

        <div class="widget-box">
          <h3 class="title">Kontak Singkat</h3>
          <p>Email: <a href="mailto:ridho@contoh.com">ridho@contoh.com</a></p>
          <p>Instagram: @m.ridho</p>
        </div>
      </aside>
    </section>

    <!-- FOOTER -->
    <footer>
      <p>&copy; 2025 - Universitas Pelita Bangsa | Praktikum 4 CSS Layout</p>
    </footer>
  </div>
</body>
</html>
```
### Penjelasan Struktur

| Bagian           | Penjelasan                                                                                         |
| ---------------- | -------------------------------------------------------------------------------------------------- |
| **Header**       | Menampilkan judul halaman “Tentang Kami”.                                                          |
| **Nav**          | Navigasi antar halaman (Home, About, Contact) — class `active` menunjukkan halaman aktif.          |
| **Section Main** | Berisi deskripsi lengkap, tujuan praktikum, dan contoh portfolio/proyek yang pernah dibuat.        |
| **Row & Box**    | Menampilkan 3 kolom portfolio menggunakan `float` (class `.box` dan `.row` diatur di `style.css`). |
| **Sidebar**      | Berisi informasi tambahan dan kontak singkat pembuat situs.                                        |
| **Footer**       | Menampilkan hak cipta dan tahun pembuatan.                                                         |

saya tambahkan css :
```css
/* Biar seluruh konten tidak terlalu nempel ke tepi */
body {
  font-family: 'Open Sans', sans-serif;
  color: #444;
  background: #f8f9fa;
  line-height: 1.6;
}

/* Container utama */
#container {
  width: 960px;
  margin: 30px auto;
  background: #fff;
  box-shadow: 0 0 15px rgba(0,0,0,0.1);
  border-radius: 8px;
  overflow: hidden; /* biar float nggak keluar */
}

/* Header */
header {
  padding: 25px 30px 10px;
  border-bottom: 3px solid #1f5faa;
}
header h1 {
  color: #2d2d2d;
  font-size: 28px;
  margin: 0;
}

/* Navigasi */
nav {
  background: #1f5faa;
  text-align: center;
}
nav a {
  color: #fff;
  display: inline-block;
  padding: 12px 25px;
  text-decoration: none;
  font-weight: 600;
  transition: background 0.3s;
}
nav a:hover,
nav a.active {
  background: #2b83ea;
}

/* Main layout */
#wrapper {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  padding: 25px 30px;
}

/* Kolom utama */
#main {
  flex: 2.3;
}

/* Sidebar */
#sidebar {
  flex: 1;
}

/* Judul bagian */
#main h2 {
  margin-top: 0;
  color: #1f5faa;
  border-bottom: 2px solid #eee;
  padding-bottom: 5px;
  margin-bottom: 10px;
}

/* Paragraf */
#main p {
  margin-bottom: 15px;
  text-align: justify;
}

/* List (Tujuan & Manfaat) */
#main ul {
  margin-left: 25px;
  margin-bottom: 20px;
}

/* Box (Portfolio) */
.row {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}
.box {
  width: 30%;
  background: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 10px;
  text-align: center;
  padding: 15px;
  box-sizing: border-box;
}
.image-circle {
  border-radius: 50%;
  display: block;
  margin: 10px auto 15px;
}

/* Sidebar widgets */
.widget-box {
  border: 1px solid #ddd;
  border-radius: 8px;
  margin-bottom: 20px;
  background: #fafafa;
  padding: 10px 15px;
}
.widget-box .title {
  background: #2b83ea;
  color: white;
  font-weight: 600;
  padding: 8px 12px;
  border-radius: 5px;
  margin-bottom: 10px;
}
.widget-box a {
  color: #1f5faa;
  text-decoration: none;
}
.widget-box a:hover {
  text-decoration: underline;
}

/* Footer */
footer {
  background: #1d1d1d;
  color: #eee;
  text-align: center;
  padding: 15px 0;
  margin-top: 20px;
  font-size: 14px;
  border-top: 3px solid #2b83ea;
}
```

**Tampilan**
<img src="tampilan dan vscode list.png" width="700">

**2. contact.html**
langkah awal membuat file baru contact.html

   di simpan di folder:
   Lab4Web/lab4_layout/contact.html
isi kode:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Contact - Layout Sederhana</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div id="container">
    <!-- HEADER -->
    <header>
      <h1>Hubungi Kami</h1>
    </header>

    <!-- NAVIGATION -->
    <nav>
      <a href="home.html">Home</a>
      <a href="about.html">About</a>
      <a href="contact.html" class="active">Contact</a>
    </nav>

    <!-- MAIN CONTENT -->
    <section id="wrapper">
      <section id="main">
        <h2>Formulir Kontak</h2>
        <p>
          Jika Anda memiliki pertanyaan, saran, atau masukan terkait latihan ini, silakan
          kirimkan pesan melalui formulir di bawah. Kami akan berusaha memberikan tanggapan secepatnya.
        </p>

        <form action="#" method="post" id="contact-form">
          <div class="form-group">
            <label for="name">Nama Lengkap</label><br>
            <input type="text" id="name" name="name" placeholder="Masukkan nama Anda" required>
          </div>

          <div class="form-group">
            <label for="email">Email</label><br>
            <input type="email" id="email" name="email" placeholder="Masukkan email aktif" required>
          </div>

          <div class="form-group">
            <label for="message">Pesan</label><br>
            <textarea id="message" name="message" rows="6" placeholder="Tulis pesan Anda di sini..." required></textarea>
          </div>

          <button type="submit" class="btn-submit">Kirim Pesan</button>
        </form>
      </section>

      <!-- SIDEBAR -->
      <aside id="sidebar">
        <div class="widget-box">
          <h3 class="title">Informasi Kontak</h3>
          <p><strong>Alamat:</strong><br> Jl. Pendidikan No.45, Cikarang, Bekasi</p>
          <p><strong>Email:</strong><br> <a href="mailto:ridho@contoh.com">ridho@contoh.com</a></p>
          <p><strong>Telepon:</strong><br> +62 812-3456-7890</p>
        </div>

        <div class="widget-box">
          <h3 class="title">Media Sosial</h3>
          <p>Instagram: <a href="https://instagram.com/m.ridho" target="_blank">@m.ridho</a></p>
          <p>LinkedIn: <a href="#">linkedin.com/in/ridho</a></p>
        </div>
      </aside>
    </section>

    <!-- FOOTER -->
    <footer>
      <p>&copy; 2025 - Universitas Pelita Bangsa | Praktikum 4 CSS Layout</p>
    </footer>
  </div>
</body>
</html>
```
**saya tambahkan css**
```css
/* --- STYLING FORM KONTAK --- */
form {
  background: #f9f9f9;
  padding: 20px;
  border-radius: 8px;
  border: 1px solid #ddd;
}

.form-group {
  margin-bottom: 15px;
}

form label {
  font-weight: 600;
  color: #333;
}

form input[type="text"],
form input[type="email"],
form textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 14px;
  margin-top: 5px;
  box-sizing: border-box;
}

form textarea {
  resize: vertical;
}

.btn-submit {
  background: #1f5faa;
  color: #fff;
  font-weight: bold;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.3s;
}

.btn-submit:hover {
  background: #2b83ea;
}
```

### Penjelasan Struktur

| Bagian              | Fungsi                                                                                                |
| ------------------- | ----------------------------------------------------------------------------------------------------- |
| **Header**          | Menampilkan judul halaman “Hubungi Kami”.                                                             |
| **Navigasi**        | Tetap sama seperti halaman lain; class `active` di menu Contact.                                      |
| **Formulir Kontak** | Memakai `<form>` dengan input: Nama, Email, Pesan. Sudah ada atribut `required` untuk validasi dasar. |
| **Sidebar**         | Berisi alamat, email, telepon, dan link media sosial.                                                 |
| **Footer**          | Konsisten dengan halaman lain (warna hitam, teks putih).                                              |


