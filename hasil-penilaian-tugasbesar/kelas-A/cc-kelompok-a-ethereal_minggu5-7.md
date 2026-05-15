# Laporan Penilaian Kelompok ethereal – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ethereal |
| Repo | cc-kelompok-a-ethereal |
| Fase | M5 (Dockerfile) → M6 (Compose) → M7 (Optimasi + Production) |

---

### A. Penilaian Kelompok – Containerization

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **88** | Backend & frontend Dockerfile tersedia. Helper scripts di root: `dev.sh`, `docker.sh`, `setup.sh`, `scripts/`, `Makefile` — sangat memudahkan dev experience. |
| **M6 – Docker Compose multi-container** | 33% | **86** | Standard 3-service compose dengan healthcheck. |
| **M7 – Optimasi & Production config** | 34% | **88** | `docker-compose.prod.yml` profesional: `ports: !reset []` untuk hide DB, `DEBUG=false`, `CORS_ORIGINS=https://kelarin-app.com`, `restart: always`. Dokumentasi: `docs/docker-architecture.md` + `docs/image-comparison.md` (+ PDF). |

**Nilai Kelompok: (88 + 86 + 88) / 3 = 87.33 → 87**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W5–W7)

> W5 = 23–29 Mar, W6 = 30 Mar – 5 Apr, W7 = 6–12 Apr. **W5 zero commit** seluruh tim (libur Lebaran).

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| Amazia Devid Saputra | Devid | 0 | 2 | 4 | **6** |
| Ansellma Tita Pakartiwuri | ansel / secretceremony | 0 | 0 | 6 | **6** |
| Andini Permata Sari | gitandys | 0 | 1 | 4 | **5** |
| Alsha Dwi Cahya | dwialsha | 0 | 1 | 3 | **4** |
| Tiya Mitra Ayu | Tiyamitrayu | 0 | 1 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Alsha Dwi Cahya (Lead Container)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 4 commits — role container prime time → 75
- **Kesesuaian Peran (20%):** 100% match role di fase Docker → 92
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×72 + 0.40×75 + 0.20×92 + 0.10×78) = 21.6 + 30.0 + 18.4 + 7.8 = 77.8 → 78**
**Grade: AB**

---

#### 2. Amazia Devid Saputra (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 6 commits → 76
- **Kesesuaian Peran (20%):** Frontend Docker → 80
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×72 + 0.40×76 + 0.20×80 + 0.10×78) = 21.6 + 30.4 + 16.0 + 7.8 = 75.8 → 76**
**Grade: AB**

---

#### 3. Andini Permata Sari (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 5 commits docs Docker → 72
- **Kesesuaian Peran (20%):** Docs → 84
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×72 + 0.40×72 + 0.20×84 + 0.10×75) = 21.6 + 28.8 + 16.8 + 7.5 = 74.7 → 75**
**Grade: B**

---

#### 4. Ansellma Tita Pakartiwuri Putri (Lead Deploy & CI/CD)
- **Konsistensi (30%):** 1/3 minggu aktif (W7 only) → 60
- **Substansi (40%):** 6 commits burst W7 → 76
- **Kesesuaian Peran (20%):** CI/CD role belum F2 prime → 75
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×60 + 0.40×76 + 0.20×75 + 0.10×78) = 18.0 + 30.4 + 15.0 + 7.8 = 71.2 → 71**
**Grade: B**

---

#### 5. Tiya Mitra Ayu (Lead Backend)
- **Konsistensi (30%):** 1/3 minggu aktif → 50
- **Substansi (40%):** 1 commit → 50
- **Kesesuaian Peran (20%):** Backend → 65
- **Kualitas Pesan (10%):** → 70

**Nilai: (0.30×50 + 0.40×50 + 0.20×65 + 0.10×70) = 15.0 + 20.0 + 13.0 + 7.0 = 55.0 → 55**
**Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C05 — Tugas terstruktur optimasi Docker image & Compose (4%):** semua anggota **87**

**C06 — Kontribusi & progres mingguan via Git commit log (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | **78** |
| 10231013 | Amazia Devid Saputra | **76** |
| 10231015 | Andini Permata Sari | **75** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | **71** |
| 10231088 | Tiya Mitra Ayu | **55** |
