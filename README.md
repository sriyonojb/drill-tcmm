# DRILL TCMM — GitHub Pages

Portal GitHub Pages untuk membuka Web App Apps Script yang sudah ada.

**Target Apps Script:** https://script.google.com/macros/s/AKfycbzY1XIbnN-u71qYdEeozhUqG25SXsYMRQSckabDIW-SHcpEOm9M6y28yyf6Kt8Zx2IJ/exec

## Cara terbitkan dari browser HP/iPad/komputer

1. Masuk ke https://github.com/new dan buat repository baru bernama `drill-tcmm`. Untuk GitHub Free, gunakan **Public** agar GitHub Pages dapat digunakan.
2. Unggah `index.html`, `.nojekyll`, dan `README.md` ke root repository pada branch `main`. **Jangan unggah file ZIP mentah sebagai satu-satunya file**; ekstrak terlebih dahulu.
3. Buka repository > **Settings** > **Pages** > **Build and deployment**.
4. Pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
5. Lihat URL yang GitHub berikan di Settings > Pages; umumnya `https://USERNAME.github.io/drill-tcmm/` (ganti `USERNAME` dengan nama akun GitHub Anda).
6. Buka link dari Safari, Chrome, atau tab privat. GitHub Pages akan meneruskan browser ke URL Google Apps Script yang sudah ada.

## Agar pengunjung berbeda akun dapat mengakses

Di Google Apps Script, buka **Deploy > Manage deployments > Edit** (atau deployment Web App baru jika belum ada), atur **Execute as: Me** dan **Who has access: Anyone**, lalu deploy. Uji URL `/exec` langsung di browser tanpa login Google. Jika Apps Script tidak dapat diakses publik, GitHub Pages tidak dapat mengatasinya.

## Batasan penting

- GitHub Pages adalah **hosting statis**. Proyek ini hanya menyediakan halaman redirect; **tidak memindahkan backend Apps Script** ke GitHub.
- Alamat browser **akan berubah ke `script.google.com`** setelah redirect. Agar aplikasi tetap berada di domain `github.io`, diperlukan porting antarmuka web ke GitHub Pages dan mempertahankan backend secara terpisah; perlu kode HTML/CSS/JS Web App asli.
- Jangan memasukkan kata sandi, token API, atau rahasia server ke repository public.
- Jangan mengubah endpoint Apps Script yang dipakai Kodular atau WA Collector hanya karena ada portal GitHub.
