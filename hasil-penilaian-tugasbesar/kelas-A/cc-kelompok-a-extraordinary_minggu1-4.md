# Laporan Penilaian Kelompok extraordinary – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | extraordinary |
| Repo | cc-kelompok-a-extraordinary |
| Project | **Temuin** — Sistem terpusat lost & found untuk civitas kampus ITK (pelacakan barang hilang/temuan dengan verifikasi kepemilikan) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Nicholas Christian Samuel Manurung | 10231069 | Lead Frontend |
| Pangeran Borneo Silaen | 10231073 | Lead DevOps |
| Raisha Alika Irwandira | 10231077 | Lead Backend |
| Rani Ayu Dewi | 10231079 | Lead QA & Docs |

---

### A. Penilaian Kelompok – Foundation Project

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **88** | README sangat lengkap dengan ToC 11 section, latar belakang masalah ITK lost & found, Mermaid arsitektur diagram, tech stack, automation `temuin.ps1` (PowerShell helper). Bonus: `AGENTS.md` di root. Tidak ada `/team` endpoint di backend (deliverable inti M1) — minus kecil. |
| **M2 – Backend CRUD domain-specific** | 25% | **90** | **Arsitektur terbaik di kelas A**: FastAPI dengan APIRouter pattern modular per domain — folder `app/{auth,claims,items,master_data,notifications}/` masing-masing punya `router.py + service.py + schemas.py`. Models terpisah di `app/models/{audit,claim,item,master_data,notification,user}.py`. Total ~25 routes. `alembic/` migrations. Pydantic `Settings` class untuk env. |
| **M3 – Frontend domain-specific** | 25% | **84** | Frontend sesuai domain, struktur standar. |
| **M4 – Auth + CORS + .env** | 25% | **88** | JWT (`app/dependencies.py`), CORS, `app/config.py` pakai `pydantic-settings` (lebih bersih dari `os.getenv`). |

**Nilai Kelompok: (88 + 90 + 84 + 88) / 4 = 87.50 → 88**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual

> **Catatan alias:** Pangeran = `PangeranSilaen` + `Pangeran Borneo Silaen`. Raisha = `disnejy` (email `rayshalika15@gmail.com`). Nicholas = `nicholasmnrng` + `nicholasmnrngu`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Pangeran Borneo Silaen | PangeranSilaen | 4 | 4 | 1 | 3 | **12** |
| Rani Ayu Dewi | raniayudewi | 4 | 5 | 2 | 0 | **11** |
| Raisha Alika Irwandira | disnejy | 2 | 5 | 0 | 0 | **7** |
| Nicholas Christian S. Manurung | nicholasmnrng / nicholasmnrngu | 1 | 1 | 1 | 0 | **3** |

---

### C. Penilaian Individual

#### 1. Pangeran Borneo Silaen (Lead DevOps)
- **Konsistensi (30%):** 4/4 → 92
- **Substansi (40%):** 12 commits → 84
- **Kesesuaian Peran (20%):** Mix (DevOps belum prime time di F1) → 78
- **Kualitas Pesan (10%):** → 78

**Nilai: 27.6 + 33.6 + 15.6 + 7.8 = 84.6 → 85** · **Grade: AB**

---

#### 2. Rani Ayu Dewi (Lead QA & Docs)
- **Konsistensi (30%):** 3/4 (W4 kosong) → 80
- **Substansi (40%):** 11 commits → 80
- **Kesesuaian Peran (20%):** Docs/QA → 86
- **Kualitas Pesan (10%):** → 78

**Nilai: 24.0 + 32.0 + 17.2 + 7.8 = 81.0 → 81** · **Grade: AB**

---

#### 3. Raisha Alika Irwandira (Lead Backend)
- **Konsistensi (30%):** 2/4 minggu aktif → 70
- **Substansi (40%):** 7 commits backend → 76
- **Kesesuaian Peran (20%):** Backend → 84
- **Kualitas Pesan (10%):** Email non-ITK (`rayshalika15@gmail.com`) → 70

**Nilai: 21.0 + 30.4 + 16.8 + 7.0 = 75.2 → 75** · **Grade: B**

---

#### 4. Nicholas Christian Samuel Manurung (Lead Frontend)
- **Konsistensi (30%):** 3/4 minggu aktif → 80
- **Substansi (40%):** 3 commits → 58
- **Kesesuaian Peran (20%):** Frontend → 76
- **Kualitas Pesan (10%):** → 72

**Nilai: 24.0 + 23.2 + 15.2 + 7.2 = 69.6 → 70** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C02 (5%):** semua anggota **88**

**C03 (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231069 | Nicholas Christian Samuel Manurung | **70** |
| 10231073 | Pangeran Borneo Silaen | **85** |
| 10231077 | Raisha Alika Irwandira | **75** |
| 10231079 | Rani Ayu Dewi | **81** |
