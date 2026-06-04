# Laporan Penilaian Kelompok extraordinary – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | extraordinary |
| Repo | cc-kelompok-a-extraordinary (branch `master`) |
| Project | **Temuin** — sistem lost & found kampus, didekomposisi jadi Auth + Item + Engagement Service |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Nicholas Christian Samuel Manurung | 10231069 | Lead Frontend | off-phase |
| Pangeran Borneo Silaen | 10231073 | Lead DevOps | ✅ prime |
| Raisha Alika Irwandira | 10231077 | Lead Backend | ✅ prime |
| Rani Ayu Dewi | 10231079 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **62** | Tidak ada `docs/architecture.md` / ADR formal. Batas domain ada di kode (3 service: auth/item/engagement) tapi tidak terdokumentasi. |
| **M13 – Implementasi microservices** | 33% | **84** | Dekomposisi nyata: `services/auth-service`, `services/item-service`, `services/engagement-service` (masing-masing `app/`, `tests/`, `entrypoint.sh`, `pyproject.toml`). Orkestrasi via `infra/docker-compose.microservices.yml`. Inter-service via `services/engagement-service/app/utils/httpx_client.py`. Minus: **tidak ada API gateway**, DB tunggal di-share (bukan per-service). |
| **M14 – Architecture diagram + monitoring** | 34% | **58** | Tidak ada diagram arsitektur terdokumentasi maupun metrics/structured logging per service. |

**Nilai Kelompok: (62 + 84 + 58) / 3 = 68.00 → 68**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Pangeran = `PangeranSilaen`/`Pangeran Borneo Silaen`; Nicholas = `nicholasmnrng`; Raisha = `Raisha Alika`/`disnejy`; Rani = `raniayudewi`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Pangeran Borneo Silaen | PangeranSilaen | 7 | 12 | 0 | **19** |
| Rani Ayu Dewi | raniayudewi | 4 | 5 | 1 | **10** |
| Nicholas Christian S. Manurung | nicholasmnrng | 5 | 0 | 0 | **5** |
| Raisha Alika Irwandira | Raisha Alika | 0 | 1 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Pangeran Borneo Silaen (Lead DevOps — prime)
- Konsistensi 75 · Substansi 90 · Peran 92 · Pesan 80
- 19 commit, motor dekomposisi + orkestrasi microservices compose.

**Nilai: 85** · **Grade: AB**

#### 2. Rani Ayu Dewi (Lead QA & Docs — off-phase)
- Konsistensi 90 · Substansi 80 · Peran 80 · Pesan 80
- 10 commit, 3/3 minggu, testing + docs. Di atas floor.

**Nilai: 83** · **Grade: AB**

#### 3. Raisha Alika Irwandira (Lead Backend — prime)
- Konsistensi 40 · Substansi 50 · Peran 60 · Pesan 60
- Hanya 1 commit di seluruh window F5 — minim untuk role Backend yang prime di fase microservices.

**Nilai: 49** · **Grade: D** (prime, tanpa floor)

#### 4. Nicholas Christian Samuel Manurung (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 68 · Peran 74 · Pesan 75
- 5 commit, 1/3 minggu (W12 saja).

**Nilai mentah: 65** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **68**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231069 | Nicholas Christian Samuel Manurung | **70** |
| 10231073 | Pangeran Borneo Silaen | **85** |
| 10231077 | Raisha Alika Irwandira | **49** |
| 10231079 | Rani Ayu Dewi | **83** |
