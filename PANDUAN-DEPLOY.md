# Panduan Deploy QRFast di qrcodemassal.id

## File yang perlu diunggah

Unggah seluruh isi paket ini ke root repositori `Arifulamar/qrfast`, terutama:

- `index.html`
- `css/style.css`
- `img/qrfast-social.png`
- `img/qrfast-social.svg`
- `sitemap.xml`
- `robots.txt`
- `CNAME`

Pastikan struktur folder tidak berubah agar alamat gambar dan stylesheet tetap benar.

## Konfigurasi DNS

Tambahkan record berikut pada pengelola DNS domain:

| Type | Name/Host | Value/Target |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `arifulamar.github.io` |

Hapus record A, AAAA, ALIAS, ANAME, atau CNAME lama yang bertabrakan dengan record di atas.

## Pengaturan GitHub Pages

1. Buka repositori `Arifulamar/qrfast`.
2. Pilih **Settings → Pages**.
3. Pada **Custom domain**, masukkan `qrcodemassal.id`, lalu simpan.
4. Tunggu pemeriksaan DNS berhasil.
5. Aktifkan **Enforce HTTPS**.

## Setelah GitHub Pages diperbarui

1. Buka `https://qrcodemassal.id/` dan pastikan generator berfungsi.
2. Buka `https://qrcodemassal.id/sitemap.xml` dan pastikan sitemap tampil.
3. Tambahkan properti situs di Google Search Console.
4. Kirim sitemap dengan alamat `https://qrcodemassal.id/sitemap.xml`.
5. Gunakan **Inspeksi URL** untuk `https://qrcodemassal.id/`, lalu pilih **Minta Pengindeksan**.
6. Periksa hasilnya kembali setelah Google melakukan crawl ulang.
