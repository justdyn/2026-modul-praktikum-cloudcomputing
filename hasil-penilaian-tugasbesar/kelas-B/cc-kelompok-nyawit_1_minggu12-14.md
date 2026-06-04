# Laporan Penilaian Kelompok nyawit_1 – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit_1 |
| Repo | cc-kelompok-nyawit_1 |
| Project | Sistem procurement — didekomposisi jadi Auth + Procurement Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Andi Adam Firdaus | 10211014 | Lead DevOps | ✅ prime |
| Ahmad Baihaqi | 10221063 | Lead DevOps | ✅ prime |
| Az-Zahra Atikah Nurhaliza | 10231022 | Lead QA & Docs | off-phase |
| Muchlis Wahyu Saputra | 10231054 | Lead Backend | ✅ prime |
| Ranaya Chintya Mahitsa | 10231078 | Lead Frontend | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **78** | Dokumentasi arsitektur di `docs/architecture/` + `docs/docker-architecture.md`. Boundaries terdokumentasi. |
| **M13 – Implementasi microservices** | 33% | **88** | `services/auth-service` + `services/procurement-service` + `services/gateway`. `docker-compose.microservices.yml`. **Inter-service auth kuat**. Minus: belum ada circuit breaker. |
| **M14 – Architecture diagram + monitoring** | 34% | **60** | Diagram di docs. Minus: tidak ada metrics/monitoring/circuit breaker per service. |

**Nilai Kelompok: (78 + 88 + 60) / 3 = 75.33 → 75**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Muchlis = `Muchlis Wahyu Saputra - 10231054`/`imsatonito`; Az-Zahra = `zahraatikah`; Ahmad Baihaqi = `Ahmad Baihaqi` (NIM 10221063).
>
> ⚠️ Beban F5 nyaris seluruhnya dipikul **Muchlis** — 3 dari 5 anggota minim/absen.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Muchlis Wahyu Saputra | imsatonito | 20 | 4 | 3 | **27** |
| Az-Zahra Atikah Nurhaliza | zahraatikah | 5 | 0 | 0 | **5** |
| Ahmad Baihaqi | Ahmad Baihaqi | 1 | 0 | 0 | **1** |
| Andi Adam Firdaus | — | 0 | 0 | 0 | **0** |
| Ranaya Chintya Mahitsa | — | 0 | 0 | 0 | **0** |

---

### C. Penilaian Individual

#### 1. Muchlis Wahyu Saputra (Lead Backend — prime)
- Konsistensi 90 · Substansi 92 · Peran 90 · Pesan 80 — 27 commit, 3/3 minggu, praktis mengerjakan seluruh dekomposisi + gateway.

**Nilai: 90** · **Grade: A**

#### 2. Az-Zahra Atikah Nurhaliza (Lead QA & Docs — off-phase)
- Konsistensi 50 · Substansi 70 · Peran 72 · Pesan 75 — 5 commit, 1/3 minggu.

**Nilai mentah: 65** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

#### 3. Ahmad Baihaqi (Lead DevOps — prime)
- Konsistensi 40 · Substansi 52 · Peran 65 · Pesan 70 — 1 commit.

**Nilai: 53** · **Grade: C** (prime, tanpa floor)

#### 4. Andi Adam Firdaus (Lead DevOps — prime)
- **0 commit** di window F5 — absen di fase microservices.

**Nilai: 25** · **Grade: E** (absen total, tanpa floor)

#### 5. Ranaya Chintya Mahitsa (Lead Frontend — off-phase)
- **0 commit** di window F5 — absen total.

**Nilai: 25** · **Grade: E** (raw < 50 → tanpa floor)

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **75**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10211014 | Andi Adam Firdaus | **25** |
| 10221063 | Ahmad Baihaqi | **53** |
| 10231022 | Az-Zahra Atikah Nurhaliza | **70** |
| 10231054 | Muchlis Wahyu Saputra | **90** |
| 10231078 | Ranaya Chintya Mahitsa | **25** |
