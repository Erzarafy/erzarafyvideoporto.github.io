# Portofolio Video Erza

Website showcase mandiri untuk karya video editing Erza Al-Isyrafy. Dibuat menggunakan HTML, CSS, dan JavaScript tanpa framework atau proses build.

## Menambahkan video

Buka `script.js` dan tambahkan objek video ke array `videoProjects` di bagian atas file. Untuk YouTube:

```js
{
  youtubeId: "ID_VIDEO_YOUTUBE",
  title: "Judul proyek",
  category: "short-form",
  categoryLabel: "SHORT-FORM",
  client: "Nama brand atau klien",
  description: "Deskripsi singkat proyek.",
  year: "2025",
  duration: "00:30",
  thumbnail: "https://example.com/thumbnail.jpg",
  mark: "ERZA.",
  glow: "rgba(205,243,107,.2)"
}
```

- Ambil `youtubeId` dari bagian setelah `v=` pada URL `youtube.com/watch?v=...`.
- Kategori yang tersedia: `short-form`, `brand`, dan `lifestyle`.
- `thumbnail`, `duration`, `client`, `description`, `year`, `mark`, dan `glow` opsional. Tanpa thumbnail, situs menampilkan visual grafis bawaan.
- Video dapat disematkan jika pengaturan YouTube mengizinkan pemutaran di situs lain.

Video Google Drive yang dibagikan dengan akses **Anyone with the link / Siapa saja yang memiliki link** juga dapat ditampilkan:

```js
{
  source: "drive",
  driveId: "ID_FILE_DRIVE",
  title: "Judul proyek",
  category: "short-form",
  categoryLabel: "SHORT-FORM",
  client: "Nama brand atau klien",
  thumbnail: "https://drive.google.com/thumbnail?id=ID_FILE_DRIVE&sz=w1200"
}
```

Klik kartu akan membuka pemutar video di halaman ini. Video YouTube menggunakan embed privasi-ditingkatkan; Google Drive menggunakan pemutar preview Drive di dalam modal.

## Menjalankan dan menerbitkan

Buka `index.html` di browser untuk melihat situs. Untuk publikasi dengan GitHub Pages:

1. Unggah isi folder ini ke root repositori GitHub dan push ke branch `main`.
2. Pada **Settings → Pages**, pilih **GitHub Actions** sebagai sumber deploy.
3. Workflow di `.github/workflows/pages.yml` akan menerbitkan situs dan menampilkan URL publiknya.

Setelah URL situs didapatkan, ganti `href` kartu video editing di `website-erza/index.html` dengan URL publik tersebut agar pengunjung dari portofolio utama diarahkan ke showcase ini.

## Kontak

Tombol “Diskusikan proyek” mengarahkan pengunjung ke situs utama: [erzarafy.github.io](https://erzarafy.github.io/). Alamat email tetap tersedia sebagai tautan terpisah di bagian kontak.
