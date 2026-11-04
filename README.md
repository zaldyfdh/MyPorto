# MyPorto

Website portofolio Zaldy Fadhlulrohman, mahasiswa Computer Engineering. Satu halaman dengan gaya neo-brutalist, dibuat dengan React dan Vite.

## Fitur

- **Bagian halaman:** Hero, About (dengan Education dan statistik), Skills, Projects, Contact, Footer.
- **Dark mode:** tombol petir di navbar. Pilihan tema disimpan di `localStorage`.
- **Skills:** 11 skill dengan filter ALL, DEVELOPMENT, DESIGN, MACHINE LEARNING, dan TOOLS.
- **Projects:** 3 project dengan filter ALL, UI/UX DESIGN, WEB, dan DESIGN.
- **Galeri project:** tombol *VIEW PROJECT* membuka jendela gambar dengan tombol PREV/NEXT dan indikator titik. Keyboard: `Esc` menutup, panah kiri/kanan mengganti gambar. Gambar yang filenya belum ada dilewati otomatis.
- **Contact:** formulir (nama, email, pesan) yang dikirim lewat [Formspree](https://formspree.io), dan tombol yang membuka Gmail dengan penerima, subjek, dan isi pesan sudah terisi. Link GitHub, LinkedIn, dan Instagram ada di bagian ini dan di footer.
- **Animasi:** elemen muncul saat di-scroll (`src/hooks/useScrollReveal.js`), efek hover pada tombol dan label, serta lampu berkedip di bingkai foto Hero. Animasi muncul-saat-scroll tidak dijalankan jika perangkat memakai pengaturan *reduce motion*.
- **Responsif:** menu hamburger pada layar ≤ 900px.
- Tombol **TOP** yang menempel di kanan bawah layar.

## Teknologi

| | Versi |
|---|---|
| React | 19 |
| Vite | 7 |
| `@vitejs/plugin-react` | 5 |
| react-icons | 5 |

Gaya memakai CSS Modules, dengan variabel warna dan tema di `src/index.css`. Font Space Grotesk dan JetBrains Mono dimuat dari Google Fonts. Deploy memakai Vercel (`vercel.json`).

## Menjalankan di komputer

Butuh Node.js `^20.19.0` atau `>=22.12.0` (syarat Vite 7).

```bash
git clone https://github.com/zaldyfdh/MyPorto.git
cd MyPorto
npm install
npm run dev
```

| Perintah | Fungsi |
|---|---|
| `npm run dev` | Server pengembangan |
| `npm run build` | Build produksi ke folder `dist` |
| `npm run preview` | Menjalankan hasil build secara lokal |

## Struktur folder

```
├── public/
│   ├── favicon.svg
│   └── images/
│       ├── profile.jpg          # foto di Hero
│       └── projects/            # sampul kartu dan gambar galeri
├── src/
│   ├── components/              # CSS Modules tiap bagian, SafeImage.jsx
│   ├── data/
│   │   ├── siteData.js          # nama, link sosial, email, menu navbar
│   │   ├── skillsData.js        # daftar skill
│   │   └── projectsData.js      # daftar project dan gambar galeri
│   ├── hooks/
│   │   └── useScrollReveal.js
│   ├── sections/                # Navbar, Hero, About, Skills, Projects,
│   │                            # ProjectModal, Connect, Footer
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── index.html
├── vercel.json
└── vite.config.js
```