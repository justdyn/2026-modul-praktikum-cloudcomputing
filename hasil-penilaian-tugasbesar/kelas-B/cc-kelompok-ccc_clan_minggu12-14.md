# Laporan Penilaian Kelompok ccc_clan – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ccc_clan |
| Repo | cc-kelompok-ccc_clan |
| Project | **SIPILIH** — Sistem Informasi Pemilihan Digital (e-voting), didekomposisi jadi Auth + Candidate Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Ade Ayu Kholifah Putri | 10231004 | Lead QA & Docs | off-phase |
| Dzakwan Fatih Fadhilah | 10231034 | Lead Backend | ✅ prime |
| Muhammad Dani | 10231062 | Lead DevOps | ✅ prime |
| Risky Nur Fatimah Bahar | 10231084 | Lead Frontend | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **64** | Tidak ada ADR/architecture.md khusus F5 (hanya `docs/docker-architecture.md`). Batas domain terimplementasi tapi tidak terdokumentasi sebagai ADR. |
| **M13 – Implementasi microservices** | 33% | **82** | Dekomposisi: `backend/services/auth-service` + `backend/services/candidate-service` + `gateway`. `docker-compose.yml` dengan **DB terisolasi** (`auth-db`, `candidate-db`). Gateway nginx routing. |
| **M14 – Architecture diagram + monitoring** | 34% | **54** | Tidak ada diagram arsitektur microservices maupun metrics/monitoring per service. |

**Nilai Kelompok: (64 + 82 + 54) / 3 = 66.67 → 67**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Dzakwan = `Awannn01`/`Dzakwan Fatih Fadhilah`; Dani = `Bento`/`Muhammad Dani`; Ade = `Adeayuuu`; Risky = `Risky Nur Fatimah Bahar`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Muhammad Dani | Bento / Muhammad Dani | 6 | 9 | 0 | **15** |
| Risky Nur Fatimah Bahar | Risky Nur Fatimah Bahar | 7 | 2 | 2 | **11** |
| Dzakwan Fatih Fadhilah | Awannn01 / Dzakwan | 9 | 0 | 0 | **9** |
| Ade Ayu Kholifah Putri | Adeayuuu | 2 | 0 | 0 | **2** |

---

### C. Penilaian Individual

#### 1. Muhammad Dani (Lead DevOps — prime)
- Konsistensi 75 · Substansi 88 · Peran 92 · Pesan 78 — 15 commit, gateway/compose/deploy core.

**Nilai: 84** · **Grade: AB**

#### 2. Risky Nur Fatimah Bahar (Lead Frontend — off-phase)
- Konsistensi 90 · Substansi 80 · Peran 76 · Pesan 78 — 11 commit, 3/3 minggu. Di atas floor.

**Nilai: 82** · **Grade: AB**

#### 3. Dzakwan Fatih Fadhilah (Lead Backend — prime)
- Konsistensi 55 · Substansi 82 · Peran 88 · Pesan 78 — 9 commit, 1/3 minggu (W12), dekomposisi backend.

**Nilai: 75** · **Grade: B**

#### 4. Ade Ayu Kholifah Putri (Lead QA & Docs — off-phase)
- Konsistensi 45 · Substansi 58 · Peran 68 · Pesan 72 — 2 commit.

**Nilai mentah: 58** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **67**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231004 | Ade Ayu Kholifah Putri | **70** |
| 10231034 | Dzakwan Fatih Fadhilah | **75** |
| 10231062 | Muhammad Dani | **84** |
| 10231084 | Risky Nur Fatimah Bahar | **82** |
