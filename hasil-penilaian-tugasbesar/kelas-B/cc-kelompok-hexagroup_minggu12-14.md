# Laporan Penilaian Kelompok hexagroup – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexagroup |
| Repo | cc-kelompok-hexagroup (repo primer F2/F4/F5 untuk 5 anggota yang juga di kel6) |
| Project | Sistem administrasi surat & keuangan — didekomposisi jadi Auth + Finance + Letters Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota** (5 orang, sama dengan kel6; F5 dikerjakan di repo hexagroup):

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Achmad Bayhaqi | 10231001 | Lead Backend | ✅ prime |
| Alfiani Dwiyuniarti | 10231010 | Lead DevOps | ✅ prime |
| Indah Nur Fortuna | 10231044 | Lead Frontend | off-phase |
| Nilam Ayu NandaStari Romdoni | 10231070 | Lead QA & Docs | off-phase |
| Zahwa Hanna Dwi Putri | 10231092 | Lead CI/CD & Deploy | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **76** | `docs/architecture.md` (88 baris): boundaries 4 domain jelas (auth/finance/letters/gateway) tapi dokumen relatif ringkas — bukan ADR mendalam. |
| **M13 – Implementasi microservices** | 33% | **92** | Dekomposisi **4 service**: `services/auth-service` + `services/finance-service` + `services/letters-service` + `services/gateway`. `docker-compose` 8 container. **Inter-service auth kuat** (banyak titik verify). |
| **M14 – Architecture diagram + monitoring** | 34% | **66** | Diagram ringkas. Minus: tidak ada metrics/circuit breaker per service. |

**Nilai Kelompok: (76 + 92 + 66) / 3 = 78.00 → 78**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Achmad Bayhaqi = `10231001-achmad-bayhaqi`/`AchmadLyraa`; Zahwa = `Hahahanaa`; Indah = `IndahNurFortuna`; Alfiani = `alfiani-a11y`; Nilam = `nilamay`/`NilamAyu`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Zahwa Hanna Dwi Putri | Hahahanaa | 0 | 14 | 0 | **14** |
| Indah Nur Fortuna | IndahNurFortuna | 0 | 4 | 0 | **4** |
| Nilam Ayu NandaStari Romdoni | nilamay | 0 | 3 | 1 | **4** |
| Alfiani Dwiyuniarti | alfiani-a11y | 0 | 3 | 0 | **3** |
| Achmad Bayhaqi | AchmadLyraa | 1 | 1 | 0 | **2** |

---

### C. Penilaian Individual

#### 1. Zahwa Hanna Dwi Putri (Lead CI/CD & Deploy — prime)
- Konsistensi 55 · Substansi 88 · Peran 90 · Pesan 80 — 14 commit, gateway/compose/deploy core (1 minggu burst).

**Nilai: 78** · **Grade: AB**

#### 2. Achmad Bayhaqi (Lead Backend — prime)
- Konsistensi 70 · Substansi 65 · Peran 80 · Pesan 76 — 2 commit, 2/3 minggu.

**Nilai: 71** · **Grade: B**

#### 3. Nilam Ayu NandaStari Romdoni (Lead QA & Docs — off-phase)
- Konsistensi 70 · Substansi 70 · Peran 72 · Pesan 76 — 4 commit, 2/3 minggu. Di atas floor.

**Nilai: 71** · **Grade: B**

#### 4. Indah Nur Fortuna (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 68 · Peran 72 · Pesan 75 — 4 commit, 1/3 minggu.

**Nilai mentah: 64** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

#### 5. Alfiani Dwiyuniarti (Lead DevOps — prime)
- Konsistensi 50 · Substansi 68 · Peran 80 · Pesan 76 — 3 commit, 1/3 minggu.

**Nilai: 66** · **Grade: BC** (prime, tanpa floor)

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **78**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231001 | Achmad Bayhaqi | **71** |
| 10231010 | Alfiani Dwiyuniarti | **66** |
| 10231044 | Indah Nur Fortuna | **70** |
| 10231070 | Nilam Ayu NandaStari Romdoni | **71** |
| 10231092 | Zahwa Hanna Dwi Putri | **78** |
