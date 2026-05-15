# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Repo | cc-kelompok-a-hexacore |
| Fase | M5 (Dockerfile) → M6 (Compose multi-container) → M7 (Optimasi & networking) |

---

### A. Penilaian Kelompok – Containerization (Kualitas Deliverable)

> 3 kriteria @ ~33% (M5 33%, M6 33%, M7 34%).

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **94** | **Backend `Dockerfile`:** multi-stage (builder → final), non-root user (`appuser`), `HEALTHCHECK` via `/health`, slim base, `--no-cache-dir`, ownership setup. **Frontend `Dockerfile`:** multi-stage (Node builder → Nginx alpine-slim), `npm ci` clean install, build ARG `VITE_API_URL`, custom `nginx.conf` di-copy ke production. Best-in-class. |
| **M6 – Docker Compose multi-container** | 33% | **90** | `docker-compose.yml` 3 service (db/backend/frontend), `healthcheck` Postgres (`pg_isready`), named volume `lentera_pgdata`, custom network `lentera_net`, `env_file` ke `.env.docker`, `restart: unless-stopped`. Volume sync `./backend/static` untuk file upload. `.env.docker.example` tersedia. Minus: password DB di-commit (`POSTGRES_PASSWORD: postgres` di compose) — perlu dipindah ke env. |
| **M7 – Optimasi & Production config** | 34% | **96** | `docker-compose.prod.yml` dengan override profesional: `DEBUG=false`, `CORS_ORIGINS=https://...`, `restart: always`, `ports: !reset []` untuk hide DB dari internet (excellent!). Multi-stage build menghasilkan ~25 MB vs ~1 GB (didokumentasikan di `docs/image-comparison.md`). Healthcheck di Dockerfile + compose. Dokumentasi pendukung: `docs/docker-architecture.md`, `docs/docker-cheatsheet.md`. |

**Nilai Kelompok: (94 + 90 + 96) / 3 = 93.33**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W5–W7)

> W5 = 23–29 Mar, W6 = 30 Mar – 5 Apr, W7 = 6–12 Apr.

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| Maulana Malik Ibrahim | Maulana Malik Ibrahim | 1 | 2 | 10 | **13** |
| Muhammad Aqila Ardhi | mightyqilo13 | 0 | 3 | 3 | **6** |
| Khanza Nabila Tsabita | Khanza nabila t | 1 | 4 | 1 | **6** |
| Micka Mayulia Utama | micka | 0 | 2 | 1 | **3** |

> 📌 Pergeseran beban kerja: di Fase 1, Khanza & Micka dominan di setup awal. Di Fase 2, Maulana naik signifikan (commit komentar penjelas + dockerfile optimasi). Khanza tetap konsisten di DevOps role. Micka turun (perlu didorong).

---

### C. Penilaian Individual

> Bobot: Konsistensi 30% + Substansi 40% + Kesesuaian Peran 20% + Kualitas Pesan 10%

#### 1. Khanza Nabila Tsabita (Lead DevOps)
- **Konsistensi (30%):** 3/3 minggu aktif → 92
- **Substansi (40%):** 6 commits berfokus DevOps: `dockerfile` + `dockerignore` (W5), `.env.docker.example` + cleanup venv (W6), finalize dockerfile + `image-comparison.md` (W6), `scripts/docker-run.ps1` optimasi backend image + DB prep timing (W7). Output crucial → 90
- **Kesesuaian Peran (20%):** 100% commit DevOps — sangat sesuai → 96
- **Kualitas Pesan (10%):** Deskriptif dengan konteks role (`update backend/dockerfile for optimise images and add scripts/docker-run.ps1 for simpelify start/stop container + 5 sec for db prep`) → 85

**Nilai: (0.30×92 + 0.40×90 + 0.20×96 + 0.10×85) = 27.6 + 36.0 + 19.2 + 8.5 = 91.3 → 91**
**Grade: A**

---

#### 2. Maulana Malik Ibrahim (Lead Backend)
- **Konsistensi (30%):** 3/3 minggu aktif → 90
- **Substansi (40%):** 13 commits: healthcheck di Dockerfile, optimasi dockerfile postgresql client, startup script backend, batch komentar penjelas (main/crud/models/schemas/auth/database/seeder), fix Lost Buku Status, fix Fine repr. Mix backend hardening + dokumentasi inline → 86
- **Kesesuaian Peran (20%):** Mostly backend; sedikit overlap ke DevOps (dockerfile) — tapi wajar untuk Lead Backend → 88
- **Kualitas Pesan (10%):** Deskriptif Indonesia (`Optimasi dockerfile dan implementasi startup script backend`) → 82

**Nilai: (0.30×90 + 0.40×86 + 0.20×88 + 0.10×82) = 27.0 + 34.4 + 17.6 + 8.2 = 87.2 → 87**
**Grade: A**

---

#### 3. Muhammad Aqila Ardhi (Lead QA & Docs)
- **Konsistensi (30%):** 2/3 minggu aktif (W5 kosong) → 75
- **Substansi (40%):** 6 commits substantif: E2E authentication testing report, docker multi-container architecture diagram, image comparison docs, final README + exported PDF. Perbaikan signifikan dari Fase 1 → 82
- **Kesesuaian Peran (20%):** 100% commit di docs → 92
- **Kualitas Pesan (10%):** Conventional commits dengan deskripsi panjang (`docs: complete E2E authentication testing report and update roadmap for Module 4`) → 90

**Nilai: (0.30×75 + 0.40×82 + 0.20×92 + 0.10×90) = 22.5 + 32.8 + 18.4 + 9.0 = 82.7 → 83**
**Grade: AB**

> 📈 Naik dari B (74) di Fase 1 ke AB (83) — pesan commit & substansi membaik signifikan.

---

#### 4. Micka Mayulia Utama (Lead Frontend)
- **Konsistensi (30%):** 2/3 minggu aktif (W5 kosong) → 70
- **Substansi (40%):** 3 commits: multi-stage Docker frontend (commit besar dengan nginx config, SPA routing, gzip, security headers), `docker-cheatsheet`, fix frontend password, notifikasi. Volume rendah tapi commit multi-stage sangat berkualitas → 76
- **Kesesuaian Peran (20%):** Sesuai (frontend + Dockerfile frontend) → 84
- **Kualitas Pesan (10%):** Sekarang lebih panjang & informatif (commit multi-stage docker detail sekali) tapi mix kualitas → 78

**Nilai: (0.30×70 + 0.40×76 + 0.20×84 + 0.10×78) = 21.0 + 30.4 + 16.8 + 7.8 = 76.0 → 76**
**Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C05 — Tugas terstruktur optimasi Docker image & Compose (4%):** semua anggota **93**

**C06 — Kontribusi & progres mingguan via Git commit log (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | **91** |
| 10231051 | Maulana Malik Ibrahim | **87** |
| 10231053 | Micka Mayulia Utama | **76** |
| 10231057 | Muhammad Aqila Ardhi | **83** |

---

### E. Catatan untuk Fase Berikutnya

- ✅ Dockerization profesional → siap untuk CI/CD (M9–11) tanpa perlu refactor
- ⚠️ `POSTGRES_PASSWORD: postgres` masih di-commit di `docker-compose.yml` — flag untuk Modul 15 security audit
- ✅ Khanza sebagai Lead DevOps mendelivery dengan kualitas tinggi & konsisten
- ⚠️ Micka perlu velocity boost di M9–11 (frontend tests dengan Vitest, dll)
- 💡 Distribusi role makin tajam: Maulana=backend hardening, Khanza=infra, Aqila=docs, Micka=frontend. Sehat.
