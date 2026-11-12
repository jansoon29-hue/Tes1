# Tim Keuangan Pribadi

Tim agen AI untuk mengelola keuangan pribadi di Claude Code. Bahasa utama Indonesia, bisa juga bahasa Inggris.

## Anggota tim

| Peran | File | Tugas |
|---|---|---|
| Koordinator (CFO pribadi) | `.claude/commands/keuangan.md` | Membagi pertanyaan ke agen yang tepat dan merangkum hasilnya |
| Budget & Cash Flow | `.claude/agents/budget-cashflow.md` | Pemasukan, pengeluaran, budget, surplus |
| Utang & Cicilan | `.claude/agents/utang-cicilan.md` | DSR, strategi pelunasan avalanche/snowball |
| Dana Darurat & Tabungan | `.claude/agents/dana-darurat-tabungan.md` | Target dana darurat, tabungan per tujuan |
| Investasi | `.claude/agents/investasi.md` | Profil risiko, alokasi aset, simulasi |

## Cara pakai

1. Salin template ke folder data: `cp -r keuangan/template keuangan/data`
2. Isi file CSV di `keuangan/data/` dengan angka Anda (atau minta Claude membantu mengisinya lewat percakapan).
3. Di Claude Code, ketik:
   - `/keuangan <pertanyaan>`, contoh: `/keuangan berapa yang bisa saya investasikan tiap bulan?`
   - `/review-bulanan Oktober 2026` untuk review lengkap oleh seluruh tim.
   - Atau panggil satu agen langsung: "pakai agen utang-cicilan untuk bandingkan avalanche vs snowball".

## Privasi

Data asli di `keuangan/data/` **ikut disimpan di repo** supaya tidak hilang antar sesi. Ini aman selama repo tetap **private**. Kalau repo akan dijadikan publik, aktifkan lagi baris `data/` di `keuangan/.gitignore` dan hapus data dari riwayat git terlebih dahulu.

> Tim ini memberi analisis dan edukasi, bukan nasihat keuangan berlisensi. Untuk keputusan besar, konsultasikan dengan perencana keuangan bersertifikat.
