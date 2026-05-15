# Laporan Penilaian Kelompok antek-antek-asing – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | antek-antek-asing |
| Repo | cc-kelompok-a-antek-antek-asing |
| Kelas | A |
| Project | **Antick Async** — Sistem internal helpdesk berbasis cloud untuk manajemen tiket pekerjaan (maintenance, perbaikan, teknis) dengan 4 role: Employee, IT Support, Admin, Super Admin |

**Anggota (dari README + `/team` endpoint `backend/main.py:210`):**

| Nama | NIM | Role |
|---|---|---|
| Muhammad Athala Romero | 10231059 | Lead Backend |
| Muhammad Bagas Setiawan | 10231061 | Lead Frontend |
| Muhammad Fikri Haikal Ariadma | 10231063 | Lead DevOps |
| Nanda Aulia Putri | 10231067 | Lead QA & Docs |

---

### A. Penilaian Kelompok – Foundation Project

> 4 kriteria @ 25%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **88** | README komprehensif: deskripsi project, 4 role eksplisit dengan capabilities, fitur utama (Auth+Approval, Ticket Management, Notification, Admin Management), tech stack. `/team` endpoint ada. Member docs per anggota di `docs/`. |
| **M2 – Backend CRUD domain-specific** | 25% | **88** | Backend FastAPI 38 endpoint sesuai domain helpdesk: tickets, users, departments, notifications, approvals. Layered: `models.py`, `schemas.py`, `crud.py`, `config.py` (env management terpusat), `auth.py`, `database.py`. `pytest.ini` + folder `tests/`. SMTP integration untuk notification email. |
| **M3 – Frontend domain-specific** | 25% | **84** | React + Vite + **Tailwind CSS** + Nginx config. ESLint configured. `src/` terstruktur. Avatar feature, dashboard, ticket forms. Beberapa pesan commit kurang deskriptif menyulitkan trace evolusi UI. |
| **M4 – Auth + CORS + .env** | 25% | **88** | `config.py` mengelola SEMUA env vars terpusat (SECRET_KEY, ALGORITHM, TOKEN_EXPIRE, SUPERADMIN_*, SMTP_*). JWT via `python-jose`. Default empty string untuk SECRET_KEY (aman — paksa env wajib). RBAC 4 role. |

**Nilai Kelompok: (88 + 88 + 84 + 88) / 4 = 87.00**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W1–W4)

> **Catatan alias:** Haikal = `Haikal` = `FikriHaikal` = `ryota` (semua email `haikalariadma07@gmail.com`). Athala = `Muhammad Athala Romero` + `ItsHertz666` (email `m.athala08@gmail.com`). Bagas = `Muhammaad Bagas Setiawan` (typo nama) + `Muhammad Bagas Setiawan`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| M. Fikri Haikal Ariadma | Haikal | 10 | 2 | 2 | 0 | **14** |
| Muhammad Bagas Setiawan | Muhammaad Bagas Setiawan | 4 | 2 | 4 | 1 | **11** |
| Nanda Aulia Putri | Nanda Aulia Putri | 5 | 3 | 2 | 1 | **11** |
| Muhammad Athala Romero | Muhammad Athala Romero / ItsHertz666 | 3 | 3 | 2 | 1 | **9** |

---

### C. Penilaian Individual

> Bobot: Konsistensi 30% + Substansi 40% + Kesesuaian Peran 20% + Kualitas Pesan 10%

#### 1. Nanda Aulia Putri (Lead QA & Docs)
- **Konsistensi (30%):** 4/4 minggu aktif → 90
- **Substansi (40%):** 11 commits; member docs, api-test-results, testing-ui-projek, setup-guide → 80
- **Kesesuaian Peran (20%):** 100% di docs/QA → 88
- **Kualitas Pesan (10%):** Mix (deskriptif + generik) → 75

**Nilai: (0.30×90 + 0.40×80 + 0.20×88 + 0.10×75) = 27.0 + 32.0 + 17.6 + 7.5 = 84.1 → 84**
**Grade: AB**

---

#### 2. Muhammad Fikri Haikal Ariadma (Lead DevOps)
- **Konsistensi (30%):** 3/4 minggu aktif (W4 kosong) → 82
- **Substansi (40%):** 14 commits — tertinggi kelompok. Banyak setup awal → 84
- **Kesesuaian Peran (20%):** Mix DevOps + general setup (di F1 role DevOps belum dominan) → 78
- **Kualitas Pesan (10%):** Mix → 75

**Nilai: (0.30×82 + 0.40×84 + 0.20×78 + 0.10×75) = 24.6 + 33.6 + 15.6 + 7.5 = 81.3 → 81**
**Grade: AB**

---

#### 3. Muhammad Bagas Setiawan (Lead Frontend)
- **Konsistensi (30%):** 4/4 minggu aktif → 88
- **Substansi (40%):** 11 commits frontend → 78
- **Kesesuaian Peran (20%):** Frontend → 82
- **Kualitas Pesan (10%):** Generik → 72

**Nilai: (0.30×88 + 0.40×78 + 0.20×82 + 0.10×72) = 26.4 + 31.2 + 16.4 + 7.2 = 81.2 → 81**
**Grade: AB**

---

#### 4. Muhammad Athala Romero (Lead Backend)
- **Konsistensi (30%):** 4/4 minggu aktif → 86
- **Substansi (40%):** 9 commits backend → 78
- **Kesesuaian Peran (20%):** Backend → 82
- **Kualitas Pesan (10%):** Mix (beberapa terlalu pendek) → 72

**Nilai: (0.30×86 + 0.40×78 + 0.20×82 + 0.10×72) = 25.8 + 31.2 + 16.4 + 7.2 = 80.6 → 81**
**Grade: AB**

---

### D. Ringkasan untuk Gradebook

**C02 — Tugas terstruktur kelompok (5%):** semua anggota **87**

**C03 — Partisipasi & kontribusi mingguan via Git log (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231059 | Muhammad Athala Romero | **81** |
| 10231061 | Muhammad Bagas Setiawan | **81** |
| 10231063 | Muhammad Fikri Haikal Ariadma | **81** |
| 10231067 | Nanda Aulia Putri | **84** |
