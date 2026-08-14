# PT. Sekawan Muda Sejahtera — Company Profile Website

Situs profil perusahaan (company profile) untuk **PT. Sekawan Muda Sejahtera**,
produsen tepung telur (egg powder) bersertifikat HACCP & Halal yang
berkedudukan di Surabaya, Jawa Timur, Indonesia.

Dibangun sebagai situs statis satu halaman (single-page), tanpa framework
atau build step — cukup HTML, CSS, dan JavaScript murni.

## Struktur Proyek

```
sekawan-muda-website/
├── index.html              # Halaman utama
├── assets/
│   ├── css/
│   │   └── style.css       # Seluruh styling (design tokens, layout, komponen)
│   ├── js/
│   │   └── main.js         # Interaksi: nav mobile, scroll reveal, tab produk
│   └── img/                # Foto & aset visual (diambil dari materi profil perusahaan)
└── .github/
    └── workflows/
        └── deploy.yml       # Auto-deploy ke GitHub Pages saat push ke main
```

## Menjalankan Secara Lokal

Tidak ada dependency atau proses build. Cukup buka `index.html` langsung di
browser, atau jalankan server statis sederhana agar path relatif berjalan
konsisten:

```bash
# Python
python3 -m http.server 8000

# Node (jika sudah terpasang npx)
npx serve .
```

Lalu buka `http://localhost:8000`.

## Deploy ke GitHub Pages

Repo ini sudah menyertakan workflow GitHub Actions (`.github/workflows/deploy.yml`)
yang otomatis men-deploy isi repo ke GitHub Pages setiap kali ada push ke
branch `main`.

Langkah aktivasi:

1. Push repo ini ke GitHub.
2. Buka **Settings → Pages** di repo GitHub.
3. Pada **Build and deployment → Source**, pilih **GitHub Actions**.
4. Push apa pun ke `main` — situs akan otomatis ter-build dan tayang di
   `https://<username>.github.io/<nama-repo>/`.

Jika ingin deploy manual tanpa Actions, cukup aktifkan Pages dari branch
`main` folder `/ (root)` di pengaturan repo.

## Konten & Sumber Aset

Seluruh teks dan foto (tim, fasilitas produksi, produk, logo, sertifikasi
HACCP & Halal) diambil dari dokumen profil perusahaan resmi PT. Sekawan
Muda Sejahtera. Font yang digunakan (Fraunces, Inter, IBM Plex Mono) dimuat
dari Google Fonts.

## Kustomisasi

- **Warna & tipografi** — atur lewat CSS custom properties di bagian atas
  `assets/css/style.css` (`:root { ... }`).
- **Konten teks** — edit langsung di `index.html`, terbagi per section
  (`#tentang`, `#proses`, `#visimisi`, `#produk`, `#sertifikasi`, `#kontak`).
- **Foto** — ganti file di `assets/img/` dengan nama file yang sama, atau
  ubah path `src` di `index.html` bila menggunakan nama baru.

## Kontak

- WhatsApp: +62 823-3216-0700 (Fredy) · +62 823-3091-1111 (Dodie)
- Email: smkomoditi@gmail.com
- Website: www.sekawanmuda.com
