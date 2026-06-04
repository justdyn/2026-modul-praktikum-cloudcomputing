# Laporan Penilaian Kelompok sowelcloudspace – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | sowelcloudspace |
| Repo | cc-kelompok-sowelcloudspace |
| Project | **Sowel Task** — to-do list kolaboratif, didekomposisi jadi Auth + Task Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Anjas Geofany Diamare | 10231016 | Lead Backend | ✅ prime |
| Arya Wijaya Saroyo | 10231020 | Lead DevOps | ✅ prime |
| Cantika Ade Qutnindra Maharani | 10231024 | Lead Frontend | off-phase |
| Meiske Handayani | 10231052 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **85** | `docs/architecture.md` (430 baris): batas domain Auth vs Task, kontrak API, topologi gateway. |
| **M13 – Implementasi microservices** | 33% | **85** | `services/auth-service` + `services/task-service` + `services/gateway`. `docker-compose` 5 container. Inter-service auth. Minus: belum ada circuit breaker. |
| **M14 – Architecture diagram + monitoring** | 34% | **64** | Diagram di `docs/architecture.md`. Minus: tidak ada metrics/monitoring/circuit breaker. |

**Nilai Kelompok: (85 + 85 + 64) / 3 = 78.00 → 78**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Cantika = `cantika ade`; Meiske = `Meiske Handayani`/`Meiskee`; Anjas = `Anjas Geofany Diamare`; Arya = `Arya Wijaya Saroyo`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Cantika Ade Qutnindra Maharani | cantika ade | 1 | 7 | 2 | **10** |
| Anjas Geofany Diamare | Anjas Geofany Diamare | 0 | 5 | 1 | **6** |
| Meiske Handayani | Meiske / Meiskee | 2 | 3 | 0 | **5** |
| Arya Wijaya Saroyo | Arya Wijaya Saroyo | 0 | 2 | 0 | **2** |

---

### C. Penilaian Individual

#### 1. Cantika Ade Qutnindra Maharani (Lead Frontend — off-phase)
- Konsistensi 90 · Substansi 80 · Peran 76 · Pesan 78 — 10 commit, 3/3 minggu, paling aktif. Di atas floor.

**Nilai: 82** · **Grade: AB**

#### 2. Anjas Geofany Diamare (Lead Backend — prime)
- Konsistensi 75 · Substansi 82 · Peran 88 · Pesan 78 — 6 commit, dekomposisi backend.

**Nilai: 81** · **Grade: AB**

#### 3. Meiske Handayani (Lead QA & Docs — off-phase)
- Konsistensi 75 · Substansi 76 · Peran 74 · Pesan 78 — 5 commit, dokumentasi arsitektur. Di atas floor.

**Nilai: 76** · **Grade: AB**

#### 4. Arya Wijaya Saroyo (Lead DevOps — prime)
- Konsistensi 50 · Substansi 60 · Peran 78 · Pesan 74 — 2 commit, 1/3 minggu.

**Nilai: 62** · **Grade: BC** (prime, tanpa floor)

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **78**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231016 | Anjas Geofany Diamare | **81** |
| 10231020 | Arya Wijaya Saroyo | **62** |
| 10231024 | Cantika Ade Qutnindra Maharani | **82** |
| 10231052 | Meiske Handayani | **76** |
