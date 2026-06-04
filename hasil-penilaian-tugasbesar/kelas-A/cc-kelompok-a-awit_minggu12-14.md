# Laporan Penilaian Kelompok awit – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | awit |
| Repo | cc-kelompok-a-awit |
| Project | **PalmTrack Cloud (PalmChain)** — monitoring pengangkutan TBS kelapa sawit |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Adam Ibnu Ramadhan | 10231003 | Lead Backend | ✅ prime |
| Adhyasta Firdaus | 10231005 | Lead CI/CD & Deployment | ✅ prime |
| Adonia Azarya Tamalonggehe | 10231007 | Lead QA & Documentation | off-phase |
| Alfian Fadillah Putra | 10231009 | Lead Frontend | off-phase |
| Varrel Kaleb Ropard Pasaribu | 10231089 | Lead DevOps & Container | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **60** | Tidak ada ADR formal (hanya `docs/docker-architecture.md`). Batas service ada di kode tapi tidak terdokumentasi. |
| **M13 – Implementasi microservices** | 33% | **64** | Kode service ditulis: `services/auth-service`, `services/item-service`, `services/gateway/nginx.conf`, inter-service `services/item-service/auth_client.py`. **Minus krusial: tidak terhubung ke compose** — `docker-compose.yml` & `docker-compose.prod.yml` masih monolith (`backend`/`frontend`/`db`). Microservices belum runnable end-to-end. |
| **M14 – Architecture diagram + monitoring** | 34% | **50** | Tidak ada diagram arsitektur microservices maupun monitoring. |

**Nilai Kelompok: (60 + 64 + 50) / 3 = 58.00 → 58**
**Grade Kelompok: BC**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Adhyasta = `Adhyasta Firdaus`/`adhyasta firdaus`; Adonia = `Adonia76`; Alfian = `Alfian Fadillah Putra`; Adam = `Adam IR`; Varrel = `VarrelKaleb89`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Adhyasta Firdaus | Adhyasta Firdaus / adhyasta firdaus | 0 | 6 | 0 | **6** |
| Adonia Azarya Tamalonggehe | Adonia76 | 0 | 4 | 0 | **4** |
| Alfian Fadillah Putra | Alfian Fadillah Putra | 1 | 0 | 0 | **1** |
| Adam Ibnu Ramadhan | Adam IR | 0 | 0 | 0 | **0** |
| Varrel Kaleb Ropard Pasaribu | VarrelKaleb89 | 0 | 0 | 0 | **0** |

---

### C. Penilaian Individual

#### 1. Adhyasta Firdaus (Lead CI/CD & Deployment — prime)
- Konsistensi 55 · Substansi 78 · Peran 85 · Pesan 78
- 6 commit, 1/3 minggu (W13), penulis utama kode service + gateway.

**Nilai: 73** · **Grade: B**

#### 2. Adonia Azarya Tamalonggehe (Lead QA & Docs — off-phase)
- Konsistensi 50 · Substansi 70 · Peran 72 · Pesan 75
- 4 commit, 1/3 minggu.

**Nilai mentah: 65** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

#### 3. Alfian Fadillah Putra (Lead Frontend — off-phase)
- Konsistensi 45 · Substansi 55 · Peran 65 · Pesan 70
- 1 commit, 1/3 minggu.

**Nilai mentah: 56** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

#### 4. Adam Ibnu Ramadhan (Lead Backend — prime)
- **0 commit** di window F5 — absen di fase microservices padahal role Backend prime.

**Nilai: 25** · **Grade: E** (absen total, tanpa floor)

#### 5. Varrel Kaleb Ropard Pasaribu (Lead DevOps & Container — prime)
- **0 commit** di window F5 — absen di fase microservices padahal role DevOps/Container prime.

**Nilai: 25** · **Grade: E** (absen total, tanpa floor)

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **58**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | **25** |
| 10231005 | Adhyasta Firdaus | **73** |
| 10231007 | Adonia Azarya Tamalonggehe | **70** |
| 10231009 | Alfian Fadillah Putra | **70** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | **25** |
