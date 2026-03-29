# Laporan Penilaian Kelompok nyawit – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit |
| Aplikasi | IT Asset Management System |
| Repo | cc-kelompok-a-nyawit |
| Kelas | A |

**Anggota (dari git log – `/team` endpoint tidak ada):**

| Git Name | NIM (dari email) | Commits W1-4 |
|---|---|---|
| PutuNgurahSemara / Putu Ngurah Semara | Tidak diketahui (email non-ITK) | 11 |
| Hazley | 10231042 | 5 |

> **Catatan:** Tidak ditemukan endpoint `/team` di backend. Kelompok hanya memiliki 2 kontributor aktif.

---

### A. Penilaian Kelompok (Kualitas Kode & Deliverable)

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| M1 – README + /team endpoint | 25% | 40 | **Tidak ada `/team` endpoint** – kebutuhan utama Modul 1 tidak terpenuhi. README ada. |
| M2 – Backend CRUD | 25% | 90 | 23 routes CRUD + auth + role-based access – sangat komprehensif. Multi-entitas (assets, borrow_logs, categories, users). |
| M3 – React Frontend | 25% | 92 | TypeScript React dengan 15+ komponen (charts, dialogs, sidebar, navigation) – jauh di atas rata-rata kelas |
| M4 – JWT + CORS + .env | 25% | 75 | JWT 4 file ✓, CORSMiddleware ✓, tetapi **tidak ada `.env.example`** |

**Nilai Kelompok: (40 + 90 + 92 + 75) / 4 = 74.25**
**Grade Kelompok: B**

---

### B. Distribusi Kontribusi Individual (git log W9–W12)

> W9 = Minggu 1 (24 Feb–1 Mar), W10 = Minggu 2 (2–8 Mar), W11 = Minggu 3 (9–15 Mar), W12 = Minggu 4 (16–22 Mar)

> **Catatan alias:** `PutuNgurahSemara` + `Putu Ngurah Semara` = orang yang sama (email GitHub noreply berbeda tapi identitas sama). Kedua kontributor **tidak ada commit di Minggu 1 (W9)**.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| PutuNgurahSemara | PutuNgurahSemara + Putu Ngurah Semara | 0 | 3+3 | 0 | 5 | **11** |
| Hazley | Hazley | 0 | 2 | 1 | 2 | **5** |

---

### C. Penilaian Individual

#### 1. PutuNgurahSemara
- **Konsistensi (30%):** 2/4 minggu aktif (tidak ada W9 dan W11) → 55
- **Substansi (40%):** 11 commits; sangat aktif di W10 dan W12; substansi tinggi (setup FastAPI, JWT, PostgreSQL, Docker Compose) → 85
- **Kesesuaian Peran (20%):** Backend + infra setup → 82
- **Kualitas Pesan (10%):** Campuran baik ("feat: Add JWT authentication") dan informal ("rapihin") → 72

**Nilai: (0.30×55 + 0.40×85 + 0.20×82 + 0.10×72) = 16.5 + 34.0 + 16.4 + 7.2 = 74.1 → 74**
**Grade: B**

---

#### 2. Hazley (NIM: 10231042)
- **Konsistensi (30%):** 3/4 minggu aktif (tidak ada W9) → 70
- **Substansi (40%):** 5 commits; frontend/general → 65
- **Kesesuaian Peran (20%):** Commit "tambah log in/out", "Update README" → 68
- **Kualitas Pesan (10%):** Campuran → 68

**Nilai: (0.30×70 + 0.40×65 + 0.20×68 + 0.10×68) = 21.0 + 26.0 + 13.6 + 6.8 = 67.4 → 67**
**Grade: B**

---

### D. Rekap Nilai

| Nama | NIM | Role | Nilai Individu | Nilai Kelompok | Rata-rata | Grade |
|---|---|---|---|---|---|---|
| PutuNgurahSemara | Tidak diketahui | — | 74 | 74.25 | 74.13 | **B** |
| Hazley | 10231042 | — | 67 | 74.25 | 70.63 | **B** |

### E. Catatan & Flag

- **FLAG KRITIS:** Tidak ada `/team` endpoint → kewajiban utama Modul 1 tidak dipenuhi → M1 sangat rendah.
- **FLAG:** Tidak ada `.env.example` → M4 dikurangi.
- **FLAG:** Tidak ada commit di Minggu 1 (W9) – kedua anggota baru mulai di W10.
- **FLAG:** Hanya 2 kontributor teridentifikasi. Jika ada anggota lain yang belum commit, mohon dikonfirmasi.
- Secara teknis, kelompok ini memiliki implementasi **paling canggih di Kelas A** (TypeScript, charts, role-based auth) tetapi gagal memenuhi deliverable dasar (no /team endpoint, tidak ada .env.example).
- Perlu konfirmasi NIM Putu Ngurah Semara (email `ngurahgondol1260@gmail.com`, tidak ada email ITK di git).
