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

## Referensi Gaya Tulisan
- URL: https://herman.bearblog.dev
- Ciri khas: esai pendek-menengah, judul singkat, paragraf padat, bahasa personal
- Tidak ada meta tag Hugo, tidak ada jejak generator

## Preferensi Pengguna
- Judul artikel pendek dan to the point
- Tidak mau ketahuan pakai Hugo dari View Source
- Update artikel via Termux copas dari AI, bukan PocketHugo

## Update Log

### Sesi 2
- Deskripsi situs diubah jadi: "Tulisan pendek tentang apa pun yang sedang menarik perhatian"
- disableHugoGeneratorInject = true ditambahkan ke hugo.toml (hapus jejak meta generator Hugo)
- line-height dirapatkan: body 1.5 -> 1.4, main 1.6 -> 1.5
- Artikel Halo Dunia ditulis ulang gaya Herman: pendek, personal, tanpa menyebut Hugo
- Referensi: herman.bearblog.dev
- Judul artikel mulai sekarang pendek dan to the point
- Update artikel via Termux (copas dari AI), bukan PocketHugo

## ATURAN PENTING (mulai sekarang)
- Setiap update WAJIB langsung commit dan push, tanpa nunggu konfirmasi
- Setiap kali ada perubahan, CATATAN.md ikut diupdate
- Artikel minimal 800 kata
- Judul artikel pendek dan to the point
- Bahasa Indonesia, gaya Herman: paragraf mengalir, personal, tanpa bullet berlebihan

## Update Log Sesi 3
- Deskripsi situs: "Tulisan pendek tentang apa pun yang sedang menarik perhatian"
- disableHugoGeneratorInject = true (hapus jejak meta Hugo)
- line-height: body 1.4, main 1.5 (dirapatkan sesuai permintaan)
- Artikel Halo Dunia ditulis ulang, 850+ kata, gaya Herman
- Referensi gaya: herman.bearblog.dev
- Font: InterDisplay (heading), Inter (body), IBM Plex Mono (code & time)

## Update Log Sesi 4
- Artikel Halo Dunia ditulis ulang, tanpa em dash sama sekali
- Ditambahkan cerita personal: lagu Abadi dari Perunggu diputar 1.284 kali + sebungkus Djarum 76 Apel Royal
- ATURAN BARU: semua tulisan tidak boleh pakai em dash (biar tidak kelihatan AI)

## ATURAN MUTLAK (jangan dilanggar)
- JANGAN PERNAH pakai em dash (karakter panjang ini: —) di tulisan apapun
- Alasan: biar tidak kelihatan seperti tulisan AI
- Kalau butuh pemisah, pakai koma, titik, titik dua, tanda kurung, atau pisah jadi dua kalimat
- Berlaku untuk artikel, catatan, komentar, dan file apapun di repo ini

## Koreksi
- Judul lagu Perunggu yang benar: "Ini Abadi", bukan "Abadi"

## Update Log Sesi 5
- Termux di-uninstall, proyek di-clone ulang dari GitHub ke ~/rannndoms
- Submodule tema perlu git submodule update --init --recursive setiap clone ulang
- Fix warning deprecated .Site.LanguageCode dengan override file tema ke layouts/ lokal
- Perbaikan ini permanent, ikut ter-push ke GitHub, tidak perlu diulang tiap clone

## ATURAN FORMAT TULISAN
- Boleh pakai **bold**, *italic*, dan `code` inline kalau memang sesuai konteks
- Jangan dipaksakan. Kalau tidak perlu, tidak usah dipakai
- Bold: untuk penekanan pada frasa kunci, nama diri penting
- Italic: untuk judul lagu/buku, istilah asing, pemikiran internal, kata yang sedang dibahas
- Code: untuk istilah teknis, nama file, perintah, path
- Jangan pakai em dash (—), tetap berlaku

## ATURAN BACKLINK
- Setiap artikel sebaiknya punya beberapa backlink ke situs eksternal yang relevan dengan konteks kalimat
- Sumber bebas: berita, X, YouTube, Reddit, Wikipedia, situs resmi brand, dan lain-lain
- Jangan dipaksakan. Kalau kalimatnya tidak butuh link, tidak usah
- Link ditaruh di dalam kalimat, bukan daftar terpisah di akhir
- Format: [teks](url)

## ATURAN FORMAT TULISAN
- Boleh pakai **bold**, *italic*, dan `code` inline kalau sesuai konteks
- Jangan dipaksakan. Kalau tidak perlu, tidak usah dipakai
- Bold: untuk penekanan frasa kunci, nama diri penting
- Italic: untuk judul lagu/buku, istilah asing, pemikiran internal
- Code: untuk istilah teknis, nama file, perintah, path
- Em dash (—) tidak boleh dipakai sama sekali

## ATURAN BACKLINK (REVISI)
- Wajib pakai link spesifik, bukan homepage. Contoh: postingan X tertentu, video YouTube tertentu, artikel berita tertentu.
- Dilarang link ke Wikipedia.
- Untuk lagu: pakai link video YouTube official dari channel resmi artis/label.
- Untuk brand: pakai link resmi brand, atau review/artikel berita yang kredibel.
- Sumber boleh dari mana saja: X, YouTube, Reddit, berita, jurnal, blog pribadi, dll.
- Link harus relevan dengan konteks kalimat. Jangan dipaksakan.
- Link ditaruh di dalam kalimat, bukan daftar terpisah.

## ATURAN BACKLINK (REVISI FINAL)
- Dilarang keras link ke Wikipedia.
- Dilarang pakai frasa pengantar seperti "ada sebuah utas", "ada sebuah tweet", "ada penelitian". Link harus langsung menyatu dengan kalimat.
- Contoh benar: "Levelsio pernah bilang di X bahwa..." dengan X di-link.
- Contoh salah: "Ada sebuah tweet dari Levelsio yang bilang..."
- Link harus spesifik ke halaman/konten tertentu, bukan homepage.
- Untuk lagu: link ke video YouTube official dari channel resmi artis/label.
- Untuk brand: link ke situs resmi atau review/artikel kredibel yang membahas brand itu.
- Sumber bebas: X, YouTube, Reddit, berita, jurnal, blog pribadi. Selain Wikipedia.

## ATURAN BACKLINK (FINAL)
- Link langsung menyatu di dalam kalimat, TANPA frasa pengantar apapun
- Dilarang: "ada sebuah tweet", "xxx pernah bilang", "artikel di X", "penelitian dari X", "menurut X"
- Contoh benar: "Jangkauan di X bisa [35.000 kali lebih besar dari blog](url)."
- Contoh salah: "Levelsio pernah bilang bahwa jangkauan di X bisa 35.000 kali lebih besar dari blog."
- Dilarang link ke Wikipedia
- Untuk lagu: link YouTube official dari channel resmi
- Untuk brand: situs resmi atau review kredibel

## Update Log Sesi 6
- Heading h1-h6 line-height diset 1
- Heading margin-bottom 0.4em
- Jarak judul ke time dirapatkan dengan rule h1 + p margin-top 0

## Update Log Sesi 7
- Deskripsi situs diganti: "Tulisan yang tidak dicari siapa pun, tapi ditulis dengan sungguh-sungguh"
- Alasan: konsisten dengan artikel 800+ kata, lebih catchy, self-aware

## Koreksi
- Deskripsi situs diakhiri titik

## ATURAN TANGGAL ARTIKEL
- Halo Dunia: 8 Januari 2025

## Update Log Sesi 8
- Footer diganti: Rannndoms® / {{ now.Year }} (tahun otomatis)
- Styling: border-top 1px #e5e5e5, margin-top 40px, warna #999, font-size 0.85em, letter-spacing 0.05em
- Kombinasi F (slash) + D (garis horizontal)

## Update Log Sesi 9
- Footer final: Rannndoms® (link ke x.com/rannndoms) / slash besar / tahun otomatis
- Styling slash: font-size 1.4em, weight 200, warna #ccc, margin horizontal 0.3em
- Link footer warna #999, hover biru, tanpa underline
- File static/preview.html dihapus

## Update Log Sesi 9 revisi
- Hapus border-top (garis horizontal) di footer
- Hapus styling custom footer a dan a:hover, kembali ke default tema (warna link, hover underline)

## Update Log Sesi 10
- Footer brand pakai InterDisplay weight 900 (Black)
- Letter-spacing -0.02em biar rapat dan tegas
- Selector: footer a:first-child

## Update Log Sesi 10 revisi
- Tahun di-wrap dalam span.year
- Selector footer a:first-child, footer .year sama-sama InterDisplay 900

## Update Log Sesi 11
- Footer final gaya opsi I: bird SVG + slash + Rannndoms link + (R)
- Semua warna senada #222
- Link pakai dotted underline, warna inherit
- Tahun dihapus dari footer
- Bird dan (R) di luar link, hanya Rannndoms yang bisa diklik

## Update Log Sesi 11 revisi
- Padding-top footer dikurangi dari 25px ke 10px, padding-bottom 20px
- Hapus duplikasi CSS footer (tema asli + override tadi)
- CSS footer sekarang hanya satu blok, isinya padding, color #222, InterDisplay 900
- Konfirmasi: tag <footer> hanya ada di baseof.html, tidak diduplikasi

## Update Log Sesi 11 revisi 2
- Padding-top footer diset 0, padding-bottom tetap 20px

## Update Log Sesi 11 revisi 3
- Padding-top footer diset 1.4rem (sama dengan line-height body)
- Tambah rule main > *:last-child margin-bottom: 0 biar paragraf terakhir gak ada margin bawah
- Total jarak paragraf terakhir ke footer = 1.4rem (setara 1 line height)

## Update Log Sesi 11 revisi 4
- Root cause jarak footer jauh: paragraf terakhir punya margin-bottom 1em, tidak collapse karena beda parent dengan footer
- Fix: main p:last-child dan content p:last-child margin-bottom 0

## Update Log Sesi 11 revisi 5
- Rewrite penuh style.html dari nol, bersih dari sisa-sisa patch
- Tambah content { display: block; } yang sebelumnya tidak ada, kemungkinan penyebab utama gap
- content > *:last-child margin-bottom 0 untuk hapus margin paragraf terakhir

## Update Log Sesi 11 revisi 6
- Rule last-child diubah dari * ke p saja, biar ul.blog-posts tidak kena margin 0
- ul.blog-posts dapat margin block 1em atas dan bawah
- Homepage: jarak list ke footer seimbang dengan jarak elemen lain
- Artikel: paragraf terakhir tetap margin 0, jarak ke footer tetap rapat

## Update Log Sesi 12
- Heading h1-h6 dapat font-weight 900 (sama dengan footer)
- Sudah pakai InterDisplay via var(--font-main), sekarang weight juga konsisten

## Update Log Sesi 12 revisi
- font-weight 900 dihapus dari heading umum (h1-h6)
- Hanya judul situs di header (.title h1 / .title h2) yang dapat weight 900
- Judul artikel dan heading lain kembali normal

## Update Log Sesi 13
- Body pakai Inter weight 500 (Medium)
- Heading h1-h6 tetap weight 400 (normal), tidak ikut berubah
- Judul situs tetap 900 via .title h1, .title h2

## Update Log Sesi 13 revisi 2
- Konfirmasi: selector ul.blog-posts li a hanya berlaku di homepage list
- single.html pakai h1 default, tidak terpengaruh

## Update Log Sesi 13 revisi 5
- Hapus font-weight dari heading umum h1-h6, biarkan browser default (bold)
- Sesuai tema asli Bear Blog yang tidak set font-weight di heading
- Judul situs (.title h1, .title h2) tetap 900 karena permintaan eksplisit sebelumnya

## Update Log Sesi 13 revisi 6
- Hapus font-weight 500 dari body
- Hapus font-weight 400 dari heading h1-h6
- Body kembali Inter normal, heading kembali default tema (bold browser)
- Sisa font-weight: 900 judul situs, 200 slash, 900 footer

## Update Log Sesi 13 revisi 7
- Tambah rule ul.blog-posts li a font-weight 500 (Medium)
- Judul artikel di homepage list jadi Medium, judul di single article tetap default

## Update Log Sesi 14
- Gap judul artikel ke time dikurangi setengah
- Rule baru: h1 + p margin-top 0.5em

## Update Log Sesi 14 revisi
- Gap judul artikel ke time: 0.5em -> 0.7em

## Update Log Sesi 14 revisi 2
- Gap judul artikel ke time: 0.7em -> 0.3em

## Update Log Sesi 14 revisi 4
- Kembalikan h1-h6 margin-bottom ke 0.4em
- Tambah rule khusus h1 { margin-bottom: 0.1em } untuk judul artikel
- Hanya judul artikel yang rapat ke time, heading lain (h2-h6) tetap default

## Update Log Sesi 15
- Artikel baru: "Kalah dari yang Gratis", tanggal 2025-03-15
- Tema: langganan Gemini Pro tapi DeepSeek gratis lebih pintar
- Backlink: deepseek.com, arxiv V3, arxiv R1
- Judul pendek biar tidak wrapping di HP

## Update Log Sesi 16
- Tambah README.md untuk GitHub, tanpa menyebut nama generator situs
- Isi: deskripsi blog, daftar artikel, prinsip tulisan, kontak

## Update Log Sesi 17
- Fix artikel Kalah dari yang Gratis: hapus kalimat Selamat datang di awal
- Tambah rule footer a:hover text-decoration none (hover di footer tidak underline, link di body tetap)

## Update Log Sesi 18
- Footer jadi split layout: brand kiri, tombol back to top kanan
- Tombol back to top: panah chevron abu (#999), hover hitam (#222)
- Footer link hover: border-bottom dotted ilang
- html scroll-behavior smooth
- body id="top" sebagai target anchor
- Preview.html dihapus

## Update Log Sesi 18 revisi
- Fix padding footer: dari 20px 0 jadi 0 0 20px 0 (bawah saja)
- Penyebab: rewrite CSS sesi 18 menimpa padding sebelumnya

## ATURAN README.md
- Setiap ada artikel baru, WAJIB update README.md bagian Isi dengan tambah judul + tanggal
- JANGAN pernah tulis di README hal-hal yang mengindikasikan pakai AI atau generator situs
- Dilarang menulis di README: "tidak pakai em dash", "judul pendek", "gaya mengalir", "minimal 800 kata", "Hugo", nama generator lain
- Section Prinsip DIHAPUS dari README, diganti "Catatan" berisi kalimat natural
- Alasan: README publik, bisa dilihat siapa saja, jangan sampai ketahuan pakai AI

## Update Log Sesi 19
- Tombol back to top auto-hide kalau halaman tidak scrollable
- File baru: layouts/partials/custom_body.html berisi JS cek scrollHeight vs innerHeight
- CSS .to-top default display none, JS yang nampilin kalau halaman bisa discroll

## Update Log Sesi 20
- Footer: link pindah ke bird, teks jadi copyright (c) tahun berjalan
- Bird hover jadi warna Twitter #1DA1F2, tanpa underline
- footer-brand auto-hide sama seperti to-top saat halaman tidak scrollable
- JS update selector .footer-brand dan .to-top sekaligus

## Update Log Sesi 21
- Footer punya dua versi teks:
  - Tidak scrollable (pendek): bird / (c) tahun
  - Scrollable (artikel panjang): bird / Rannndoms (R) dengan link + hover
- JS toggling class scrollable di html element, CSS yang switch
- Bird dan Rannndoms dua-duanya link ke x.com/rannndoms
- Bird hover warna Twitter, Rannndoms hover tanpa underline

## Update Log Sesi 21 revisi
- Fix CSS nyasar di luar </style> karena append >> ke style.html
- Hapus baris CSS yang muncul sebagai teks, re-insert di dalam </style>
- Pelajaran: JANGAN pakai >> ke style.html, harus pakai sed insert sebelum </style>
