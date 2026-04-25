# 🚀 GitPush Web

> **Solusi cepat push file ke GitHub tanpa ribet ketik perintah terminal.**
> Dirancang khusus untuk pengguna mobile, Termux, dan siapapun yang ingin alur push yang lebih nyaman.

GitPush Web adalah **GUI berbasis browser** untuk upload file dan folder ke repositori GitHub kamu.
Drag & drop file, ekstrak ZIP otomatis, dan push dalam satu klik — semua tanpa keluar dari browser.

![Tech](https://img.shields.io/badge/React-19-61dafb?style=flat-square&logo=react)
![Vite](https://img.shields.io/badge/Vite-7-646cff?style=flat-square&logo=vite)
![Tailwind](https://img.shields.io/badge/Tailwind-4-38bdf8?style=flat-square&logo=tailwindcss)

---

## ✨ Fitur Utama

- 🎨 **Dark Glassmorphism UI** dengan animasi neon halus
- 🔐 **Login via Personal Access Token** (atau OAuth opsional) — token tersimpan hanya di browser
- 📂 **Drag & drop** file individual, folder lengkap, atau ZIP archive
- 📦 **Ekstrak ZIP otomatis** di browser pakai JSZip
- 👁️ **Preview kode** untuk file teks (JS, CSS, MD, dll) sebelum push
- 🌿 **Pilih branch & path** target dengan mudah
- 🤖 **Saran AI** untuk pesan commit otomatis
- 📊 **Riwayat aktivitas** tersimpan di localStorage
- 🔒 **Zero-server-state** — tidak ada backend yang menyimpan token atau file kamu

---

## 🚀 Deploy ke Vercel (1 Klik)

Project sudah pre-configured dengan `vercel.json`. Cukup:

1. Push fork repo kamu ke GitHub.
2. Import ke [Vercel](https://vercel.com/new).
3. Vercel auto-detect framework dan deploy.

Selesai. Tidak ada environment variable wajib yang perlu di-set.

### (Opsional) Setup OAuth GitHub App

Default-nya GitPush Web pakai **Personal Access Token** untuk login (lebih simpel, tidak butuh
backend). Jika ingin pakai full OAuth flow:

1. Buat OAuth App di [GitHub Developer Settings](https://github.com/settings/developers).
   - **Homepage URL:** `https://your-app.vercel.app`
   - **Authorization callback URL:** `https://your-app.vercel.app/auth/callback`
2. Copy **Client ID**.
3. Di Vercel → Project Settings → Environment Variables, tambahkan:
   ```
   VITE_GITHUB_CLIENT_ID=Iv1.xxxxxxxxxxxxxxxx
   ```
4. Redeploy.

---

## 🛠️ Development

```bash
# Install deps
bun install

# Run dev server
bun run dev

# Build for production
bun run build

# Preview build
bun run preview
```

---

## 🔒 Keamanan & Privasi

- ❌ **Tidak ada server perantara.** Semua request berjalan langsung dari browser kamu ke `https://api.github.com`.
- ❌ **Token tidak pernah dikirim ke server kami.** Token disimpan hanya di `localStorage` browser.
- ✅ **HTTPS only.** Komunikasi browser ↔ GitHub terenkripsi.
- ✅ **Open source.** Kode dapat diaudit langsung.

> 💡 **Tips:** Selalu logout dari perangkat publik. Untuk keamanan maksimal, buat token dengan
> masa berlaku pendek (7–30 hari) dan revoke setelah selesai.

---

## 📦 Tech Stack

- **React 19** + **TypeScript**
- **TanStack Start / Router** — file-based routing & SSR
- **Vite 7** — build tool
- **Tailwind CSS 4** — styling
- **Framer Motion** — animasi smooth
- **Lucide Icons** — ikon yang clean
- **JSZip** — ekstraksi ZIP di browser
- **shadcn/ui** — komponen base
- **Sonner** — toast notification

---

## 💬 Dukungan

Gabung saluran WhatsApp untuk update fitur dan support:

👉 [Saluran WhatsApp GitPush Web](https://whatsapp.com/channel/0029VbBsAy17T8bbFQZ9y410)

---

## 📄 Lisensi

MIT — Bebas digunakan, dimodifikasi, dan didistribusikan ulang.
