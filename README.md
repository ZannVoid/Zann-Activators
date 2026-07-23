# 🔑 Zann Activators

> **One-Liner** — Aktivasi Windows & Office dalam sekali perintah
>
> ```powershell
> irm https://get.zannvoid.my.id | iex
> ```

**Zann Activators** adalah tools aktivasi Windows & Office yang cepat, ringan, dan mudah digunakan. Dibangun dengan fokus pada efisiensi, kompatibilitas lintas versi, dan kemudahan akses bagi pengguna rumahan maupun teknisi.

Proyek ini terinspirasi dari kebutuhan akan solusi aktivasi yang transparan, open-source, dan tidak bergantung pada software pihak ketiga yang mencurigakan. **Semua kode dapat diperiksa, dimodifikasi, dan didistribusikan ulang** sesuai kebutuhan.

---

## 📋 Daftar Isi

- [Fitur Utama](#-fitur-utama)
- [Quick Start](#-quick-start)
- [Metode Aktivasi](#-metode-aktivasi)
- [Struktur Proyek](#-struktur-proyek)
- [Keamanan & Verifikasi](#-keamanan--verifikasi)
- [Troubleshooting](#-troubleshooting)
- [Infrastruktur](#-infrastruktur)
- [Kontribusi](#-kontribusi)
- [Lisensi & Disclaimer](#-lisensi--disclaimer)

---

## 🚀 Fitur Utama

| Fitur | Deskripsi | Target |
|-------|-----------|--------|
| **HWID Activation** | Aktivasi permanen Windows menggunakan digital license | Windows 10/11 |
| **Ohook Activation** | Aktivasi Office dengan metode hooking yang stabil | Office 2016-2024 |
| **TSforge Activation** | Aktivasi offline berbasis trusted store | Win/Office/ESU |
| **Online KMS** | Aktivasi dengan renewal task otomatis | Volume licenses |
| **Status Checker** | Lihat detail status lisensi Windows & Office | Semua versi |
| **Edition Changer** | Ubah edisi Windows/Office (Home ↔ Pro, dll) | All editions |
| **Auto Troubleshoot** | Perbaikan WMI, SPP, licensing, dan WPA registry | System repair |

---

## ⚡ Quick Start

### Persyaratan Sistem

- ✓ Windows 7 / 8 / 8.1 / 10 / 11
- ✓ PowerShell (bawaan Windows)
- ✓ Koneksi internet (untuk download script)
- ✓ Administrator privileges

### Instalasi & Eksekusi

**Metode 1: One-Liner (Direkomendasikan)** ⭐

Buka PowerShell sebagai Administrator, lalu jalankan:

```powershell
irm https://get.zannvoid.my.id | iex
```

**Metode 2: GitHub Raw**

```powershell
irm https://raw.githubusercontent.com/Zannvoid/Zann-Activators/main/ZannActivator.ps1 -OutFile ZannActivator.ps1
.\ZannActivator.ps1
```

**Metode 3: Cloudflare Worker (Backup)**

```powershell
irm https://zannvoid.asepterbakarbakar.workers.dev | iex
```

**Metode 4: URL Shortener**

```powershell
irm https://tinyurl.com/zannact | iex
```

> **💡 Tips:** Klik kanan PowerShell → Run as Administrator untuk hasil optimal.

---

## 🧪 Metode Aktivasi

Setelah menjalankan script, Anda akan melihat menu interaktif dengan pilihan metode aktivasi berikut:

### 1️⃣ HWID Activation

**Target:** Windows 10 / 11

**Keunggulan:**
- Aktivasi permanen (tidak perlu renew)
- Mirip aktivasi official dari Microsoft
- Terhubung ke digital license account

**Cocok untuk:** Pengguna rumahan, PC pribadi, developer

---

### 2️⃣ Ohook Activation

**Target:** Office 2016 / 2019 / 2021 / 2024

**Keunggulan:**
- Aktivasi permanen dengan method hooking
- Kompatibel dengan berbagai edisi Office
- Stable dan reliable

**Cocok untuk:** Pengguna Office rumahan & profesional

---

### 3️⃣ TSforge Activation

**Target:** Windows / Office / ESU (Extended Security Updates)

**Sub-metode:**
- **ZeroCID** — Offline, tidak perlu internet
- **StaticCID** — Online dengan Static CID
- **KMS4k** — Offline license (4000+ tahun)

**Keunggulan:**
- Metode offline tersedia
- Ideal untuk Windows 7/8
- Cocok untuk environment tanpa koneksi stabil

**Cocok untuk:** Server, offline systems, Windows 7/8 legacy

---

### 4️⃣ Online KMS

**Target:** Windows / Office (Volume licenses)

**Keunggulan:**
- Aktivasi 180 hari dengan renewal task otomatis
- Cocok untuk multiple devices
- Renewal terjadi di background

**Cocok untuk:** Enterprise, banyak perangkat, volume licensing

---

### 5️⃣ Utility Tools

**Troubleshoot & Maintenance:**

- 🔧 DISM Restore Health — Perbaiki Windows image corruption
- 🔧 SFC Scan Now — System File Checker
- 🔧 Fix WMI — Windows Management Instrumentation
- 🔧 Fix Licensing — ClipSVC + SPP + OSPP services
- 🔧 Fix WPA Registry — Windows Product Activation registry

---

## 📁 Struktur Proyek

```
Zann-Activators/
│
├── README.md                          # Dokumentasi proyek
├── LICENSE                            # MIT License
│
├── ZannActivator.ps1                  # PowerShell loader (one-liner target)
│   └── Downloads ZannActivators.cmd ke temp folder
│       └── Menjalankan dengan hak admin
│
└── Zann/
    └── All-In-One-Version-KL/
        └── ZannActivators.cmd         # Script utama (batch file)
            ├── HWID Activation logic
            ├── Ohook Activation logic
            ├── TSforge Activation logic
            ├── Online KMS logic
            ├── Status checking
            ├── Edition changer
            └── Troubleshoot tools
```

### Penjelasan Komponen

**ZannActivator.ps1** (PowerShell Loader)
- Entry point dari one-liner
- Download ZannActivators.cmd ke `%temp%`
- Request admin privileges jika perlu
- Execute script utama dengan hak admin
- Clean up temp file setelah eksekusi

**ZannActivators.cmd** (Main Script)
- Core logic semua metode aktivasi
- Interaktif menu-driven interface
- Error handling & logging
- Registry manipulation & service management

---

## 🔐 Keamanan & Verifikasi

### SHA256 Hash Verification

**ZannActivators.cmd:**
```
AE1FA3A95BDAA9703C37286E23F6272F0273BC24A3946A92A3989385C8685BCD
```

### Cara Verifikasi Integritas File

```powershell
Get-FileHash ZannActivators.cmd -Algorithm SHA256
```

Bandingkan hasil dengan hash di atas. **Jika tidak cocok, jangan jalankan script** — laporkan ke developer.

### Praktik Keamanan

✓ Open-source — semua kode dapat diperiksa di GitHub  
✓ Tidak ada obfuscation — kode transparan & readable  
✓ Minimal dependencies — hanya PowerShell bawaan  
✓ No telemetry — tidak ada tracking/data collection  
✓ No bloatware — hanya tools aktivasi yang diperlukan  

---

## 🛠️ Troubleshooting

### Error: "The remote name could not be resolved"

**Penyebab:** DNS resolution failure

**Solusi:**
```cmd
ipconfig /flushdns
```

Coba jalankan ulang script setelah flushing DNS cache.

---

### Error: "SSL/TLS secure channel" atau Status 522

**Penyebab:** Koneksi ke server terblokir atau timeout

**Solusi:**
1. Pastikan koneksi internet stabil
2. Coba gunakan metode alternatif:
   - Cloudflare Worker URL
   - GitHub Raw URL
   - URL Shortener
3. Periksa firewall/antivirus — pastikan tidak memblokir Cloudflare

---

### Error: "PowerShell not in Full Language Mode"

**Penyebab:** Restricted PowerShell execution policy

**Solusi:**
```powershell
# Jalankan PowerShell sebagai Administrator
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

Kemudian jalankan script lagi.

---

### Error: "Windows Defender flagged as Hacktool"

**Penyebab:** Script dibaca sebagai potentially unwanted program (PUP)

**Solusi:**
1. Buka Windows Security
2. Klik Virus & threat protection
3. Klik Manage settings
4. Scroll ke bawah → Add or remove exclusions
5. Tambahkan folder script sebagai exclusion
6. Restore file dari quarantine jika perlu

---

### Script Error / Menu Tidak Muncul

**Solusi:**
1. Pastikan menggunakan PowerShell terbaru (Windows PowerShell 5.1+)
2. Jalankan sebagai Administrator
3. Coba metode alternatif (Worker URL atau GitHub Raw)
4. Periksa log di event viewer untuk error details

---

## 🌐 Infrastruktur

### Domain & Endpoint

| Domain | Fungsi | Provider |
|--------|--------|----------|
| `zannvoid.my.id` | Homepage & informasi proyek | Custom domain |
| `get.zannvoid.my.id` | One-liner loader (target `irm ... \| iex`) | Cloudflare DNS |
| `zannvoid.asepterbakarbakar.workers.dev` | Backup loader (Cloudflare Worker) | Cloudflare Workers |

### Stack Teknologi

- **Loader:** PowerShell 5.1+
- **Core:** Batch script (.cmd)
- **Hosting:** Cloudflare Workers (serverless)
- **DNS:** Cloudflare (managed DNS)
- **Repository:** GitHub (source code & releases)

### Deployment Architecture

```
                          ┌─────────────────────┐
                          │  One-liner Request  │
                          │ irm ... | iex       │
                          └──────────┬──────────┘
                                     │
                    ┌────────────────┼────────────────┐
                    │                │                │
            ┌───────▼──────┐  ┌──────▼────────┐  ┌──▼───────────┐
            │ get.zannvoid │  │  GitHub Raw   │  │  Shortener   │
            │   .my.id     │  │   Endpoint    │  │   Service    │
            │ (DNS alias)  │  │               │  │              │
            └───────┬──────┘  └──────┬────────┘  └──┬───────────┘
                    │                │             │
                    └────────────────┼─────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  ZannActivator.ps1     │
                         │  (PowerShell Loader)   │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  Download to %temp%    │
                         │  ZannActivators.cmd    │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  Request Admin Privs   │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  Execute as Admin      │
                         │  Show interactive menu │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  User selects method   │
                         │  (HWID/Ohook/TSforge) │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  Execute activation    │
                         │  Display result        │
                         └───────────┬────────────┘
                                     │
                         ┌───────────▼────────────┐
                         │  Clean up temp files   │
                         │  Exit gracefully       │
                         └────────────────────────┘
```

---

## 🤝 Kontribusi

Proyek ini dikembangkan secara independen. Namun, saran, laporan bug, dan masukan konstruktif sangat dihargai!

### Cara Berkontribusi

1. **Fork** repositori ke akun GitHub Anda
2. **Buat branch** untuk fitur atau bugfix:
   ```bash
   git checkout -b fitur-keren
   ```
3. **Commit** perubahan dengan pesan yang deskriptif:
   ```bash
   git commit -m "Add: deskripsi fitur atau perbaikan"
   ```
4. **Push** ke branch Anda:
   ```bash
   git push origin fitur-keren
   ```
5. **Buka Pull Request** dengan penjelasan lengkap

### Catatan

- Semua kontribusi akan ditinjau & diuji sebelum merge
- Ikuti code style yang sudah ada
- Pastikan tidak ada breaking changes
- Test di berbagai Windows version jika memungkinkan

---

## 📜 Lisensi & Disclaimer

### Lisensi

Proyek ini dilisensikan di bawah **MIT License** — silakan gunakan, modifikasi, dan distribusikan ulang dengan **atribusi yang sesuai**.

[Lihat file LICENSE untuk detail lengkap]

### ⚠️ Disclaimer

**Penting:** Baca sebelum menggunakan tools ini.

1. **Tools untuk tujuan edukasi**  
   Tools ini dibuat untuk tujuan edukasi dan penggunaan pribadi.

2. **Tanggung jawab pengguna**  
   Pengguna bertanggung jawab penuh atas penggunaan alat ini dan konsekuensinya.

3. **Aktivasi perangkat lunak**  
   Aktivasi perangkat lunak secara ilegal melanggar ketentuan layanan Microsoft dan penyedia software lainnya. Pengguna harus mematuhi peraturan lisensi yang berlaku di yurisdiksi mereka.

4. **Tidak ada garansi**  
   Pengembang tidak bertanggung jawab atas:
   - Kerusakan pada sistem
   - Kehilangan data
   - Konsekuensi hukum
   - Masalah teknis apapun

5. **Penggunaan non-commercial**  
   Tools ini hanya boleh digunakan untuk personal/non-commercial purposes. Penggunaan commercial atau redistribusi tanpa izin tidak diperkenankan.

**Gunakan dengan bijak dan ikuti peraturan lokal Anda.**

---

## 📞 Kontak & Dukungan

| Channel | Link |
|---------|------|
| **GitHub Issues** | [Zannvoid/Zann-Activators/issues](https://github.com/Zannvoid/Zann-Activators/issues) |
| **Homepage** | [zannvoid.my.id](https://zannvoid.my.id) |
| **Email** | [contact@zannvoid.my.id] |

---

## 📊 Statistik Proyek

- **Repository:** [github.com/Zannvoid/Zann-Activators](https://github.com/Zannvoid/Zann-Activators)
- **License:** MIT
- **Status:** Active Development
- **Last Updated:** 2026
- **Supported Windows:** 7, 8, 8.1, 10, 11
- **Supported Office:** 2016, 2019, 2021, 2024

---

<div align="center">

### Made with ❤️ and ☕

© 2026 **Zann Activators**

[⭐ Star](https://github.com/Zannvoid/Zann-Activators) • [🐛 Report Issue](https://github.com/Zannvoid/Zann-Activators/issues) • [💡 Request Feature](https://github.com/Zannvoid/Zann-Activators/discussions)

</div>

---

## 🗺️ Roadmap

### v1.0 (Current)
- ✅ HWID Activation
- ✅ Ohook Activation  
- ✅ TSforge Activation
- ✅ Online KMS
- ✅ Troubleshoot Tools

### v1.1 (Planned)
- 🔄 GUI-based interface
- 🔄 Activation verification tools
- 🔄 Advanced logging & debug mode
- 🔄 Multi-language support

### v2.0 (Future)
- 📋 TBD

---

## FAQ

**Q: Apakah tools ini aman?**  
A: Ya, tools ini open-source dan dapat diperiksa. Tidak ada malware atau tracking. Namun, selalu scan dengan antivirus lokal Anda sebelum jalankan.

**Q: Berapa lama aktivasi bertahan?**  
A: Tergantung metode — HWID & Ohook permanen, KMS renewal setiap 180 hari.

**Q: Bisakah saya gunakan di VM/VPS?**  
A: Ya, tapi beberapa metode (HWID) mungkin tidak bekerja sempurna di VM. TSforge & KMS lebih cocok untuk VM.

**Q: Apakah legal?**  
A: Tools ini disediakan untuk edukasi. Penggunaan untuk aktivasi ilegal melanggar hukum — pastikan Anda memiliki lisensi yang sah atau use case yang justified.

**Q: Bagaimana jika ada error?**  
A: Lihat section Troubleshooting atau buka issue di GitHub.

---

**Last Updated:** 24 Juli 2026  
**Maintained by:** Zann Activators Team
