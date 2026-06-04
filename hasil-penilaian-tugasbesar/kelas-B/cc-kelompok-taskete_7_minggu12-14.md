# Laporan Penilaian Kelompok taskete_7 – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | taskete_7 |
| Repo | cc-kelompok-taskete_7 |
| Project | **Sistem Manajemen SDM Cuti Karyawan** — didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota** (Rayhan magang — dinilai di tabel magang):

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Amalia Tiara Rezfani | 10231012 | Lead QA & Docs | off-phase |
| Irwan Maulana | 10231046 | Lead Frontend | off-phase |
| Noviansyah | 10231072 | Lead Backend | ✅ prime |
| Rayhan Iqbal 🎓 | 10231080 | Lead DevOps | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **86** | `docs/architecture.md` (401 baris): batas domain, kontrak API, topologi gateway. |
| **M13 – Implementasi microservices** | 33% | **92** | `services/auth-service` + `services/item-service` + `services/gateway`. `docker-compose` 6 container. **Inter-service auth** + **circuit breaker**. |
| **M14 – Architecture diagram + monitoring** | 34% | **78** | Diagram + circuit breaker. Minus: belum ada metrics collector. |

**Nilai Kelompok: (86 + 92 + 78) / 3 = 85.33 → 85**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Amalia = `10231012tiara`; Irwan = `Irwan Maulana`/`Irwannnnn`; Noviansyah = `Noviansyahhh`; Rayhan = `RayhanIqbal80`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Amalia Tiara Rezfani | 10231012tiara | 2 | 11 | 1 | **14** |
| Rayhan Iqbal 🎓 | RayhanIqbal80 | 4 | 4 | 0 | **8** |
| Irwan Maulana | Irwan Maulana | 2 | 3 | 1 | **6** |
| Noviansyah | Noviansyahhh | 2 | 2 | 1 | **5** |

---

### C. Penilaian Individual

#### 1. Amalia Tiara Rezfani (Lead QA & Docs — off-phase)
- Konsistensi 90 · Substansi 82 · Peran 76 · Pesan 80 — 14 commit, 3/3 minggu, dokumentasi arsitektur (arch.md 401 baris) + paling aktif. Di atas floor.

**Nilai: 83** · **Grade: AB**

#### 2. Noviansyah (Lead Backend — prime)
- Konsistensi 90 · Substansi 78 · Peran 88 · Pesan 78 — 5 commit, 3/3 minggu, dekomposisi backend.

**Nilai: 84** · **Grade: AB**

#### 3. Rayhan Iqbal 🎓 (Lead DevOps — prime, magang)
- Konsistensi 75 · Substansi 82 · Peran 88 · Pesan 80 — 8 commit, gateway/infra.

**Nilai: 81** · **Grade: AB** *(masuk tabel magang)*

#### 4. Irwan Maulana (Lead Frontend — off-phase)
- Konsistensi 90 · Substansi 76 · Peran 74 · Pesan 78 — 6 commit, 3/3 minggu. Di atas floor.

**Nilai: 80** · **Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **85**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231012 | Amalia Tiara Rezfani | **83** |
| 10231046 | Irwan Maulana | **80** |
| 10231072 | Noviansyah | **84** |
| 10231080 | Rayhan Iqbal 🎓 (magang) | **81** |
