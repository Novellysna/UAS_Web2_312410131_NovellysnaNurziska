# 📚 UAS Pemrograman Web 2
# UAS_Web2_312410131_NovellysnaNurziska

# Aplikasi E-Library Berbasis REST API dan Single Page Application (SPA)

---

## Identitas Mahasiswa

**Nama** : Novellysna Nurziska
**NIM** : 312410131
**Mata Kuliah** : Pemrograman Web 2
**Dosen Pengampu** : .......................................
**Program Studi** : Teknik Informatika
**Universitas** : Universitas Pelita Bangsa

---

# Deskripsi Proyek

E-Library merupakan aplikasi perpustakaan sederhana yang dibangun menggunakan konsep **REST API** pada sisi backend dan **Single Page Application (SPA)** pada sisi frontend.

Backend dikembangkan menggunakan **CodeIgniter 4**, sedangkan frontend menggunakan **HTML, CSS, Bootstrap 5, dan JavaScript (Fetch API)**.

Seluruh proses pengolahan data dilakukan melalui REST API sehingga frontend dan backend terpisah (decoupled).

---

# Tujuan

Tujuan pembuatan aplikasi ini adalah:

* Menerapkan konsep REST API.
* Menerapkan konsep Single Page Application (SPA).
* Mengimplementasikan autentikasi menggunakan Bearer Token.
* Menghubungkan frontend dengan backend menggunakan Fetch API.
* Mengelola data perpustakaan secara CRUD.

---

# Teknologi yang Digunakan

## Backend

* PHP 8
* CodeIgniter 4
* REST API
* MySQL

## Frontend

* HTML5
* CSS3
* Bootstrap 5
* Bootstrap Icons
* JavaScript ES6
* Fetch API

## Database

* MySQL
* phpMyAdmin

---

# Fitur Aplikasi

## Login

Pengguna melakukan login menggunakan username dan password.

Jika berhasil maka sistem akan menghasilkan token yang disimpan pada Local Storage.

---

## Dashboard

Dashboard menampilkan halaman utama aplikasi beserta menu navigasi menuju setiap modul.

---

## Data Kategori

Fitur yang tersedia:

* Menampilkan seluruh kategori
* Menambah kategori
* Mengubah kategori
* Menghapus kategori

---

## Data Penulis

Fitur yang tersedia:

* Menampilkan seluruh penulis
* Menambah penulis
* Mengubah penulis
* Menghapus penulis

---

## Data Anggota

Fitur yang tersedia:

* Menampilkan seluruh anggota
* Menambah anggota
* Mengubah anggota
* Menghapus anggota

---

## Data Buku

Fitur yang tersedia:

* Menampilkan seluruh buku
* Menambah buku
* Mengubah buku
* Menghapus buku

---

# Struktur Folder

```
backend-api/
│
├── app/
│
├── public/
│
├── writable/
│
└── ...

frontend-spa/
│
├── assets/
│   ├── css/
│   │
│   └── js/
│
├── pages/
│
└── login.html
```

---

# Struktur Database

Database terdiri dari beberapa tabel:

* users
* kategori
* penulis
* anggota
* buku

Relasi utama:

* Buku memiliki satu kategori
* Buku memiliki satu penulis

---

# Endpoint REST API

## Login

```
POST /login
```

---

## Kategori

```
GET /kategori
GET /kategori/{id}
POST /kategori
PUT /kategori/{id}
DELETE /kategori/{id}
```

---

## Penulis

```
GET /penulis
GET /penulis/{id}
POST /penulis
PUT /penulis/{id}
DELETE /penulis/{id}
```

---

## Anggota

```
GET /anggota
GET /anggota/{id}
POST /anggota
PUT /anggota/{id}
DELETE /anggota/{id}
```

---

## Buku

```
GET /buku
GET /buku/{id}
POST /buku
PUT /buku/{id}
DELETE /buku/{id}
```

---

# Authentication

REST API menggunakan Bearer Token.

Contoh Header:

```
Authorization: Bearer xxxxxxxxxxxxxxxxx
```

Token diperoleh saat login dan disimpan pada Local Storage.

---

# Alur Sistem

1. User membuka halaman login.
2. User memasukkan username dan password.
3. Frontend mengirim request ke REST API.
4. Backend melakukan validasi.
5. Jika berhasil maka token dikirim ke frontend.
6. Token disimpan di Local Storage.
7. Setiap request CRUD akan membawa Authorization Bearer Token.
8. Backend memvalidasi token sebelum memberikan respon.

---

# Cara Menjalankan Project

## Backend

Masuk ke folder backend.

```
cd backend-api
```

Jalankan server.

```
php spark serve
```

Server berjalan pada

```
http://localhost:8080
```

---

## Frontend

Buka folder frontend menggunakan Visual Studio Code.

Jalankan menggunakan Live Server.

Contoh:

```
http://127.0.0.1:5500/frontend-spa/login.html
```

---

# Konfigurasi Frontend

Konfigurasi endpoint API terdapat pada file:

```
assets/js/config.js
```

Contoh:

```javascript
const CONFIG = {
    BASE_URL: "http://localhost:8080/",
    ENDPOINTS: {
        LOGIN: "login",
        KATEGORI: "kategori",
        PENULIS: "penulis",
        ANGGOTA: "anggota",
        BUKU: "buku"
    }
};
```

---

# Pengujian

Pengujian dilakukan terhadap setiap modul CRUD.

| No | Modul     | Hasil    |
| -- | --------- | -------- |
| 1  | Login     | Berhasil |
| 2  | Dashboard | Berhasil |
| 3  | Kategori  | Berhasil |
| 4  | Penulis   | Berhasil |
| 5  | Anggota   | Berhasil |
| 6  | Buku      | Berhasil |

---

# Screenshot

Tambahkan screenshot berikut:

* Halaman Login
* Dashboard
* Data Kategori
* Data Penulis
* Data Anggota
* Data Buku
* Tambah Data
* Edit Data
* Hapus Data

---

# Kelebihan Aplikasi

* Menggunakan REST API.
* Menggunakan konsep Single Page Application.
* Antarmuka sederhana dan mudah digunakan.
* Menggunakan autentikasi Bearer Token.
* CRUD seluruh data dilakukan melalui API.

---

# Kekurangan Aplikasi

* Belum terdapat fitur pencarian.
* Belum terdapat fitur pagination.
* Belum terdapat upload cover buku.
* Belum terdapat manajemen hak akses pengguna.

---

# Kesimpulan

Aplikasi E-Library berhasil dibangun menggunakan CodeIgniter 4 sebagai backend REST API dan HTML, Bootstrap, serta JavaScript sebagai frontend SPA. Seluruh proses CRUD dapat dilakukan melalui komunikasi API menggunakan Fetch API dan autentikasi Bearer Token sehingga aplikasi menjadi lebih terstruktur dan mudah dikembangkan di masa mendatang.

---

# Daftar Pustaka

1. Dokumentasi CodeIgniter 4
2. Dokumentasi Bootstrap 5
3. Dokumentasi JavaScript Fetch API
4. Dokumentasi PHP 8
5. Dokumentasi MySQL
