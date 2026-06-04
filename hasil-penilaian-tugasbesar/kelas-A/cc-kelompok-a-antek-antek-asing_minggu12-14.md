# Laporan Penilaian Kelompok antek-antek-asing – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | antek-antek-asing |
| Repo | cc-kelompok-a-antek-antek-asing |
| Project | **Antick Async** — helpdesk internal manajemen tiket, didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Muhammad Athala Romero | 10231059 | Lead Backend | ✅ prime |
| Muhammad Bagas Setiawan | 10231061 | Lead Frontend | off-phase |
| Muhammad Fikri Haikal Ariadma | 10231063 | Lead DevOps | ✅ prime |
| Nanda Aulia Putri | 10231067 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **87** | `docs/architecture.md` (275 baris): batas domain Auth vs Item, topologi gateway, kontrak API terdokumentasi lengkap. |
| **M13 – Implementasi microservices** | 33% | **92** | Dekomposisi penuh: `services/auth-service` + `services/item-service` + `services/gateway` (nginx). `docker-compose.yml` 8 container. **Inter-service auth** `services/item-service/auth_client.py` (verify token ke auth-service). |
| **M14 – Architecture diagram + monitoring** | 34% | **85** | Diagram arsitektur di `docs/architecture.md`. **Monitoring**: metrics/observability di `services/auth-service/main.py`. |

**Nilai Kelompok: (87 + 92 + 85) / 3 = 88.00 → 88**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Athala = `Muhammad Athala Romero`/`ItsHertz666`; Bagas = `Muhammad Bagas Setiawan`/`Muhammaad Bagas Setiawan`/`gascrow`; Fikri = `FikriHaikal`/`Haikal`; Nanda = `Nanda Aulia Putri`/`nanda-aulia`.
>
> **W14 kosong seluruh tim** — sprint microservices selesai di W12–W13.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Muhammad Athala Romero | Muhammad Athala Romero | 11 | 7 | 0 | **18** |
| Nanda Aulia Putri | Nanda Aulia Putri / nanda-aulia | 5 | 2 | 0 | **7** |
| Muhammad Bagas Setiawan | Muhammad Bagas Setiawan / gascrow | 5 | 0 | 0 | **5** |
| Muhammad Fikri Haikal Ariadma | FikriHaikal | 5 | 0 | 0 | **5** |

---

### C. Penilaian Individual

#### 1. Muhammad Athala Romero (Lead Backend — prime)
- Konsistensi 75 · Substansi 92 · Peran 94 · Pesan 82
- 18 commit, motor dekomposisi backend service. W14 kosong.

**Nilai: 86** · **Grade: A**

#### 2. Nanda Aulia Putri (Lead QA & Docs — off-phase)
- Konsistensi 75 · Substansi 80 · Peran 80 · Pesan 80
- 7 commit, 2/3 minggu, dokumentasi arsitektur + testing. Di atas floor.

**Nilai: 79** · **Grade: AB**

#### 3. Muhammad Fikri Haikal Ariadma (Lead DevOps — prime)
- Konsistensi 55 · Substansi 80 · Peran 88 · Pesan 80
- 5 commit, 1/3 minggu (W12 saja), gateway + infra.

**Nilai: 74** · **Grade: B**

#### 4. Muhammad Bagas Setiawan (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 72 · Peran 74 · Pesan 78
- 5 commit, 1/3 minggu (W12 saja).

**Nilai mentah: 66** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **88**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231059 | Muhammad Athala Romero | **86** |
| 10231061 | Muhammad Bagas Setiawan | **70** |
| 10231063 | Muhammad Fikri Haikal Ariadma | **74** |
| 10231067 | Nanda Aulia Putri | **79** |
