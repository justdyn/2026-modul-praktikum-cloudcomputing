# Laporan Penilaian Kelompok miracle – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | miracle |
| Repo | cc-kelompok-a-miracle |
| Project | **Donor Manajemen** — sistem manajemen pendonor darah, didekomposisi jadi Auth + Item Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Avhilla Catton Andalucia | 10231021 | Lead Container | ✅ prime |
| Betran | 10231023 | Lead QA & Docs | off-phase |
| Chelsy Olivia | 10231025 | Lead CI/CD & Deploy | ✅ prime |
| Debora Intania Subekti | 10231029 | Lead Backend | ✅ prime |
| Yosan Pratiwi | 10231091 | Lead Frontend | off-phase |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **64** | Tidak ada `docs/architecture.md` / ADR (hanya `docs/docker-architecture.md` warisan F2). Batas domain terimplementasi tapi tidak terdokumentasi sebagai ADR. |
| **M13 – Implementasi microservices** | 33% | **92** | Dekomposisi penuh: `services/auth-service` + `services/item-service` + `services/gateway` (nginx). `docker-compose.yml` 9 container. **Inter-service comm** `services/item-service/auth_client.py` + **resilience** `services/item-service/circuit_breaker.py`. |
| **M14 – Architecture diagram + monitoring** | 34% | **70** | Circuit breaker sebagai pola reliability. Minus: tidak ada diagram arsitektur microservices terdokumentasi, belum ada metrics collector. |

**Nilai Kelompok: (64 + 92 + 70) / 3 = 75.33 → 75**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Chelsy = `chelolv15`/`Chelsy Olivia`; Avhilla = `Avhilla`/`Avhilla Catton Andalucia`; Debora = `Debora Intania Subekti`/`intniaaa20`; Betran = `Betran`/`BETRAN`; Yosan = `Yosan Pratiwi`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Chelsy Olivia | chelolv15 / Chelsy Olivia | 5 | 12 | 0 | **17** |
| Yosan Pratiwi | Yosan Pratiwi | 0 | 4 | 4 | **8** |
| Avhilla Catton Andalucia | Avhilla | 1 | 4 | 2 | **7** |
| Debora Intania Subekti | intniaaa20 / Debora | 0 | 4 | 1 | **5** |
| Betran | Betran / BETRAN | 0 | 1 | 1 | **2** |

---

### C. Penilaian Individual

#### 1. Chelsy Olivia (Lead CI/CD & Deploy — prime)
- Konsistensi 75 · Substansi 90 · Peran 92 · Pesan 82
- 17 commit, motor gateway + compose + CI microservices.

**Nilai: 85** · **Grade: AB**

#### 2. Avhilla Catton Andalucia (Lead Container — prime)
- Konsistensi 90 · Substansi 82 · Peran 88 · Pesan 80
- 7 commit, 3/3 minggu, containerization service.

**Nilai: 85** · **Grade: AB**

#### 3. Debora Intania Subekti (Lead Backend — prime)
- Konsistensi 75 · Substansi 82 · Peran 90 · Pesan 80
- 5 commit, backend decomposition item-service.

**Nilai: 81** · **Grade: AB**

#### 4. Yosan Pratiwi (Lead Frontend — off-phase)
- Konsistensi 75 · Substansi 80 · Peran 78 · Pesan 78
- 8 commit, 2/3 minggu. Di atas floor.

**Nilai: 78** · **Grade: AB**

#### 5. Betran (Lead QA & Docs — off-phase)
- Konsistensi 70 · Substansi 60 · Peran 70 · Pesan 72
- 2 commit, 2/3 minggu.

**Nilai mentah: 66** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **75**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | **85** |
| 10231023 | Betran | **70** |
| 10231025 | Chelsy Olivia | **85** |
| 10231029 | Debora Intania Subekti | **81** |
| 10231091 | Yosan Pratiwi | **78** |
