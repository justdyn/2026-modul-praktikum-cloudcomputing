# Laporan Penilaian Kelompok ethereal – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ethereal |
| Repo | cc-kelompok-a-ethereal |
| Project | **Kelarin** — platform manajemen tugas akademik, didekomposisi jadi Auth Service + Task Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Alsha Dwi Cahya | 10231011 | Lead Container | ✅ prime |
| Amazia Devid Saputra | 10231013 | Lead Frontend | off-phase |
| Andini Permata Sari | 10231015 | Lead QA & Docs | off-phase |
| Ansellma Tita Pakartiwuri Putri | 10231017 | Lead Deploy & CI/CD | ✅ prime |
| Tiya Mitra Ayu | 10231088 | Lead Backend | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **86** | `docs/architecture.md` (215 baris): batas domain Auth vs Task, topologi gateway, kontrak API. Boundaries jelas dan terdokumentasi. |
| **M13 – Implementasi microservices** | 33% | **92** | Dekomposisi penuh: `services/auth-service` + `services/task-service` + `services/gateway` (nginx). `docker-compose.yml` 6 container. **Inter-service comm** via `services/task-service/auth_client.py` + **resilience** `services/task-service/circuit_breaker.py`. |
| **M14 – Architecture diagram + monitoring** | 34% | **82** | Diagram arsitektur di `docs/architecture.md`. Circuit breaker sebagai pola reliability. Minus: belum ada metrics collector / structured logging eksplisit per service. |

**Nilai Kelompok: (86 + 92 + 82) / 3 = 86.67 → 87**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> W12 = 11–17 Mei, W13 = 18–24 Mei, W14 = 25–31 Mei.
>
> **Alias:** Tiya = `Tiyamitraayu`/`Tiyamitrayu`; Devid = `Devid`/`Devid1013`; Alsha = `dwialsha`; Andini = `gitandys`; Ansellma = `secretceremony`/`ansel`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Ansellma Tita | secretceremony / ansel | 5 | 2 | 14 | **21** |
| Andini Permata Sari | gitandys | 4 | 4 | 2 | **10** |
| Tiya Mitra Ayu | Tiyamitraayu / Tiyamitrayu | 3 | 3 | 0 | **6** |
| Alsha Dwi Cahya | dwialsha | 1 | 4 | 0 | **5** |
| Amazia Devid Saputra | Devid / Devid1013 | 0 | 4 | 0 | **4** |

---

### C. Penilaian Individual

#### 1. Ansellma Tita Pakartiwuri Putri (Lead Deploy & CI/CD — prime)
- Konsistensi 90 · Substansi 92 · Peran 95 · Pesan 85
- 21 commit, 3/3 minggu, motor infra microservices (gateway, compose, deploy).

**Nilai: 91** · **Grade: A**

#### 2. Andini Permata Sari (Lead QA & Docs — off-phase)
- Konsistensi 90 · Substansi 82 · Peran 80 · Pesan 82
- 10 commit, 3/3 minggu, dokumentasi arsitektur + testing. Volume tinggi untuk role off-phase.

**Nilai: 84** · **Grade: AB** (di atas floor, tidak perlu penyesuaian)

#### 3. Tiya Mitra Ayu (Lead Backend — prime)
- Konsistensi 75 · Substansi 84 · Peran 90 · Pesan 82
- 6 commit, 2/3 minggu (W14 kosong), backend service decomposition.

**Nilai: 82** · **Grade: AB**

#### 4. Alsha Dwi Cahya (Lead Container — prime)
- Konsistensi 75 · Substansi 80 · Peran 88 · Pesan 80
- 5 commit, 2/3 minggu, containerization service.

**Nilai: 80** · **Grade: AB**

#### 5. Amazia Devid Saputra (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 70 · Peran 75 · Pesan 78
- 4 commit, 1/3 minggu (hanya W13), integrasi frontend ke gateway.

**Nilai mentah: 66** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **87**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | **80** |
| 10231013 | Amazia Devid Saputra | **70** |
| 10231015 | Andini Permata Sari | **84** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | **91** |
| 10231088 | Tiya Mitra Ayu | **82** |
