# Laporan Penilaian Kelompok awit – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | awit |
| Repo | cc-kelompok-a-awit |
| Fase | M5 (Dockerfile) → M6 (Compose) → M7 (Optimasi + Production) |

---

### A. Penilaian Kelompok – Containerization

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **92** | **Backend `Dockerfile`:** multi-stage dengan pola venv (builder install ke /opt/venv → final copy), dedicated copy `curl` + 7 shared libs untuk healthcheck (lebih granular dari kelompok lain), `postgresql-client` untuk `pg_isready`. Startup script support. **Frontend `Dockerfile`:** multi-stage Node 18→Nginx alpine, `npm ci` clean install, build ARG `VITE_API_URL`, custom nginx.conf. Dokumentasi: `backend/MULTISTAGE_BUILD.md` + `backend/STARTUP_SCRIPT.md`. |
| **M6 – Docker Compose multi-container** | 33% | **88** | `docker-compose.yml` 3 services dengan healthcheck, named volume, custom network `cloudnet`. Sesuai standar. |
| **M7 – Optimasi & Production config** | 34% | **92** | `docker-compose.prod.yml` profesional: `DEBUG=false`, `CORS_ORIGINS=${PROD_CORS_ORIGINS}` (env var, bukan hardcoded), `restart: unless-stopped`, `ports: !reset []` untuk hide DB. Dokumentasi `docs/image-comparison-modul6.md` + `docs/docker-architecture.md`. |

**Nilai Kelompok: (92 + 88 + 92) / 3 = 90.67 → 91**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W5–W7)

> W5 = 23–29 Mar, W6 = 30 Mar – 5 Apr, W7 = 6–12 Apr.
> Catatan: **W5 zero commit** seluruh tim (kemungkinan libur Lebaran).

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| Varrel Kaleb Ropard Pasaribu | VarrelKaleb / unknown | 0 | 5 | 0 | **5** |
| Adam Ibnu Ramadhan | adamimir | 0 | 1 | 2 | **3** |
| Adhyasta Firdaus | Adhyasta Firdaus | 0 | 2 | 0 | **2** |
| Alfian Fadillah Putra | Alfian Fadillah Putra | 0 | 1 | 1 | **2** |
| Adonia Azarya Tamalonggehe | Adonia Azarya Tamalonggehe | 0 | 1 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Varrel Kaleb Ropard Pasaribu (Lead DevOps & Container)
- **Konsistensi (30%):** 1/3 minggu aktif (W6 only, W5 universal kosong) → 78
- **Substansi (40%):** 5 commits — burst di W6 untuk Dockerfile + Compose setup → 80
- **Kesesuaian Peran (20%):** 100% containerization → 92
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×78 + 0.40×80 + 0.20×92 + 0.10×78) = 23.4 + 32.0 + 18.4 + 7.8 = 81.6 → 82**
**Grade: AB**

---

#### 2. Adam Ibnu Ramadhan (Lead Backend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 3 commits backend hardening untuk Docker → 70
- **Kesesuaian Peran (20%):** Backend → 80
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×72 + 0.40×70 + 0.20×80 + 0.10×78) = 21.6 + 28.0 + 16.0 + 7.8 = 73.4 → 73**
**Grade: B**

---

#### 3. Alfian Fadillah Putra (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 2 commits → 60
- **Kesesuaian Peran (20%):** Frontend Docker → 78
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×72 + 0.40×60 + 0.20×78 + 0.10×75) = 21.6 + 24.0 + 15.6 + 7.5 = 68.7 → 69**
**Grade: B**

---

#### 4. Adhyasta Firdaus (Lead CI/CD & Deployment)
- **Konsistensi (30%):** 1/3 minggu aktif → 55
- **Substansi (40%):** 2 commits — role CI/CD belum F2 fokus → 60
- **Kesesuaian Peran (20%):** → 65
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×55 + 0.40×60 + 0.20×65 + 0.10×75) = 16.5 + 24.0 + 13.0 + 7.5 = 61.0 → 61**
**Grade: BC**

---

#### 5. Adonia Azarya Tamalonggehe (Lead QA & Documentation)
- **Konsistensi (30%):** 1/3 minggu aktif → 50
- **Substansi (40%):** 1 commit → 50
- **Kesesuaian Peran (20%):** → 60
- **Kualitas Pesan (10%):** → 70

**Nilai: (0.30×50 + 0.40×50 + 0.20×60 + 0.10×70) = 15.0 + 20.0 + 12.0 + 7.0 = 54.0 → 54**
**Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C05 — Tugas terstruktur optimasi Docker image & Compose (4%):** semua anggota **91**

**C06 — Kontribusi & progres mingguan via Git commit log (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | **73** |
| 10231005 | Adhyasta Firdaus | **61** |
| 10231007 | Adonia Azarya Tamalonggehe | **54** |
| 10231009 | Alfian Fadillah Putra | **69** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | **82** |
