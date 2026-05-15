# Laporan Penilaian Kelompok antek-antek-asing – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | antek-antek-asing |
| Repo | cc-kelompok-a-antek-antek-asing |
| Fase | M5 (Dockerfile) → M6 (Compose multi-container) → M7 (Optimasi & dokumentasi) |

---

### A. Penilaian Kelompok – Containerization

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **88** | **Backend `Dockerfile`:** multi-stage dengan pola virtualenv (builder install ke /opt/venv → final copy venv saja), non-root user `appuser`, `HEALTHCHECK` via `/health` dengan curl. **Frontend `Dockerfile`:** multi-stage Node→Nginx alpine, 3 build ARG (`VITE_API_URL`, `VITE_SPLINE_SCENE_URL`, `VITE_SPLINE_SCENE_URL_REGISTER`), custom `nginx.conf` di-copy, dist + public/avatars di-serve. Solid. |
| **M6 – Docker Compose multi-container** | 33% | **86** | `docker-compose.yml` 3 service. `healthcheck` Postgres (`pg_isready`) + healthcheck backend (`urllib.request.urlopen('/health')` — kreatif tanpa curl). `depends_on: condition: service_healthy` di backend (best practice). Named volume `pgdata`, custom network `cloudnet`. Image tag pre-built (`notyourkisee/antick-async-backend:latest`) — sudah ada di Docker Hub. Minus: `POSTGRES_PASSWORD: postgres123` hardcoded di compose. |
| **M7 – Optimasi & Production config** | 34% | **78** | Dokumentasi pendukung lengkap: `docs/DOCKER_GUIDE.md`, `docs/DOCKER-COMMANDS-CHEATSHEET.md`, `docs/docker-architecture.md`, `docs/image-comparison.md`. **Minus:** tidak ada `docker-compose.prod.yml` untuk override production (DEBUG=false, CORS production, port hiding DB) — gap signifikan vs best practice yang dicontohkan modul. Production `VITE_API_URL` masih commented di compose. |

**Nilai Kelompok: (88 + 86 + 78) / 3 = 84.00**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W5–W7)

> W5 = 23–29 Mar, W6 = 30 Mar – 5 Apr, W7 = 6–12 Apr.
> Catatan: **W5 zero commit** seluruh tim — minggu setup/diskusi atau libur Lebaran.

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| M. Fikri Haikal Ariadma | Haikal / FikriHaikal / ryota | 0 | 9 | 4 | **13** |
| Muhammad Athala Romero | Muhammad Athala Romero | 0 | 7 | 1 | **8** |
| Muhammad Bagas Setiawan | Muhammaad Bagas Setiawan | 0 | 3 | 2 | **5** |
| Nanda Aulia Putri | Nanda Aulia Putri | 0 | 0 | 1 | **1** |

---

### C. Penilaian Individual

#### 1. M. Fikri Haikal Ariadma (Lead DevOps)
- **Konsistensi (30%):** 2/3 minggu aktif (W5 kosong seluruh tim) → 75
- **Substansi (40%):** 13 commits — pemimpin fase ini. Backend Dockerfile, compose, healthcheck, docker-architecture docs → 88
- **Kesesuaian Peran (20%):** Sangat sesuai DevOps untuk fase Docker → 94
- **Kualitas Pesan (10%):** Cukup deskriptif → 78

**Nilai: (0.30×75 + 0.40×88 + 0.20×94 + 0.10×78) = 22.5 + 35.2 + 18.8 + 7.8 = 84.3 → 84**
**Grade: AB**

---

#### 2. Muhammad Athala Romero (Lead Backend)
- **Konsistensi (30%):** 2/3 minggu aktif → 72
- **Substansi (40%):** 8 commits backend hardening & Docker support → 78
- **Kesesuaian Peran (20%):** Backend → 82
- **Kualitas Pesan (10%):** Mix → 75

**Nilai: (0.30×72 + 0.40×78 + 0.20×82 + 0.10×75) = 21.6 + 31.2 + 16.4 + 7.5 = 76.7 → 77**
**Grade: AB**

---

#### 3. Muhammad Bagas Setiawan (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif → 70
- **Substansi (40%):** 5 commits; frontend Docker setup, nginx config → 72
- **Kesesuaian Peran (20%):** Frontend → 80
- **Kualitas Pesan (10%):** Generik → 70

**Nilai: (0.30×70 + 0.40×72 + 0.20×80 + 0.10×70) = 21.0 + 28.8 + 16.0 + 7.0 = 72.8 → 73**
**Grade: B**

---

#### 4. Nanda Aulia Putri (Lead QA & Docs)
- **Konsistensi (30%):** 1/3 minggu aktif → 50
- **Substansi (40%):** 1 commit (W7) → 50
- **Kesesuaian Peran (20%):** Walaupun docs Docker tersedia, kontribusinya minim di fase ini → 60
- **Kualitas Pesan (10%):** → 65

**Nilai: (0.30×50 + 0.40×50 + 0.20×60 + 0.10×65) = 15.0 + 20.0 + 12.0 + 6.5 = 53.5 → 54**
**Grade: BC**

> ⚠️ Turun signifikan dari Fase 1 (84) ke Fase 2 (54). Catatan: docs Docker (DOCKER_GUIDE, image-comparison) mungkin dibuat di luar minggu evaluasi atau di-commit oleh anggota lain — perlu konfirmasi.

---

### D. Ringkasan untuk Gradebook

**C05 — Tugas terstruktur optimasi Docker image & Compose (4%):** semua anggota **84**

**C06 — Kontribusi & progres mingguan via Git commit log (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231059 | Muhammad Athala Romero | **77** |
| 10231061 | Muhammad Bagas Setiawan | **73** |
| 10231063 | Muhammad Fikri Haikal Ariadma | **84** |
| 10231067 | Nanda Aulia Putri | **54** |
