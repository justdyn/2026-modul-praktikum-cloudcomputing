# Laporan Penilaian Kelompok nyawit – Kelas A
## Fase 2: Minggu Kuliah 5–7 (23 Mar – 12 Apr 2026) — Containerization

---

### A. Penilaian Kelompok – Containerization

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M5 – Dockerfile per service** | 33% | **75** | Backend Dockerfile multi-stage (disebut di README). Pendekatan unik: `supervisord.conf` untuk run multi-process di 1 container (nginx + uvicorn). `requirements-prod.txt` separate. |
| **M6 – Docker Compose multi-container** | 33% | **70** | `docker-compose.yml` ada (di root + di backend/), tapi struktur agak duplikat. |
| **M7 – Optimasi & Production config** | 34% | **60** | **Tidak ada `docker-compose.prod.yml`** untuk production override — gap signifikan vs peer. Tidak ada dokumentasi `image-comparison.md`. |

**Nilai Kelompok: (75 + 70 + 60) / 3 = 68.33 → 68**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual

| Nama | Git Name(s) | W5 | W6 | W7 | Total |
|---|---|---|---|---|---|
| Ilham Ahmad Fahriji | Hazley | 6 | 0 | 1 | **7** |
| Putu Ngurah Semara | PutuNgurahSemara + Putu Ngurah | 1+4=5 | 0 | 0 | **5** |

---

### C. Penilaian Individual

#### 1. Ilham Ahmad Fahriji (Lead Backend & DevOps)
- **Konsistensi (30%):** 2/3 → 72 · **Substansi (40%):** 7 commits, role DevOps prime → 78 · **Peran (20%):** 100% DevOps F2 → 88 · **Pesan (10%):** → 75

**Nilai: 21.6 + 31.2 + 17.6 + 7.5 = 77.9 → 78** · **Grade: AB**

---

#### 2. Putu Ngurah Semara (Lead Frontend & QA & Docs)
- **Konsistensi (30%):** 1/3 → 60 · **Substansi (40%):** 5 commits → 72 · **Peran (20%):** Mixed → 75 · **Pesan (10%):** → 75

**Nilai: 18.0 + 28.8 + 15.0 + 7.5 = 69.3 → 69** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C05 (4%):** kelompok **68**

**C06 (4%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231042 | Ilham Ahmad Fahriji | **78** |
| 10231075 | Putu Ngurah Semara | **69** |
