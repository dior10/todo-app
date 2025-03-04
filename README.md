Link Github: https://github.com/dior10/todo-app.git

Todo App adalah aplikasi berbasis Node.js, Express.js, dan MySQL, yang menggunakan JSON Web Token (JWT) untuk validasi pengguna. Database yang digunakan adalah MySQL, yang harus dikonfigurasi terlebih dahulu di file .env. Untuk menjalankan aplikasi secara lokal, pengguna harus meng-clone repositori dari GitHub, masuk ke direktori proyek, menginstal dependensi dengan npm install, dan menjalankan server dengan npm start.

Fitur utama aplikasi ini meliputi autentikasi pengguna dengan bcrypt, manajemen tugas (tambah, lihat, edit, hapus), serta keamanan melalui hashing password dan middleware JWT. Bootstrap digunakan untuk membuat tampilan antarmuka yang responsif.

Aplikasi ini menyediakan beberapa API endpoint, termasuk autentikasi pengguna (register dan login) serta pengelolaan tugas (tambah, lihat, edit, hapus) yang memerlukan autentikasi JWT. Struktur proyek mencakup berbagai folder untuk mengorganisir file statis, template, routing, logika bisnis, model database, middleware, dan file konfigurasi utama.

Todo App adalah aplikasi berbasis Node.js, Express.js, dan MySQL, yang dilengkapi dengan validasi menggunakan JSON Web Token (JWT). Untuk menjalankan aplikasi ini, pengguna harus menginstal Node.js dan MySQL.

Konfigurasi Database
Untuk mengatur database, ikuti langkah-langkah berikut:

Pastikan MySQL telah berjalan di komputer, bisa menggunakan aplikasi seperti phpMyAdmin atau MySQL Workbench.
Buat database baru dengan nama uts.
Tambahkan file .env di direktori utama proyek dan isikan konfigurasi berikut:
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=uts
JWT_SECRET=0b523a169206db0b073c5b94bc3b9e94b42f8a448e42aa494c39af7ac9fb782564b55eae37048d795270ce98ccd697768e10557dc676d16472c70f0b51221dcbdd3ac164b6349a8fb526a0d08b7b565f49a48462c4578790f07d38d65519fb26ea5111db381041f1b94f0fe131816343c25fc7bd20d6403d36f3a6a9a55906209304ba0c30aad0aa5e6fbc1104cf56b5642f5328681db395dd28b2d2b82e19ef8d919c3cebdc47d24cfb97e7a14ff9cdc95e51aff9661fe52230fadd974ee863fea25e1f68a73ba688889997f0dcf04919df4264d924403d93327e19161aba184323382df562ae11ed8193a6236658c2276d1542c3d2c5480fc691cdf34776ea
PORT=3000
Menjalankan Proyek Secara Lokal
Untuk menjalankan aplikasi ini di komputer lokal, lakukan langkah-langkah berikut:

Clone repositori dengan perintah:
git clone https://github.com/Edbert395/utsweb.git
Masuk ke direktori proyek:
cd utsweb
Instal dependensi yang diperlukan:
npm install
Jalankan server dengan perintah:
npm start
Akses aplikasi melalui browser di http://localhost:3000
Fitur Utama
Aplikasi ini memiliki beberapa fitur utama, di antaranya:

1. Autentikasi Pengguna

Registrasi dan login dengan password yang dienkripsi menggunakan bcrypt.
2. Manajemen Tugas

Menambahkan tugas baru
Melihat daftar tugas berdasarkan pengguna
Mengedit tugas yang sudah ada
Menghapus tugas
3. Keamanan

Middleware untuk melindungi rute menggunakan JWT.
Hash password dengan bcrypt.
4. Antarmuka Responsif

Menggunakan Bootstrap untuk tampilan yang responsif.
API Endpoints
Aplikasi ini menyediakan beberapa endpoint untuk keperluan autentikasi dan manajemen tugas, yaitu:

Autentikasi

POST /api/auth/register → Mendaftarkan pengguna baru
POST /api/auth/login → Login dan mendapatkan token JWT
Tugas (Memerlukan Autentikasi JWT)

POST /api/tasks → Menambahkan tugas baru
GET /api/tasks → Mendapatkan semua tugas milik pengguna
PUT /api/tasks/:id → Memperbarui tugas berdasarkan ID
DELETE /api/tasks/:id → Menghapus tugas berdasarkan ID
Struktur Proyek
Struktur direktori dalam proyek ini adalah sebagai berikut:

/utsweb
│-- /public           # File statis (CSS, JS, Images)
│-- /views            # Template EJS
│-- /routes           # Routing aplikasi
│-- /controllers      # Logika bisnis
│-- /models           # Model database
│-- /middlewares      # Middleware autentikasi
│-- .env              # Konfigurasi lingkungan
│-- server.js         # Entry point aplikasi
│-- package.json      # Dependensi proyek
