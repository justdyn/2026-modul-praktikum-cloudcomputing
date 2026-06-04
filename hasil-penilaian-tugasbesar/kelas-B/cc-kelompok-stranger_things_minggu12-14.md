# Laporan Penilaian Kelompok stranger_things – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | stranger_things |
| Repo | cc-kelompok-stranger_things |
| Project | Sistem manajemen jadwal imunisasi — didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Ahmad Daffa Alfattah | 10231008 | Lead Backend | ✅ prime |
| Cintya Widhi Astuti | 10231026 | Lead DevOps | ✅ prime |
| Nazwa Amelia Zahra | 10231068 | Lead Frontend | off-phase |
| Verina Rahma Dinah | 10231090 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **85** | `docs/architecture.md` (326 baris): batas domain, kontrak API, topologi gateway. |
| **M13 – Implementasi microservices** | 33% | **92** | `services/auth-service` + `services/item-service` + `services/gateway`. `docker-compose` 9 container. **Inter-service auth** + **circuit breaker**. |
| **M14 – Architecture diagram + monitoring** | 34% | **78** | Diagram + circuit breaker (resilience). Minus: belum ada metrics collector. |

**Nilai Kelompok: (85 + 92 + 78) / 3 = 85.00 → 85**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> W14 kosong seluruh tim. **Alias:** Cintya = `10231026-stack`/`Cintya`; Ahmad Daffa = `Ahmad Daffa`; Nazwa = `Nazwa Amelia Zahra`; Verina = `verinaaaa`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Ahmad Daffa Alfattah | Ahmad Daffa | 14 | 2 | 0 | **16** |
| Cintya Widhi Astuti | 10231026-stack / Cintya | 2 | 6 | 0 | **8** |
| Nazwa Amelia Zahra | Nazwa Amelia Zahra | 2 | 3 | 0 | **5** |
| Verina Rahma Dinah | verinaaaa | 4 | 1 | 0 | **5** |

---

### C. Penilaian Individual

#### 1. Ahmad Daffa Alfattah (Lead Backend — prime)
- Konsistensi 75 · Substansi 90 · Peran 90 · Pesan 80 — 16 commit, motor dekomposisi backend.

**Nilai: 85** · **Grade: AB**

#### 2. Cintya Widhi Astuti (Lead DevOps — prime)
- Konsistensi 75 · Substansi 82 · Peran 88 · Pesan 80 — 8 commit, gateway/infra.

**Nilai: 81** · **Grade: AB**

#### 3. Verina Rahma Dinah (Lead QA & Docs — off-phase)
- Konsistensi 75 · Substansi 76 · Peran 74 · Pesan 78 — 5 commit, dokumentasi arsitektur. Di atas floor.

**Nilai: 76** · **Grade: AB**

#### 4. Nazwa Amelia Zahra (Lead Frontend — off-phase)
- Konsistensi 75 · Substansi 74 · Peran 72 · Pesan 76 — 5 commit, 2/3 minggu. Di atas floor.

**Nilai: 74** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **85**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231008 | Ahmad Daffa Alfattah | **85** |
| 10231026 | Cintya Widhi Astuti | **81** |
| 10231068 | Nazwa Amelia Zahra | **74** |
| 10231090 | Verina Rahma Dinah | **76** |
