# KasirKilat UMKM

KasirKilat adalah aplikasi point-of-sale (POS) berbasis web untuk UMKM kuliner. Aplikasi ini menyediakan katalog menu, pengelolaan keranjang, perhitungan diskon dan pajak, proses pembayaran, struk transaksi, riwayat, pesanan aktif, serta laporan penjualan dalam satu halaman responsif.

## Fitur

- Pencarian dan pemfilteran katalog berdasarkan kategori.
- Simulasi pemindaian barcode/SKU.
- Pengelolaan jumlah item dan pengosongan keranjang.
- Perhitungan otomatis:
  - Diskon member sebesar 10%
  - Pajak sebesar 10%
  - Total pembayaran
  - Uang kembalian
- Nominal pembayaran cepat dan input nominal manual.
- Cetak atau simpan tampilan struk melalui fitur print browser.
- Riwayat transaksi beserta detail struk.
- Ringkasan pesanan aktif.
- Laporan pendapatan, jumlah pesanan, jumlah item, dan menu terlaris.
- Penyimpanan keranjang, pengaturan diskon, nominal pembayaran, nomor transaksi, dan riwayat menggunakan `localStorage`.

## Teknologi

- HTML5
- Tailwind CSS melalui CDN
- JavaScript tanpa framework
- Google Fonts
- Material Symbols
- Browser `localStorage`

Tidak diperlukan backend atau proses build untuk menjalankan aplikasi ini.

## Struktur Proyek

```text
.
├── index.html
└── README.md
```

## Cara Menjalankan

### Metode langsung

1. Buka folder proyek.
2. Jalankan [index.html](./index.html) dengan browser.

### Menggunakan server lokal

Jika tersedia VS Code Live Server:

1. Buka `index.html` di Visual Studio Code.
2. Klik kanan pada file.
3. Pilih **Open with Live Server**.

Atau jalankan server sederhana dengan Python:

```bash
python -m http.server 8000
```

Kemudian buka `http://localhost:8000`.

## Penggunaan

1. Cari atau pilih menu pada tab **Katalog**.
2. Tambahkan item ke keranjang.
3. Sesuaikan jumlah atau hapus item bila diperlukan.
4. Aktifkan/nonaktifkan diskon member.
5. Masukkan uang pembayaran atau pilih nominal cepat.
6. Tekan **Proses Pembayaran** setelah nominal mencukupi.
7. Struk transaksi akan muncul dan dapat dicetak.
8. Buka tab **Pesanan**, **Riwayat**, atau **Laporan** untuk melihat data lainnya.

## Penyimpanan Data

Data disimpan pada browser yang digunakan saat ini melalui `localStorage`. Data tidak dikirim ke server dan dapat hilang jika pengguna membersihkan data situs atau menggunakan browser/profil lain.

Untuk menghapus seluruh data aplikasi, buka tab **Laporan Penjualan** lalu pilih **Reset Data**.

## Cetak Struk

Struk dapat dicetak atau disimpan sebagai PDF melalui dialog print browser. Tampilan cetak hanya menampilkan area struk karena aplikasi menerapkan aturan khusus pada CSS `@media print`.
