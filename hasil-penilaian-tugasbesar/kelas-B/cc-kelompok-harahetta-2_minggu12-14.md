# Laporan Penilaian Kelompok harahetta-2 – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | harahetta-2 |
| Repo | cc-kelompok-harahetta-2 |
| Project | **Sewain** — platform rental, didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota** (role estimasi — tidak eksplisit di README):

| Nama | NIM | Role (estimasi) | F5 prime? |
|---|---|---|---|
| Achmad Zaki Zaidan | 10231002 | Backend | ✅ prime |
| Djaky Abbyyu Fauzan Timumum | 10231032 | Frontend/Support | off-phase |
| Muhammad Alif Setiawan | 10231056 | DevOps/Backend | ✅ prime |
| Riqqah Khalda Karina | 10231082 | QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **84** | `docs/architecture.md` (230 baris): batas domain Auth vs Item, topologi gateway. |
| **M13 – Implementasi microservices** | 33% | **88** | `services/auth-service` + `services/item-service` + `services/gateway` (nginx). `docker-compose` 6 container. **Inter-service auth** (verify token). Minus: belum ada circuit breaker. |
| **M14 – Architecture diagram + monitoring** | 34% | **68** | Diagram di `docs/architecture.md`. Minus: tidak ada metrics/monitoring/circuit breaker per service. |

**Nilai Kelompok: (84 + 88 + 68) / 3 = 80.00 → 80**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Alif = `Shoryu`/`alifmiaw`/`Muhammad Alif Setiawan`; Zaki = `ZakiZaidan`; Djaky = `ZannSamaa`/`boxermr8`; Riqqah = `riqqahkhalda`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Muhammad Alif Setiawan | Shoryu | 17 | 7 | 4 | **28** |
| Achmad Zaki Zaidan | ZakiZaidan | 1 | 3 | 0 | **4** |
| Riqqah Khalda Karina | riqqahkhalda | 1 | 1 | 1 | **3** |
| Djaky Abbyyu Fauzan Timumum | ZannSamaa | 0 | 2 | 0 | **2** |

---

### C. Penilaian Individual

#### 1. Muhammad Alif Setiawan (DevOps/Backend — prime)
- Konsistensi 90 · Substansi 90 · Peran 88 · Pesan 80 — 28 commit, 3/3 minggu, motor dekomposisi + gateway.

**Nilai: 89** · **Grade: A**

#### 2. Achmad Zaki Zaidan (Backend — prime)
- Konsistensi 70 · Substansi 78 · Peran 85 · Pesan 78 — 4 commit, 2/3 minggu.

**Nilai: 77** · **Grade: AB**

#### 3. Riqqah Khalda Karina (QA & Docs — off-phase)
- Konsistensi 75 · Substansi 62 · Peran 70 · Pesan 75 — 3 commit, 3/3 minggu (konsisten kecil).

**Nilai mentah: 69** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

#### 4. Djaky Abbyyu Fauzan Timumum (Frontend/Support — off-phase)
- Konsistensi 45 · Substansi 60 · Peran 68 · Pesan 72 — 2 commit, 1/3 minggu.

**Nilai mentah: 58** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **80**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231002 | Achmad Zaki Zaidan | **77** |
| 10231032 | Djaky Abbyyu Fauzan Timumum | **70** |
| 10231056 | Muhammad Alif Setiawan | **89** |
| 10231082 | Riqqah Khalda Karina | **70** |
