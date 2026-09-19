# Rannndoms® — Catatan Proyek

## Stack
Hugo + tema hugo-bearblog + GitHub + Cloudflare Pages

## Lokasi dan Repo
- Proyek: ~/rannndoms (Termux)
- Repo: github.com/stagnansi/rannndoms (branch: master)
- Live: https://rannndoms.pages.dev
- Cloudflare: build command hugo --minify, output public, env HUGO_VERSION=0.166.0

## Konfigurasi hugo.toml
- baseURL = https://rannndoms.pages.dev/
- title = Rannndoms®
- theme = hugo-bearblog
- buildFuture = true (WAJIB, kalau tidak artikel bertanggal besok tidak akan tampil)
- params description = Catatan acak dari Android, author = Rannndoms
- markup.goldmark.renderer.unsafe = true

## Konten
- Artikel ditaruh di content/blog/*.md
- Frontmatter YAML --- atau TOML +++ keduanya OK
- Kalau tidak mau pakai buildFuture, tanggal artikel harus sudah lewat

## Kustomisasi Lokal di layouts/
- layouts/index.html: halaman depan menampilkan daftar artikel dari section blog
- layouts/partials/footer.html: copyright 2026 Rannndoms
- layouts/partials/style.html: CSS kustom light mode only, tanpa dark mode, tanpa warna visited link

## PENTING - Bug Paste Termux HP Ini
Paste multi-baris di Termux HP ini mengubah newline jadi spasi dan MERUSAK file.
Solusi: gunakan printf dengan format persen-b dan penulisan backslash-n di dalam string, semua dalam SATU BARIS TUNGGAL.
Jangan pakai heredoc cat EOF atau printf dengan backslash di akhir baris.

## Perintah Umum
- Jalankan server: cd ~/rannndoms && hugo server --noBuildLock --bind 0.0.0.0
- Buka http://localhost:1313
- Build statis: cd ~/rannndoms && hugo --noBuildLock
- Push: git add -A && git commit -m pesan && git push

## Yang Sudah Selesai
- Situs Hugo berjalan di Termux, tema Bear Blog aktif
- Halaman depan menampilkan daftar artikel
- Footer copyright kustom
- Light mode paksa, visited link dimatikan
- Artikel contoh Halo Dunia tampil

## Ide Berikutnya yang Belum Dikerjakan
- Kustomisasi font (Verdana jadi system-ui)
- Kustomisasi lebar konten (720px)
- Ganti URL /blog/ jadi /catatan/ atau lainnya
- Favicon kustom
- Menu navigasi
- Sosial media links
