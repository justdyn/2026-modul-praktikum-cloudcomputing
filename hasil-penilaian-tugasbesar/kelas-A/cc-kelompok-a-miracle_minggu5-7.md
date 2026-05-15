# Laporan Penilaian Kelompok miracle – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### A. Penilaian Kelompok – Containerization

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **92** | Backend & frontend Dockerfile multi-stage. **Optimasi terdokumentasi konkret di README:** Backend 1.2GB→216MB (~82%), Frontend 1.1GB→93.8MB (~91%). Teknik: multi-stage build, Alpine base, `.dockerignore`, non-root user, healthcheck. |
| **M6 – Docker Compose multi-container** | 33% | **88** | Standard 3-service compose dengan healthcheck. |
| **M7 – Optimasi & Production config** | 34% | **90** | `docker-compose.prod.yml` ada. Dokumentasi reduction ratio image terbukti di README. |

**Nilai Kelompok: (92 + 88 + 90) / 3 = 90.00 → 90**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual

> W5 NOT zero — miracle aktif W5 (beda dari kelompok lain).

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| Avhilla Catton Andalucia | Avhilla Catton Andalucia | 3 | 3 | 4 | **10** |
| Debora Intania Subekti | intniaaa20 | 2 | 0 | 5 | **7** |
| Yosan Pratiwi | Yosan Pratiwi | 1 | 0 | 3 | **4** |
| Chelsy Olivia | Chelsy Olivia | 0 | 2 | 0 | **2** |
| Betran | BETRAN | 0 | 1 | 0 | **1** |

---

### C. Penilaian Individual

#### 1. Avhilla Catton Andalucia (Lead Container)
- **Konsistensi (30%):** 3/3 → 95 · **Substansi (40%):** 10 commits, role prime time → 88 · **Peran (20%):** 100% containerization → 96 · **Pesan (10%):** → 82

**Nilai: 28.5 + 35.2 + 19.2 + 8.2 = 91.1 → 91** · **Grade: A**

---

#### 2. Debora Intania Subekti (Lead Backend)
- **Konsistensi (30%):** 2/3 → 75 · **Substansi (40%):** 7 commits → 78 · **Peran (20%):** Backend dockerization → 82 · **Pesan (10%):** → 78

**Nilai: 22.5 + 31.2 + 16.4 + 7.8 = 77.9 → 78** · **Grade: AB**

---

#### 3. Yosan Pratiwi (Lead Frontend)
- **Konsistensi (30%):** 2/3 → 72 · **Substansi (40%):** 4 commits → 68 · **Peran (20%):** Frontend → 80 · **Pesan (10%):** → 75

**Nilai: 21.6 + 27.2 + 16.0 + 7.5 = 72.3 → 72** · **Grade: B**

---

#### 4. Chelsy Olivia (Lead CI/CD & Deploy)
- **Konsistensi (30%):** 1/3 → 55 · **Substansi (40%):** 2 commits → 58 · **Peran (20%):** CI/CD belum F2 prime → 65 · **Pesan (10%):** → 75

**Nilai: 16.5 + 23.2 + 13.0 + 7.5 = 60.2 → 60** · **Grade: BC**

---

#### 5. Betran (Lead QA & Docs)
- **Konsistensi (30%):** 1/3 → 50 · **Substansi (40%):** 1 commit → 50 · **Peran (20%):** Docs → 65 · **Pesan (10%):** → 70

**Nilai: 15.0 + 20.0 + 13.0 + 7.0 = 55.0 → 55** · **Grade: BC**

---

### D. Ringkasan untuk Gradebook

**C05 (4%):** semua anggota **90**

**C06 (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | **91** |
| 10231023 | Betran | **55** |
| 10231025 | Chelsy Olivia | **60** |
| 10231029 | Debora Intania Subekti | **78** |
| 10231091 | Yosan Pratiwi | **72** |
