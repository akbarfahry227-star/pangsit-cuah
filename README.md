# ​ Pangsit Cuahh

Situs katalog dan pemesanan online untuk brand makanan **Pangsit Cuahh**, dengan tampilan modern bergaya *neumorphism*, dibangun menggunakan **React**, **TailwindCSS**, dan **Firebase**, lalu di-*deploy* di **Netlify**.

**Live demo**: [https://dincth-aridin.netlify.app](https://dincth-aridin.netlify.app)

##  Teknologi

- **React 18** + **Vite**  
- **TailwindCSS 3**  
- **Firebase Web SDK v12** – Authentication (Google & Email/Password)  
- **Netlify** – Build & Deploy  

##  Fitur Utama

- Halaman **Login** (Google & Email/Password)  
- **Katalog Produk** lengkap dengan gambar dan harga  
- **Keranjang Belanja** multi-item dengan animasi halus (fade & slide)  
- **Checkout via WhatsApp** ke `0821-9169-8115` dengan pesan otomatis berisi daftar order, total, dan nama customer  
- Desain **neumorphism**: shadow lembut, rounded corners, dan efek hover yang menarik  

##  Daftar Produk

| Produk        | Harga      | Gambar         | Keterangan Gambar |
|---------------|-----------:|----------------|------------------|
| Pangsit Kuah  | Rp 15.000  | mi-pangsit.png | `object-contain`, `h-48` |
| Es Teh        | Rp 3.000   | es-teh.png     | `object-contain`, `h-60` |
| Es Jeruk      | Rp 5.000   | es-jeruk.png   | `object-contain`, `h-56` |
| Bakso         | Rp 12.000  | bakso.png      | `object-contain`, `h-48` |

##  Warna Tema

- **Utama**: `#D62828`  
- **Sekunder**: `#F77F00`  
- **Aksen**: `#FCBF49`  
- **Background**: `#FFF8F0`  
- **Teks**: `#3A3A3A`  

##  Struktur Proyek

```

/
├── public/
│   ├── mi-pangsit.png
│   ├── es-teh.png
│   ├── es-jeruk.png
│   ├── bakso.png
│   ├── background.jpg
│   └── logo-google.svg
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   ├── index.css
│   ├── firebase.js
│   └── components/
│       ├── Login.jsx
│       ├── ProductCard.jsx
│       └── Cart.jsx
├── index.html
├── tailwind.config.js
├── postcss.config.js
├── vite.config.js
└── netlify.toml

````

##  Instalasi & Penggunaan

1. Install dependencies:
   ```bash
   npm install
   ```

2. Jalankan development server:

   ```
   npm run dev
   ```

   Akses melalui browser di `http://localhost:5173`

3. Build untuk production:

   ```
   npm run build
   ```

   Hasil build akan tersimpan di folder `dist/`

## Deploy di Netlify

* **Build command**: `npm run build`
* **Publish directory**: `dist/`
* Konfigurasi dasar sudah tersedia di `netlify.toml`

## Setup Firebase

1. Tambahkan `firebaseConfig` kamu di `src/firebase.js`
2. Aktifkan **Google** dan **Email/Password** pada menu *Authentication → Sign-in method* di Firebase Console
3. Tambahkan domain lokal serta domain Netlify ke daftar Authorized domains

## Alur Penggunaan

1. User login (Google / Email & Password)
2. Produk ditambahkan ke keranjang
3. User mengatur jumlah item
4. Klik tombol **“Pesan via WhatsApp”**
5. WhatsApp akan terbuka dengan format pesan seperti berikut:

   ```
   Halo, saya mau pesan:
   - Pangsit Kuah x2 (Rp 30.000)
   - Es Teh x1 (Rp 3.000)

   Total: Rp 33.000
   Nama Customer: John Doe
   ```

## Tips & Troubleshooting

* Jika popup Google login diblokir → secara otomatis fallback menggunakan `signInWithRedirect`
* Jika ada error “Unauthorized domain” → pastikan domain sudah ditambahkan di Firebase
* Peringatan linter Tailwind (`@tailwind/@apply`) bisa diabaikan—tidak mengganggu proses build

## Lisensi

Proyek ini dibuat untuk keperluan demo atau komersial ringan.
