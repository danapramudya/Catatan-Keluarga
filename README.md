# Catatan Program Keluarga

Aplikasi catatan harian untuk program kebiasaan keluarga: aturan malam, Subuh berjamaah, minum, tidur, tugas rumah, olahraga, dan screen time.

## Cara memasang di Android

1. Buka alamat GitHub Pages repository ini di **Chrome**.
2. Ketuk menu ⋮ di kanan atas, lalu **Install aplikasi** (atau **Tambahkan ke layar utama**).
3. Ikon "Catatan Keluarga" muncul di layar utama dan bisa dibuka tanpa internet.

## Tentang data

- Semua catatan tersimpan **hanya di HP tempat aplikasi dipasang**, tidak dikirim ke mana pun.
- Jangan pakai mode penyamaran (Incognito), dan jangan hapus data situs Chrome untuk alamat ini.
- Unduh cadangan seminggu sekali dari menu **Atur → Cadangan data**, simpan di Google Drive. File yang sama bisa dipakai untuk memulihkan data di HP lain.

## Isi repository

| Berkas | Fungsi |
| --- | --- |
| `index.html` | Seluruh aplikasi |
| `manifest.webmanifest` | Nama, ikon, dan warna saat dipasang |
| `sw.js` | Menyimpan berkas supaya bisa dibuka tanpa internet |
| `icons/` | Ikon aplikasi |

Setelah mengubah `index.html`, naikkan nomor versi `CACHE` di `sw.js` supaya HP mengambil versi baru.

## Versi APK Android (untuk tablet Nara)

Folder `android/` berisi aplikasi Android yang menjalankan catatan harian langsung dari dalam APK: tanpa internet, tanpa website, dan tidak bisa dipakai browsing.

- APK dibuat otomatis oleh GitHub Actions (`.github/workflows/android.yml`) setiap ada perubahan di `android/`, lalu diterbitkan di halaman **Releases**.
- Unduhan terbaru: https://github.com/danapramudya/Catatan-Keluarga/releases/latest/download/catatan-keluarga.apk
- Kunci tanda tangan disimpan terenkripsi di `android/catatan.jks.enc`; kata sandinya ada di secret repo `CATATAN_KEY`. Jangan ganti kunci ini, supaya pembaruan bisa dipasang di atas versi lama tanpa menghapus catatan.
- Isi aplikasi ada di `android/app/src/main/assets/index.html` (versi Nara: batas perangkat 22.00).
