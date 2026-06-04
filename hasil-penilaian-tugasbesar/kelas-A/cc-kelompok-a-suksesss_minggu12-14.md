# Laporan Penilaian Kelompok suksesss – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | suksesss |
| Repo | cc-kelompok-a-suksesss |
| Project | **SafeSpace** — layanan bimbingan konseling, didekomposisi jadi Auth Service + Item Service |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Rendy Rifandy Kurnia | 10231081 | Lead Backend | ✅ prime |
| Riska Fadlun Khairiyah Purba | 10231083 | Lead Frontend | off-phase |
| Rizki Abdul Aziz | 10231085 | Lead DevOps | ✅ prime |
| Siti Nur Azizah Putri Awni | 10231087 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **66** | Tidak ada ADR formal (hanya `docs/docker-architecture.md`). Tapi tiap service punya `README.md` (`services/auth-service/README.md`, `services/item-service/README.md`) yang menjelaskan boundary. |
| **M13 – Implementasi microservices** | 33% | **80** | Dekomposisi: `services/auth-service` + `services/item-service` (struktur `app/` + `tests/`). `docker-compose.microservices.yml` dengan **DB terisolasi** (`auth-db`, `item-db`). **Inter-service comm** `services/item-service/app/auth_client.py`. Minus: **tidak ada API gateway**, frontend belum terintegrasi di compose microservices. |
| **M14 – Architecture diagram + monitoring** | 34% | **54** | Tidak ada diagram arsitektur microservices terdokumentasi maupun metrics/monitoring per service. |

**Nilai Kelompok: (66 + 80 + 54) / 3 = 66.67 → 67**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Riska = `riskapurba`/`Riska Purba`; Rendy = `NorEndGate`; Rizki = `Liveral`; Siti = `Azizah66`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Riska Fadlun Khairiyah Purba | riskapurba / Riska Purba | 1 | 8 | 1 | **10** |
| Rendy Rifandy Kurnia | NorEndGate | 4 | 1 | 0 | **5** |
| Rizki Abdul Aziz | Liveral | 0 | 1 | 0 | **1** |
| Siti Nur Azizah Putri Awni | Azizah66 | 0 | 0 | 0 | **0** |

---

### C. Penilaian Individual

#### 1. Riska Fadlun Khairiyah Purba (Lead Frontend — off-phase)
- Konsistensi 90 · Substansi 80 · Peran 76 · Pesan 78
- 10 commit, 3/3 minggu — paling aktif. Di atas floor.

**Nilai: 82** · **Grade: AB**

#### 2. Rendy Rifandy Kurnia (Lead Backend — prime)
- Konsistensi 70 · Substansi 78 · Peran 85 · Pesan 78
- 5 commit, 2/3 minggu, dekomposisi backend service.

**Nilai: 77** · **Grade: AB**

#### 3. Rizki Abdul Aziz (Lead DevOps — prime)
- Konsistensi 45 · Substansi 60 · Peran 75 · Pesan 72
- Hanya 1 commit di window F5 — minim untuk role DevOps prime.

**Nilai: 60** · **Grade: BC** (prime, tanpa floor)

#### 4. Siti Nur Azizah Putri Awni (Lead QA & Docs — off-phase)
- Konsistensi 20 · Substansi 30 · Peran 40 · Pesan 40
- **0 commit** di seluruh window F5 (aktif di F4, hilang di F5).

**Nilai: 30** · **Grade: E** (absen total, raw < 50 → tanpa floor)

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **67**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231081 | Rendy Rifandy Kurnia | **77** |
| 10231083 | Riska Fadlun Khairiyah Purba | **82** |
| 10231085 | Rizki Abdul Aziz | **60** |
| 10231087 | Siti Nur Azizah Putri Awni | **30** |
