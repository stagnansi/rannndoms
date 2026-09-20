# Rannndoms — Catatan Proyek

## Stack
Hugo + tema hugo-bearblog + GitHub + Cloudflare Pages

## Lokasi dan Repo
- Proyek: ~/rannndoms (Termux)
- Repo: github.com/stagnansi/rannndoms (branch: master, public)
- Live: https://rannndoms.pages.dev
- Cloudflare: build command hugo --minify, output public, env HUGO_VERSION=0.166.0

## Konfigurasi hugo.toml
- baseURL = https://rannndoms.pages.dev/
- title = Rannndoms®
- theme = hugo-bearblog
- buildFuture = true
- disableHugoGeneratorInject = true
- params description = Tulisan yang tidak dicari siapa pun, tapi ditulis dengan sungguh-sungguh.
- markup.goldmark.renderer.unsafe = true

## Konten
- Artikel di content/blog/*.md
- Frontmatter YAML atau TOML
- Kalau tidak pakai buildFuture, tanggal artikel harus sudah lewat

## Kustomisasi Lokal
- layouts/index.html: halaman depan menampilkan daftar artikel
- layouts/partials/footer.html: bird + slash + copyright/link
- layouts/partials/custom_head.html: link font Inter + IBM Plex Mono
- layouts/partials/custom_body.html: JS auto-hide footer dan tombol back to top
- layouts/partials/style.html: CSS lengkap, rewrite penuh sesi 22

## Aturan Kerja
- Setiap update langsung commit dan push
- Setiap update ikut update changelog.md ini
- Setiap update sertakan perintah restart server + cek localhost
- Jangan pakai em dash di tulisan apapun
- Artikel minimal 800 kata
- Judul artikel pendek, tidak panjang
- Setiap artikel baru wajib update readme.md bagian Isi

## Aturan Backlink
- Link spesifik ke halaman tertentu, bukan homepage
- Dilarang link ke Wikipedia
- Link menyatu di dalam kalimat, tanpa frasa pengantar
- Untuk lagu: link YouTube official dari channel resmi
- Untuk brand: situs resmi atau review kredibel

## Aturan Tulisan
- Boleh pakai bold, italic, code inline sesuai konteks, tidak dipaksakan
- Body font Inter, heading InterDisplay, mono IBM Plex Mono
- Gaya esai mengalir seperti herman.bearblog.dev

## Bug Termux HP Ini
Paste multi-baris di Termux HP ini mengubah newline jadi spasi dan merusak file.
Solusi: gunakan printf dengan format %b dan \n di dalam string, semua dalam satu baris tunggal.
Jangan pakai heredoc cat EOF, jangan pakai printf dengan backslash di akhir baris.
Jangan pakai >> ke style.html, harus rewrite penuh atau sed insert sebelum </style>.

## Perintah Umum
- Jalankan server: cd ~/rannndoms && hugo server --noBuildLock --bind 0.0.0.0
- Buka http://localhost:1313
- Build statis: cd ~/rannndoms && hugo --noBuildLock
- Push: git add -A && git commit -m pesan && git push

## Yang Sudah Selesai
- Situs Hugo jalan, tema Bear Blog aktif
- Halaman depan menampilkan daftar artikel
- Footer split: minimal di halaman pendek, lengkap di halaman panjang
- Bird hover biru Twitter, link ke x.com/rannndoms
- Tombol back to top, auto-hide kalau halaman tidak scrollable
- Font Inter, InterDisplay, IBM Plex Mono
- Warning LanguageCode teratasi lewat override baseof.html
- Artikel: Halo Dunia (8 Jan 2025), Kalah dari yang Gratis (15 Mar 2025)
- readme.md tanpa mention Hugo
- Catatan proyek ini (publik, ditulis ringkas tanpa info sensitif)

## Referensi
- herman.bearblog.dev (gaya tulisan)
- x.com/rannndoms (akun X)

## Update Log Ringkas
- Sesi 1 sampai 15: Setup awal, tema, artikel pertama, artikel kedua
- Sesi 16 sampai 22: Poles footer, tombol back to top, README, rewrite style.html

## Update Log Sesi 23
- Artikel baru: "Blog dari HP Sebelum Zaman Android" tentang Mywapblog
- Tanggal: 2025-06-12
- Tema: kenangan platform blog seluler legendaris, pendiri Arvind Gupta, penutupan 2016
- Backlink: esato.com, sepenggal.info, mojok.co, infiartt.com
- README diupdate dengan judul artikel baru

## Update Log Sesi 23 revisi
- Fix artikel Mywapblog: hapus marker [reference:N], ganti dengan link asli
- Backlink: esato.com forum untuk tanggal rilis, mojok.co untuk pesan perpisahan
- Fix readme: pindahkan link artikel baru ke section Isi, tidak lagi nyasar di Lisensi

## Update Log Sesi 24
- Rewrite artikel "Kalah dari yang Gratis" dengan variasi teks merata
- Variasi bold/italic tersebar dari awal sampai akhir, tidak numpuk di awal
- Backlink sengaja tidak dipasang karena belum bisa verifikasi link yang valid
- Aturan final: semua artikel wajib variasi teks merata

## Update Log Sesi 25
- Artikel baru: "Tiga Singkatan yang Sering Tertukar" tentang perbedaan FBI, SWAT, MI6
- Tanggal: 2025-09-08
- Tema: perbandingan fungsi, yurisdiksi, dan domain kerja FBI, SWAT, MI6
- Gaya: mengalir, personal, dengan analogi
- Variasi teks: bold untuk istilah kunci dan angka, italic untuk istilah asing
- README diupdate dengan judul artikel baru
