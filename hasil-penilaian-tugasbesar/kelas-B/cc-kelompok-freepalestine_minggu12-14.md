# Laporan Penilaian Kelompok freepalestine (magang) – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | freepalestine 🎓 (semua anggota magang) |
| Repo | cc-kelompok-freepalestine |
| Project | Aplikasi cloud-native FastAPI + React — didekomposisi jadi Auth + Dashboard Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota** (semua magang — dinilai di tabel magang):

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Ariel Itsbat Nurhaq | 10231018 | Lead Backend & Frontend | ✅ prime |
| Muhammad Khoiruddin Marzuq | 10231065 | Lead DevOps | ✅ prime |
| Raditya Yudianto | 10231076 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **88** | Dokumentasi per-modul sangat lengkap: `docs/modul12-microservices.md` (dekomposisi monolith + service boundaries + DB per service), `docs/modul13-reliability.md`, `docs/modul14-monitoring-observability.md`. |
| **M13 – Implementasi microservices** | 33% | **94** | `services/auth-service` + `services/dashboard-service` + `services/gateway`. `docker-compose.microservices.yml` + `docker-compose.microservices.prod.yml`. **Inter-service auth** + **circuit breaker** + reliability patterns. |
| **M14 – Architecture diagram + monitoring** | 34% | **86** | `docs/modul14-monitoring-observability.md` + metrics/structured logging per service. Paling lengkap untuk M14 di kelas B. |

**Nilai Kelompok: (88 + 94 + 86) / 3 = 89.33 → 89**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> 80 commit di window F5 — paling aktif di kelas B. **Alias:** Ariel = `Ariel Itsbat Nurhaq`/`Itsbat`; Marzuq = `Mukhoma`; Raditya = `Raditya Yudianto`/`Rhadide`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Ariel Itsbat Nurhaq | Ariel Itsbat Nurhaq / Itsbat | 28 | 23 | 2 | **53** |
| Raditya Yudianto | Raditya Yudianto / Rhadide | 18 | 3 | 0 | **21** |
| Muhammad Khoiruddin Marzuq | Mukhoma | 6 | 0 | 0 | **6** |

---

### C. Penilaian Individual

#### 1. Ariel Itsbat Nurhaq (Lead Backend & Frontend — prime)
- Konsistensi 90 · Substansi 95 · Peran 94 · Pesan 82 — 53 commit, 3/3 minggu, dominan di seluruh dekomposisi.

**Nilai: 92** · **Grade: A**

#### 2. Raditya Yudianto (Lead QA & Docs — off-phase)
- Konsistensi 75 · Substansi 85 · Peran 82 · Pesan 80 — 21 commit, dokumentasi modul12-14 yang sangat lengkap. Di atas floor.

**Nilai: 81** · **Grade: AB**

#### 3. Muhammad Khoiruddin Marzuq (Lead DevOps — prime)
- Konsistensi 55 · Substansi 72 · Peran 82 · Pesan 78 — 6 commit, 1/3 minggu.

**Nilai: 70** · **Grade: B** (prime, tanpa floor)

---

### D. Ringkasan untuk Gradebook (tabel magang)

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **89**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231018 | Ariel Itsbat Nurhaq | **92** |
| 10231065 | Muhammad Khoiruddin Marzuq | **70** |
| 10231076 | Raditya Yudianto | **81** |
