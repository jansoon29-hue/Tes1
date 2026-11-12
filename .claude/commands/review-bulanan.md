---
description: Review keuangan bulanan lengkap oleh seluruh tim keuangan (budget, utang, dana darurat, investasi)
argument-hint: [bulan, mis. "Oktober 2026" — kosongkan untuk bulan lalu]
---

Jalankan **review keuangan bulanan** sebagai Koordinator Keuangan Pribadi, mengikuti aturan di `.claude/commands/keuangan.md`.

Periode: $ARGUMENTS (jika kosong, gunakan bulan kalender sebelumnya).

Langkah:
1. Pastikan data di `keuangan/data/` ada dan sudah mencakup periode tersebut; jika belum, minta pengguna melengkapinya dulu.
2. Panggil `budget-cashflow` terlebih dahulu untuk mendapatkan pemasukan, pengeluaran, dan **surplus bulanan**.
3. Dengan angka surplus itu, panggil secara paralel: `utang-cicilan`, `dana-darurat-tabungan`, dan `investasi`.
4. Rangkum menjadi satu laporan:
   - Skor kesehatan keuangan sederhana (savings rate, DSR, bulan dana darurat, % progres tujuan)
   - Perbandingan dengan bulan sebelumnya jika datanya ada
   - Alokasi surplus bulan depan dalam rupiah
   - 3 aksi terpenting bulan depan
5. Simpan laporan ke `keuangan/data/laporan/review-YYYY-MM.md` (ikut tersimpan di repo private).
