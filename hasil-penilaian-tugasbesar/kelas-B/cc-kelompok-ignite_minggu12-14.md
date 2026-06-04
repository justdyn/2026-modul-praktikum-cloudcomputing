# Laporan Penilaian Kelompok ignite – Kelas B
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ignite |
| Repo | cc-kelompok-ignite |
| Project | **E-commerce / Inventory** — katalog produk + statistik inventori, didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Andini Permata Dewanti | 10231014 | Lead Backend | ✅ prime |
| Desnita Dwi Putri | 10231030 | Lead Frontend | off-phase |
| Krishandy Dhanysa Pratama | 10231050 | Lead DevOps | ✅ prime |
| Putri Rahmawati | 10231074 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **90** | `docs/architecture.md` (**1082 baris** — paling lengkap di kelas B): batas domain, kontrak API, panduan per service, diagram. |
| **M13 – Implementasi microservices** | 33% | **92** | `services/auth-service` + `services/item-service` + `services/gateway` (nginx). `docker-compose` 6 container. **Inter-service auth** + **circuit breaker**. |
| **M14 – Architecture diagram + monitoring** | 34% | **78** | Diagram + circuit breaker (resilience). Minus: belum ada metrics collector. |

**Nilai Kelompok: (90 + 92 + 78) / 3 = 86.67 → 87**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Krishandy = `Krishandy Dhanysa Pratama`; Putri = `10231074-sketch`/`Putri Rahmawati`; Desnita = `desnitadwip`; Andini = `Andini Permata Dewanti`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Krishandy Dhanysa Pratama | Krishandy Dhanysa Pratama | 4 | 7 | 2 | **13** |
| Putri Rahmawati | 10231074-sketch | 2 | 1 | 0 | **3** |
| Andini Permata Dewanti | Andini Permata Dewanti | 0 | 2 | 0 | **2** |
| Desnita Dwi Putri | desnitadwip | 1 | 1 | 0 | **2** |

---

### C. Penilaian Individual

#### 1. Krishandy Dhanysa Pratama (Lead DevOps — prime)
- Konsistensi 90 · Substansi 88 · Peran 92 · Pesan 80 — 13 commit, 3/3 minggu, gateway/infra core.

**Nilai: 89** · **Grade: A**

#### 2. Putri Rahmawati (Lead QA & Docs — off-phase)
- Konsistensi 70 · Substansi 78 · Peran 74 · Pesan 78 — 3 commit, dokumentasi arsitektur (arch.md 1082 baris). Di atas floor.

**Nilai: 75** · **Grade: B**

#### 3. Andini Permata Dewanti (Lead Backend — prime)
- Konsistensi 50 · Substansi 65 · Peran 80 · Pesan 76 — 2 commit, 1/3 minggu.

**Nilai: 65** · **Grade: BC** (prime, tanpa floor)

#### 4. Desnita Dwi Putri (Lead Frontend — off-phase)
- Konsistensi 70 · Substansi 62 · Peran 70 · Pesan 75 — 2 commit, 2/3 minggu.

**Nilai mentah: 67** → off-phase + raw ≥ 50 → **floor 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **87**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231014 | Andini Permata Dewanti | **65** |
| 10231030 | Desnita Dwi Putri | **70** |
| 10231050 | Krishandy Dhanysa Pratama | **89** |
| 10231074 | Putri Rahmawati | **75** |
