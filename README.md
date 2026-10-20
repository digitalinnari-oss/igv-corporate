# IGV Corporate Website — profil perusahaan

## Isi
- `index.html`: halaman korporasi, profil, 5 layanan KBLI, legalitas, ekosistem, kontak.
- `privacy.html`: draf kebijakan privasi.
- `assets/igv-logo.jpg`: logo resmi yang diberikan pemilik.
- `config.js`: nomor WhatsApp admin (sengaja kosong, **jangan mengarang nomor**).
- `styles.css`, `app.js`: desain responsif dan interaksi.

## Pengaturan WhatsApp
Buka `config.js`. Isi `adminWhatsApp` dengan nomor resmi yang telah disetujui dalam format `628...` tanpa simbol `+`, spasi atau awalan `0`. Jika kosong, tombol WhatsApp mengarahkan pengunjung ke email resmi sebagai alternatif. Uji nomor sebelum mempublikasikan.

## Cara memasang website baru, tanpa mengganggu INNARI Digital
1. Di GitHub buat repository BARU, misalnya `igv-corporate` pada akun `digitalinnari-oss`. Jangan mengganti isi repository `innari-digital`.
2. Upload semua file dari folder ini ke akar repository (root), bukan ZIP-nya. Pastikan `index.html` di root.
3. Cloudflare Dashboard > Workers & Pages > Create > Pages > Import existing Git repository.
4. Pilih `digitalinnari-oss/igv-corporate`, branch `main`.
5. Untuk website statis: build command kosong, build output directory `/` (atau opsi default yang sesuai pada UI). Tidak memerlukan framework, Node atau build.
6. Pilih nama proyek, misalnya `igv-corporate` jika tersedia. Alamat akan berbentuk `https://igv-corporate.pages.dev`.
7. Deploy. Buka alamat yang diberikan Cloudflare. Uji menu, tautan, mobile, email dan WhatsApp.
8. Tiap commit ke branch `main` akan memicu deploy otomatis.

## Integrasi website unit layanan
Lima unit yang tercantum adalah nama konsep pemasaran, **bukan badan hukum tersendiri**. Saat website unit telah siap, ubah label 'Website khusus: segera hadir' dan link pada `index.html`/`app.js` sesuai alamat sebenarnya. Jangan mengarang URL.

## INNARI Digital
Tautan marketplace yang sudah ada: https://innari-digital.pages.dev/. Katalog, demo software, e-book preview dan penjualan dikelola terpisah di website tersebut. Jangan menaruh e-book full atau lisensi software privat di direktori publik Cloudflare Pages/GitHub. Untuk preview, unggah hanya cuplikan yang disetujui pemegang hak. Jangan mengandalkan larangan klik kanan sebagai perlindungan file.

## Catatan legal dan keamanan
- Data AHU dan NIB digunakan sesuai dokumen yang diberikan. NPWP pribadi tidak dipublikasikan.
- Tidak ada pembayaran, keranjang, akun pengguna, atau penyimpanan database.
- Pastikan profil, alamat, KBLI, izin tambahan, kebijakan privasi dan nomor admin dikonfirmasi manajemen sebelum dipublikasikan.
- Tidak ada biaya hosting atau subdomain Cloudflare Pages pada penggunaan yang memenuhi batas paket gratis; layanan pihak ketiga/upgrade dapat berbiaya jika dipilih.
