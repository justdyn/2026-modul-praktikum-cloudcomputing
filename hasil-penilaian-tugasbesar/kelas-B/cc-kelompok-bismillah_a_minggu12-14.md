# Laporan Penilaian Kelompok bismillah_a – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | bismillah_a |
| Repo | cc-kelompok-bismillah_a |
| Project | **Sistem Pelaporan Perundungan Kampus ITK** — didekomposisi jadi Auth + Report Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota** (Salsabila magang — dinilai di tabel magang):

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Aditya Laksamana P Butar Butar | 10231006 | Lead Backend | ✅ prime |
| Firni Fauziah Ramadhini | 10231038 | Lead Frontend | off-phase |
| Muhammad Novri Aziztra | 10231066 | Lead DevOps | ✅ prime |
| Salsabila Putri Zahrani 🎓 | 10231086 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **86** | `docs/architecture.md` (414 baris): batas domain Auth vs Report, kontrak API, topologi gateway. |
| **M13 – Implementasi microservices** | 33% | **92** | `services/auth-service` + `services/report-service` + `services/gateway` (nginx). `docker-compose` 6 container. **Inter-service auth** + **circuit breaker** di service. |
| **M14 – Architecture diagram + monitoring** | 34% | **76** | Diagram di `docs/architecture.md` + circuit breaker. Minus: belum ada metrics/structured logging. |

**Nilai Kelompok: (86 + 92 + 76) / 3 = 84.67 → 85**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> W14 kosong seluruh tim. **Alias:** Firni = `firnifziah`; Salsabila = `salsabila1086`; sisanya commit dengan NIM email.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Aditya Laksamana P Butar Butar | (10231006) | 4 | 2 | 0 | **6** |
| Muhammad Novri Aziztra | Novri Aziztra | 3 | 2 | 0 | **5** |
| Firni Fauziah Ramadhini | firnifziah | 0 | 3 | 0 | **3** |
| Salsabila Putri Zahrani 🎓 | salsabila1086 | 1 | 0 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Aditya Laksamana P Butar Butar (Lead Backend — prime)
- Konsistensi 75 · Substansi 85 · Peran 90 · Pesan 80 — 6 commit, dekomposisi backend.

**Nilai: 83** · **Grade: AB**

#### 2. Muhammad Novri Aziztra (Lead DevOps — prime)
- Konsistensi 75 · Substansi 82 · Peran 90 · Pesan 80 — 5 commit, gateway + infra.

**Nilai: 81** · **Grade: AB**

#### 3. Firni Fauziah Ramadhini (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 68 · Peran 72 · Pesan 75 — 3 commit, 1/3 minggu.

**Nilai mentah: 64** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

#### 4. Salsabila Putri Zahrani 🎓 (Lead QA & Docs — off-phase, magang)
- Konsistensi 45 · Substansi 55 · Peran 65 · Pesan 70 — 1 commit.

**Nilai mentah: 56** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B** *(masuk tabel magang)*

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **85**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231006 | Aditya Laksamana P Butar Butar | **83** |
| 10231038 | Firni Fauziah Ramadhini | **70** |
| 10231066 | Muhammad Novri Aziztra | **81** |
| 10231086 | Salsabila Putri Zahrani 🎓 (magang) | **70** |
