Link WEB : https://ffaawwaazz.github.io/WEB-Profil-Perusahaan/
# WEB-Profil-Perusahaan

Berikut adalah penjelasan kode HTML, CSS, dan JavaScript yang digunakan dalam proyek **NIKE Profile**:

---

## **1. Struktur HTML (`index.html`)**
HTML digunakan untuk menyusun struktur halaman web.

### **a. Bagian `<head>`**
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NIKE Profile</title>
```
- **`<meta charset="UTF-8">`** → Mendukung karakter internasional.
- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`** → Membuat tampilan responsif di berbagai perangkat.
- **`<title>NIKE Profile</title>`** → Menampilkan judul halaman di tab browser.

---

### **b. Bagian `<body>`**
Bagian utama halaman, yang terdiri dari **Header, Banner, About Us, Produk, dan Kontak**.

#### **1) Header (Navigasi)**
```html
<header>
    <div class="logo">NIKE</div>
    <nav>
        <a href="#about-us">About Us</a>
        <a href="#vision-mission">Vision & Mission</a>
        <a href="#contact">Contact</a>
    </nav>
</header>
```
- **`<header>`** → Bagian atas halaman yang berisi logo dan navigasi.
- **`<div class="logo">NIKE</div>`** → Menampilkan logo NIKE.
- **`<nav>`** → Menu navigasi dengan tautan ke bagian berbeda di halaman.

---

#### **2) Banner (Gambar Utama)**
```html
<div class="banner">
    <img src="NIKE banner.jpg" alt="NIKE Banner">
</div>
```
- **`<div class="banner">`** → Area untuk gambar utama.
- **`<img src="NIKE banner.jpg" alt="NIKE Banner">`** → Gambar banner dengan teks alternatif.

---

#### **3) Tentang NIKE (`About Us`)**
```html
<section id="about-us">
    <h2>About NIKE</h2>
    <p>Nike didirikan pada 1964 oleh Phil Knight dan Bill Bowerman...</p>
</section>
```
- **`<section>`** → Bagian terpisah yang membahas sejarah Nike.
- **`<h2>`** → Judul utama bagian ini.
- **`<p>`** → Paragraf penjelasan sejarah Nike.

---

#### **4) Informasi Produk**
```html
<div class="info-boxes">
    <div class="box">
        <img id="mainImage1" src="AR1 W.png" alt="Nike Air Force 1">
        <h3>Nike Air Force 1</h3>
        <p>Sepatu ikonik sejak 1982 dengan teknologi Air Cushion.</p>
        <div class="thumbnails">
            <img src="AR1 W.png" onclick="changeImage('mainImage1', 'AR1 W.png')">
            <img src="AR1 B.png" onclick="changeImage('mainImage1', 'AR1 B.png')">
        </div>
    </div>
</div>
```
- **`<div class="box">`** → Setiap produk ditampilkan dalam kotak.
- **`<img id="mainImage1" src="AR1 W.png">`** → Gambar utama produk.
- **Thumbnail interaktif:** Ketika gambar kecil diklik, gambar utama berubah.

---

#### **5) Bagian Kontak**
```html
<section id="contact">
    <h2>Contact Us</h2>
    <p>Email: media.relations@nike.com</p>
    <p>Phone: 001-803-65-6453</p>
</section>
```
- **Menampilkan informasi kontak perusahaan.**

---

#### **6) Footer**
```html
<footer>
    <p>&copy; 2025 NIKE. All Rights Reserved.</p>
</footer>
```
- **Menampilkan hak cipta di bagian bawah halaman.**

---

## **2. Gaya Tampilan CSS**
Kode CSS digunakan untuk memberikan tampilan yang menarik.

### **a. Pengaturan Global**
```css
body {
    font-family: Arial, sans-serif;
    background-color: #131921;
    color: #ffffff;
}
```
- **Menggunakan font Arial.**
- **Latar belakang hitam kebiruan (#131921).**
- **Teks berwarna putih.**

---

### **b. Header dan Navigasi**
```css
header {
    display: flex;
    justify-content: space-between;
    background: #232f3e;
    padding: 20px;
}
```
- **Menampilkan header secara horizontal (display: flex).**
- **Memberikan latar belakang biru tua.**
- **Menambahkan jarak (padding) agar terlihat lebih rapi.**

---

### **c. Banner**
```css
.banner img {
    width: 100%;
    max-height: 400px;
    object-fit: cover;
    border-radius: 8px;
}
```
- **Gambar memenuhi lebar layar.**
- **Maksimal tinggi 400px agar tidak terlalu besar.**
- **Gambar memiliki sudut melengkung (border-radius: 8px).**

---

### **d. Produk (Info Boxes)**
```css
.info-boxes {
    display: flex;
    justify-content: space-between;
}
.box {
    background: #37475a;
    padding: 20px;
    border-radius: 8px;
    text-align: center;
}
```
- **Menata produk secara horizontal (flexbox).**
- **Latar belakang abu-abu kebiruan (#37475a).**
- **Teks rata tengah.**
- **Gambar dan teks diberi jarak agar lebih enak dilihat.**

---

### **e. Thumbnail Interaktif**
```css
.thumbnails img {
    width: 50px;
    height: 50px;
    margin: 5px;
    cursor: pointer;
    border-radius: 5px;
    border: 2px solid transparent;
}
.thumbnails img:hover {
    border-color: #ffffff;
}
```
- **Ukuran kecil (50x50px) agar rapi.**
- **Efek hover (border putih muncul saat kursor menyentuh gambar).**

---

## **3. JavaScript (Interaktivitas)**
```html
<script>
    function changeImage(mainImageId, newImageSrc) {
        document.getElementById(mainImageId).src = newImageSrc;
    }
</script>
```
- **Fungsi `changeImage(mainImageId, newImageSrc)`**:
  - **Mengubah gambar utama sesuai thumbnail yang diklik.**
- **Contoh Pemanggilan:** 
  ```html
  <img src="AR1 W.png" onclick="changeImage('mainImage1', 'AR1 W.png')">
  ```
  - Jika gambar kecil diklik, gambar utama akan berubah.

---

## **Kesimpulan**
- **HTML** → Menyusun konten dan struktur halaman.
- **CSS** → Memberikan desain dan tampilan responsif.
- **JavaScript** → Menambahkan fitur interaktif, seperti mengganti gambar produk.

Itulah penjelasan kode proyek **NIKE Profile**. Jika ada yang ingin diperbaiki atau ditambahkan, beri tahu saya! 🚀
