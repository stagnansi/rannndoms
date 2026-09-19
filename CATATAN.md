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
