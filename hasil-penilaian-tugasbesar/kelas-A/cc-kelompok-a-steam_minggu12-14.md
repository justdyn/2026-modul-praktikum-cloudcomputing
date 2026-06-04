# Laporan Penilaian Kelompok steam – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | steam |
| Repo | cc-kelompok-a-steam |
| Project | **Inti Rupa** — asisten cerdas (summarizer + image generator), didekomposisi jadi Auth Service + AI Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Incha Raghil | 10231043 | Lead Frontend | off-phase |
| Irfan Zaki Riyanto | 10231045 | Lead Backend | ✅ prime |
| Jonathan Cristopher Jetro | 10231047 | Lead DevOps | ✅ prime |
| Jonathan Joseph Yudita Tampubolon | 10231048 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **64** | Tidak ada `docs/architecture.md` / ADR. Batas domain (Auth + AI) terimplementasi dengan DB terisolasi per service tapi tidak terdokumentasi. |
| **M13 – Implementasi microservices** | 33% | **90** | Dekomposisi: `services/auth-service` + `services/ai-service` + `services/gateway` (nginx). `docker-compose.yml` 6 container dengan **DB terisolasi** (`auth-db`, `ai-db`). **Inter-service comm** `services/ai-service/auth_client.py`. Pemisahan domain AI dari auth rapi. |
| **M14 – Architecture diagram + monitoring** | 34% | **56** | Tidak ada diagram arsitektur terdokumentasi, tidak ada metrics/circuit breaker per service. |

**Nilai Kelompok: (64 + 90 + 56) / 3 = 70.00 → 70**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Jonathan Cristopher = `Jonathan Cristopher Jetro`/`joreyjo10`; Irfan = `Irfan Zaki`/`IrfanZakiRiyanto`; Incha = `Inchaaaa`/`Incharaghil`; Jonathan Joseph = `Jonathan-Joseph-yudita`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Jonathan Cristopher Jetro | Jonathan Cristopher Jetro | 1 | 16 | 1 | **18** |
| Irfan Zaki Riyanto | IrfanZakiRiyanto / Irfan Zaki | 0 | 5 | 0 | **5** |
| Jonathan Joseph Yudita | Jonathan-Joseph-yudita | 1 | 3 | 0 | **4** |
| Incha Raghil | Inchaaaa / Incharaghil | 1 | 2 | 0 | **3** |

---

### C. Penilaian Individual

#### 1. Jonathan Cristopher Jetro (Lead DevOps — prime)
- Konsistensi 90 · Substansi 92 · Peran 94 · Pesan 82
- 18 commit, 3/3 minggu, motor gateway + service decomposition + compose.

**Nilai: 91** · **Grade: A**

#### 2. Irfan Zaki Riyanto (Lead Backend — prime)
- Konsistensi 55 · Substansi 80 · Peran 88 · Pesan 80
- 5 commit, 1/3 minggu (W13 saja), implementasi service backend.

**Nilai: 74** · **Grade: B**

#### 3. Incha Raghil (Lead Frontend — off-phase)
- Konsistensi 70 · Substansi 65 · Peran 72 · Pesan 72
- 3 commit, 2/3 minggu.

**Nilai mentah: 69** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

#### 4. Jonathan Joseph Yudita Tampubolon (Lead QA & Docs — off-phase)
- Konsistensi 70 · Substansi 68 · Peran 72 · Pesan 72
- 4 commit, 2/3 minggu.

**Nilai mentah: 70** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **70**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231043 | Incha Raghil | **70** |
| 10231045 | Irfan Zaki Riyanto | **74** |
| 10231047 | Jonathan Cristopher Jetro | **91** |
| 10231048 | Jonathan Joseph Yudita Tampubolon | **70** |
