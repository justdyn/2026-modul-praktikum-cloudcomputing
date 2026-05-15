# Laporan Penilaian Kelompok ethereal – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ethereal |
| Repo | cc-kelompok-a-ethereal |
| Kelas | A |
| Project | **Kelarin** — Platform manajemen tugas akademik berbasis cloud-native untuk kolaborasi mahasiswa (penambahan tugas, deadline, distribusi tanggung jawab tim) |

**Anggota (dari `README.md`):**

| Nama | NIM | Role |
|---|---|---|
| Alsha Dwi Cahya | 10231011 | Lead Container |
| Amazia Devid Saputra | 10231013 | Lead Frontend |
| Andini Permata Sari | 10231015 | Lead QA & Docs |
| Ansellma Tita Pakartiwuri Putri | 10231017 | Lead Deploy & CI/CD |
| Tiya Mitra Ayu | 10231088 | Lead Backend |

> 5 anggota dengan role split Container + CI/CD + Deploy (granular seperti awit).

---

### A. Penilaian Kelompok – Foundation Project

> 4 kriteria @ 25%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **82** | README profesional: project brief (Kelarin task management), tabel team 5 anggota, tech stack, ASCII architecture diagram, JWT stateless explanation. Member docs `docs/member-*.md` per anggota. Bonus: `CHANGELOG.md` di root, `docs/retrospective-m1.md`. **Minus:** tidak ada `/team` endpoint di backend (deliverable inti M1 modul). |
| **M2 – Backend CRUD domain-specific** | 25% | **76** | Backend FastAPI dengan ~9 routes di `main.py`. Folder `routes/` ada tapi hanya berisi `__init__.py` kosong (struktur scaffold disiapkan tapi belum diisi). Layered: `models.py`, `schemas.py`, `crud.py`, `auth.py`, `database.py`, `pytest.ini`, `ruff.toml`. Scope endpoint lebih kecil dari peer (hexacore 40, awit 28). |
| **M3 – Frontend domain-specific** | 25% | **84** | React + Vite + **Tailwind CSS** + PostCSS, eslint config, struktur `src/`. Sesuai domain task management. |
| **M4 – Auth + CORS + .env** | 25% | **88** | JWT via `python-jose`. CORS dari env. `SECRET_KEY = os.getenv("SECRET_KEY")` **tanpa fallback** (`auth.py:41`) — best practice (paksa env wajib di-set, lebih aman dari peer yang punya fallback hardcoded). |

**Nilai Kelompok: (82 + 76 + 84 + 88) / 4 = 82.50 → 83**
**Grade Kelompok: AB**

---

### B. Distribusi Kontribusi Individual (git log W1–W4)

> **Catatan alias:** Tiya = `Tiyamitraayu` + `Tiyamitrayu` (typo) + `Tiyamitrayu` (email `.com` suffix). Devid = `Devid` + `Devid1013`. Ansel = `ansel` + `secretceremony` (email `ansellmatita@gmail.com`). Alsha = `dwialsha`. Andini = `gitandys`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Tiya Mitra Ayu | Tiyamitraayu / Tiyamitrayu | 7 | 2 | 0 | 3 | **12** |
| Alsha Dwi Cahya | dwialsha | 7 | 1 | 1 | 2 | **11** |
| Amazia Devid Saputra | Devid / Devid1013 | 6 | 1 | 2 | 2 | **11** |
| Ansellma Tita Pakartiwuri | secretceremony / ansel | 2 | 1 | 1 | 2 | **6** |
| Andini Permata Sari | gitandys | 2 | 1 | 1 | 1 | **5** |

---

### C. Penilaian Individual

#### 1. Amazia Devid Saputra (Lead Frontend)
- **Konsistensi (30%):** 4/4 minggu aktif → 92
- **Substansi (40%):** 11 commits frontend → 82
- **Kesesuaian Peran (20%):** Frontend → 86
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×92 + 0.40×82 + 0.20×86 + 0.10×78) = 27.6 + 32.8 + 17.2 + 7.8 = 85.4 → 85**
**Grade: AB**

---

#### 2. Alsha Dwi Cahya (Lead Container)
- **Konsistensi (30%):** 4/4 minggu aktif → 92
- **Substansi (40%):** 11 commits → 82
- **Kesesuaian Peran (20%):** Container belum prime time di F1 → 75
- **Kualitas Pesan (10%):** → 78

**Nilai: (0.30×92 + 0.40×82 + 0.20×75 + 0.10×78) = 27.6 + 32.8 + 15.0 + 7.8 = 83.2 → 83**
**Grade: AB**

---

#### 3. Tiya Mitra Ayu (Lead Backend)
- **Konsistensi (30%):** 3/4 minggu aktif (W3 kosong) → 80
- **Substansi (40%):** 12 commits — tertinggi kelompok → 84
- **Kesesuaian Peran (20%):** Backend → 84
- **Kualitas Pesan (10%):** Typo email berulang (`@student.itk.ac.id.com`) — minor → 72

**Nilai: (0.30×80 + 0.40×84 + 0.20×84 + 0.10×72) = 24.0 + 33.6 + 16.8 + 7.2 = 81.6 → 82**
**Grade: AB**

---

#### 4. Andini Permata Sari (Lead QA & Docs)
- **Konsistensi (30%):** 4/4 minggu aktif → 88
- **Substansi (40%):** 5 commits docs → 68
- **Kesesuaian Peran (20%):** Docs (member docs, testing-guide) → 84
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×88 + 0.40×68 + 0.20×84 + 0.10×75) = 26.4 + 27.2 + 16.8 + 7.5 = 77.9 → 78**
**Grade: AB**

---

#### 5. Ansellma Tita Pakartiwuri Putri (Lead Deploy & CI/CD)
- **Konsistensi (30%):** 4/4 minggu aktif → 88
- **Substansi (40%):** 6 commits — role CI/CD belum prime time di F1 → 72
- **Kesesuaian Peran (20%):** → 72
- **Kualitas Pesan (10%):** → 75

**Nilai: (0.30×88 + 0.40×72 + 0.20×72 + 0.10×75) = 26.4 + 28.8 + 14.4 + 7.5 = 77.1 → 77**
**Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C02 — Tugas terstruktur kelompok (5%):** semua anggota **83**

**C03 — Partisipasi & kontribusi mingguan via Git log (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | **83** |
| 10231013 | Amazia Devid Saputra | **85** |
| 10231015 | Andini Permata Sari | **78** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | **77** |
| 10231088 | Tiya Mitra Ayu | **82** |
