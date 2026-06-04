# Laporan Penilaian Kelompok nyawit (magang) – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit 🎓 (magang/konversi) |
| Repo | cc-kelompok-a-nyawit |
| Project | **Sistem Manajemen Aset IT** — pengelolaan infrastruktur hardware perusahaan |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Ilham Ahmad Fahriji | 10231042 | Lead Backend & DevOps | ✅ prime |
| Putu Ngurah Semara | 10231075 | Lead Frontend & QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **42** | Tidak ada ADR/dokumentasi arsitektur microservices. Tidak ada batas service yang didefinisikan. |
| **M13 – Implementasi microservices** | 33% | **38** | Tidak ada folder `services/`, tidak ada gateway/inter-service comm. `docker-compose.yml` tetap monolith (`database`/`backend`/`frontend`). Ada aktivitas (deploy ke Railway) tapi bukan dekomposisi microservices. |
| **M14 – Architecture diagram + monitoring** | 34% | **40** | Tidak ada diagram arsitektur microservices maupun monitoring per service. |

**Nilai Kelompok: (42 + 38 + 40) / 3 = 40.00 → 40**
**Grade Kelompok: E**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Ilham = `Hazley`; Putu = `PutuNgurahSemara`. (`railway-app[bot]` = bot deploy, diabaikan.)

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Putu Ngurah Semara | PutuNgurahSemara | 4 | 4 | 3 | **11** |
| Ilham Ahmad Fahriji | Hazley | 1 | 3 | 4 | **8** |

---

### C. Penilaian Individual

#### 1. Ilham Ahmad Fahriji (Lead Backend & DevOps — prime)
- Konsistensi 90 · Substansi 55 · Peran 60 · Pesan 72
- 8 commit, 3/3 minggu — konsisten, tapi kerja tidak mengarah ke deliverable microservices (tetap monolith + deploy).

**Nilai: 68** · **Grade: B** (prime, tanpa floor)

#### 2. Putu Ngurah Semara (Lead Frontend & QA & Docs — off-phase)
- Konsistensi 90 · Substansi 55 · Peran 60 · Pesan 72
- 11 commit, 3/3 minggu.

**Nilai mentah: 68** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook (tabel magang)

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **40**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231042 | Ilham Ahmad Fahriji | **68** |
| 10231075 | Putu Ngurah Semara | **70** |
