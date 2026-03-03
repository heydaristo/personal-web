<div align="center">

# ⚡ Heydaristo — Personal Portfolio

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)](https://nginx.org/)

**Website portfolio personal dengan tema cyberpunk dark — tanpa framework, tanpa dependencies, murni HTML/CSS/JS.**

🌐 **Live:** [heydaristo.my.id](https://heydaristo.my.id)

</div>

---

## 📸 Preview

> **Screenshot halaman utama (Hero Section)**

![Hero Section](https://raw.githubusercontent.com/heydaristo/personal-web/main/assets/img/preview/hero.png)

> **Terminal & Projects Section**

![Projects Section](https://raw.githubusercontent.com/heydaristo/personal-web/main/assets/img/preview/projects.png)

> **AI Chat Assistant**

![AI Chat](https://raw.githubusercontent.com/heydaristo/personal-web/main/assets/img/preview/aichat.png)

> *(Tambahkan screenshot kamu sendiri ke folder `assets/img/preview/` setelah deploy)*

---

## ✨ Fitur

### 🎨 UI & Animasi
| Fitur | Deskripsi |
|---|---|
| **Page Loader** | Animasi loading bar dengan glitch effect saat pertama buka |
| **Custom Cursor** | Cursor dot + ring dengan smooth lag & sparkle trail |
| **Parallax Orbs** | Background orb ungu & cyan yang bergerak floating |
| **Particle Network** | Canvas partikel yang saling terhubung secara dinamis |
| **Scroll Progress Bar** | Bar tipis di atas halaman yang menunjukkan progress scroll |
| **Glitch Text Effect** | Nama "Heydar Risto" punya glitch animation saat di-hover |
| **Typed Text** | Animasi typing kata-kata berganti di hero section |
| **Hero Terminal** | Animasi terminal yang "mengetik sendiri" di hero section |
| **3D Tilt Card** | Project card miring 3D mengikuti gerakan mouse |
| **Scroll Reveal** | Elemen muncul dengan animasi saat masuk viewport |
| **Counter Animasi** | Angka stat (3+ tahun, 10+ project) animasi naik |

### 🧭 Navigasi
| Fitur | Deskripsi |
|---|---|
| **Sticky Navbar** | Navbar mengecil & makin pekat saat scroll ke bawah |
| **Active Nav Link** | Link nav otomatis highlight sesuai section yang sedang dilihat |
| **Hamburger Menu** | Mobile menu dengan animasi slide dari kanan |
| **Back to Top Button** | Tombol muncul setelah scroll 400px |

### 🤖 AI Chat Assistant
- Chat widget floating di kanan bawah
- **Tanpa API / tanpa backend** — murni keyword-based engine
- Bisa jawab pertanyaan soal: siapa Heydaristo, projects, tech stack, hire info, kontak, anime, dan lainnya
- Typing indicator animasi
- Quick suggestion buttons
- Fully offline & gratis

### 🗂️ Projects Section
- **Filter by tag**: All / Node.js / PHP / Android / Laravel
- Animasi card filter langsung tanpa reload
- 3D tilt + shine effect per card

### 🔧 Fitur Lainnya
| Fitur | Deskripsi |
|---|---|
| **Copy Email** | Satu klik copy email ke clipboard + toast notification |
| **Toast Notification** | Notifikasi kecil muncul di bawah layar |
| **Konami Code** | Easter egg tersembunyi: ↑↑↓↓←→←→BA 🎮 |
| **SEO Ready** | Meta tag lengkap: og:title, og:description, canonical, robots |
| **Fully Responsive** | Tampilan optimal di mobile, tablet, dan desktop |

---

## 📁 Struktur File

```
personal-web/
├── index.html          # File utama (semua CSS & JS inline)
├── robots.txt          # Instruksi untuk search engine crawler
├── sitemap.xml         # Sitemap untuk SEO
└── assets/
    ├── img/
    │   ├── logo.svg    # Favicon/logo website
    │   └── preview/    # Screenshot untuk README (opsional)
    └── ...
```

---

## 🚀 Cara Pasang

### Opsi 1 — Buka Langsung (Tanpa Server)
Paling simpel, cocok untuk preview lokal:

```bash
# Clone repo
git clone https://github.com/heydaristo/personal-web.git

# Masuk folder
cd personal-web

# Buka di browser
# Tinggal klik dua kali file index.html
# atau drag & drop ke browser
```

---

### Opsi 2 — Deploy ke VPS dengan Nginx (Cara Heydaristo)

#### 1. Upload file ke server
```bash
# Dari lokal ke VPS pakai SCP
scp -r ./personal-web user@IP_VPS:/var/www/heydaristo
```

#### 2. Install & konfigurasi Nginx
```bash
# Install Nginx (Ubuntu/Debian)
sudo apt update && sudo apt install nginx -y

# Buat konfigurasi virtual host
sudo nano /etc/nginx/sites-available/heydaristo
```

Isi config Nginx:
```nginx
server {
    listen 80;
    listen [::]:80;
    server_name heydaristo.my.id www.heydaristo.my.id;
    root /var/www/heydaristo;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }

    # Gzip compression
    gzip on;
    gzip_types text/html text/css application/javascript;
}
```

```bash
# Aktifkan config
sudo ln -s /etc/nginx/sites-available/heydaristo /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
```

#### 3. Pasang SSL (HTTPS gratis dengan Certbot)
```bash
sudo apt install certbot python3-certbot-nginx -y
sudo certbot --nginx -d heydaristo.my.id -d www.heydaristo.my.id
```

✅ Website sudah live dengan HTTPS!

---

### Opsi 3 — Deploy ke GitHub Pages (Gratis)

```bash
# Push ke GitHub dulu
git add .
git commit -m "initial commit"
git push -u origin main
```

Lalu di GitHub:
1. Buka **Settings** → **Pages**
2. Source: pilih **main branch** → folder **/ (root)**
3. Klik **Save**
4. Website live di: `https://username.github.io/personal-web`

---

### Opsi 4 — Deploy ke Netlify (Drag & Drop)
1. Buka [netlify.com](https://netlify.com)
2. Drag & drop folder `personal-web` ke dashboard
3. Selesai — dapat subdomain gratis `*.netlify.app`

---

## ✏️ Cara Kustomisasi

### Ganti Nama & Info
Buka `index.html`, cari dan ganti bagian ini:

```html
<!-- Nama di hero -->
<span class="line1 glitch-text" data-text="Heydar">Heydar</span>
<span class="line2 glitch-text" data-text="Risto">Risto</span>

<!-- Deskripsi -->
<p class="hero-desc">Developer, <span class="accent">bot creator</span>, ...</p>

<!-- Email -->
heydaristo@gmail.com

<!-- Nomor WA -->
https://wa.me/6283192928460

<!-- GitHub -->
https://github.com/heydaristo
```

### Tambah / Edit Project
Cari bagian `<div class="projects-grid">` lalu duplikat salah satu `.project-card`:

```html
<div class="project-card reveal" data-tags="Node.js TypeScript">
  <div class="tilt-shine"></div>
  <div class="project-icon">🔥</div>
  <div class="project-name">Nama Project</div>
  <div class="project-desc">Deskripsi project kamu di sini.</div>
  <div class="project-tags">
    <span class="tag">Node.js</span>
    <span class="tag">TypeScript</span>
  </div>
  <a href="https://github.com/..." class="project-link" target="_blank">View on GitHub →</a>
</div>
```

> ⚠️ Pastikan `data-tags` sesuai dengan tombol filter yang ada (atau tambahkan filter baru di `#filterBar`).

### Update AI Chat
Cari objek `KNOWLEDGE` di bagian JavaScript, tambahkan rule baru:

```js
{
  id: 'topik_baru',
  keywords: ['kata', 'kunci', 'yang', 'relevan'],
  responses: [
    'Jawaban pertama...',
    'Jawaban alternatif kedua...'
  ]
}
```

---

## 🛠️ Tech Stack

| Layer | Teknologi |
|---|---|
| Markup | HTML5 Semantic |
| Styling | CSS3 (Variables, Grid, Flexbox, Animations) |
| Logic | Vanilla JavaScript (ES6+) |
| Font | Google Fonts (Space Mono, Syne, JetBrains Mono) |
| Web Server | Nginx |
| Hosting | VPS |

> Zero dependencies. Zero npm. Zero frameworks. Zero cost. ⚡

---

## 📄 Lisensi

MIT License — bebas dipakai, dimodifikasi, dan didistribusikan.
Kredit ke [Heydaristo](https://heydaristo.my.id) sangat diapresiasi tapi tidak wajib 🙏

---

<div align="center">

built with ❤️ & caffeine — **[heydaristo.my.id](https://heydaristo.my.id)**

</div>
