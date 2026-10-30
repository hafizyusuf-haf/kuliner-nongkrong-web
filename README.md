# mampir. — Direktori Kuliner & Nongkrong Purwokerto

Website katalog statis yang responsif untuk menjelajahi tempat makan, coffee shop, dan tempat nongkrong di Purwokerto.

## Fitur
- Pencarian nama, menu/jenis tempat, dan area.
- Filter kategori dan pengurutan rating/nama.
- Kartu tempat dengan rating, kategori, area, dan ringkasan.
- Detail tempat dan tautan pencarian Google Maps.
- Simpan tempat favorit (Local Storage).
- Layout responsif untuk desktop dan ponsel.

## Menjalankan secara lokal
Tidak perlu framework atau instalasi dependency.

```bash
git clone https://github.com/USERNAME/mampir-purwokerto.git
cd mampir-purwokerto
```

Buka `index.html` di browser, atau jalankan server lokal:

```bash
python -m http.server 5500
```

Lalu buka http://localhost:5500.

## Git & GitHub workflow

### 1. Buat repository
Buat repository baru di GitHub bernama `mampir-purwokerto`. Pilih Public jika ingin dipublikasikan melalui GitHub Pages.

### 2. Inisialisasi dan commit pertama
Jika folder hasil download ZIP:

```bash
git init
git add .
git commit -m "feat: initial Purwokerto food and hangout directory"
git branch -M main
git remote add origin https://github.com/USERNAME/mampir-purwokerto.git
git push -u origin main
```

### 3. Workflow fitur menggunakan branch
```bash
git switch -c feat/add-place-submissions
# edit file, lalu:
git add .
git commit -m "feat: add place submission section"
git push -u origin feat/add-place-submissions
```
Buka Pull Request di GitHub → review perubahan → merge ke `main`.

### 4. Deploy dengan GitHub Pages
1. Buka repository di GitHub.
2. Masuk **Settings → Pages**.
3. Pada **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Tunggu proses deploy. URL umumnya `https://USERNAME.github.io/mampir-purwokerto/`.

Setiap push ke branch `main` akan memperbarui situs.

## Struktur proyek
```text
mampir-purwokerto/
├── index.html
├── styles.css
├── script.js
├── README.md
└── .gitignore
```

## Memperbarui katalog
Data tempat berada di array `places` pada `script.js`. Setiap objek memiliki:
`id`, `name`, `category`, `area`, `address`, `rating`, `tag`, `desc`, `detail`, `image`, dan `maps`.

Kategori yang digunakan: `Kuliner`, `Coffee shop`, `Nongkrong`.
Gunakan rating sebagai informasi referensi dan verifikasi kembali ke sumber terbaru sebelum publikasi. Foto demo mengambil gambar dari Unsplash; ganti dengan foto milik sendiri atau foto yang memiliki izin penggunaan sebelum dipublikasikan secara komersial.

## Sumber awal kurasi
- iNews Purwokerto, *10 Rekomendasi Kafe di Purwokerto untuk Nongkrong dan Nugas Hingga Larut Malam* (6 Februari 2025): https://purwokerto.inews.id/read/553554/10-rekomendasi-kafe-di-purwokerto-untuk-nongkrong-dan-nugas-hingga-larut-malam/all
- Traveloka, *8 Cafe Terbaik di Purwokerto*: https://www.traveloka.com/id-id/explore/activities/cafe-di-purwokerto-ta/574061
- PurwokertoHitz, *8 Cafe di Purwokerto Terbaik untuk Nongkrong dan Nugas* (11 Juli 2026): https://purwokertohitz.com/cafe-di-purwokerto-hits/
- Data lokasi dan rating tempat menggunakan hasil pencarian Google Maps yang tersedia saat pembuatan. Detail jam buka/menu tidak ditampilkan karena perlu verifikasi langsung.

**Catatan:** Direktori ini merupakan prototipe komunitas, bukan afiliasi resmi dengan tempat yang tercantum. Rating, alamat, dan status operasional dapat berubah.
