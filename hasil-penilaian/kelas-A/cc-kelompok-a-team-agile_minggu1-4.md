# Laporan Penilaian Kelompok team-agile – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | team-agile |
| Repo | cc-kelompok-a-team-agile |
| Kelas | A |

**Anggota (dari `/team` endpoint):**

| Nama | NIM | Role |
|---|---|---|
| Arthur Tirtajaya Jehuda | 10231019 | Lead Backend |
| Dahayu Azhka Daeshawnda | 10231027 | Lead Frontend |
| Norbertino Eurakha Nandatoti | 10231071 | Lead DevOps |

---

### A. Penilaian Kelompok (Kualitas Kode & Deliverable)

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| M1 – README + /team endpoint | 25% | 60 | /team ada tapi field `"team"` masih `"cloud-team-XX"`, hanya 3 anggota (kurang dari minimum 4), README ada |
| M2 – Backend CRUD | 25% | 65 | 8 routes tapi tidak ada JWT auth – CRUD tanpa autentikasi |
| M3 – React Frontend | 25% | 68 | Komponen ada (Header, ItemCard, ItemForm, ItemList, SearchBar) tapi **tidak ada LoginPage** karena tidak ada auth |
| M4 – JWT + CORS + .env | 25% | 50 | **Tidak ada JWT**, CORSMiddleware ✓, .env.example ✓ |

**Nilai Kelompok: (60 + 65 + 68 + 50) / 4 = 60.75**
**Grade Kelompok: C**

---

### B. Distribusi Kontribusi Individual (git log W9–W12)

> W9 = Minggu 1 (24 Feb–1 Mar), W10 = Minggu 2 (2–8 Mar), W11 = Minggu 3 (9–15 Mar), W12 = Minggu 4 (16–22 Mar)

> **Catatan:** `wounderfvl` = Dahayu Azhka Daeshawnda (NIM 10231027, email 10231027@student.itk.ac.id). Seluruh commit kelompok **hanya ada di Minggu 2 (W10) dan Minggu 3 (W11)**. Tidak ada commit di W9 (Minggu 1) dan W12 (Minggu 4).

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Dahayu Azhka Daeshawnda | wounderfvl | 0 | 3 | 3 | 0 | **6** |
| Arthur Tirtajaya Jehuda | Arthur Tirtajaya Jehuda | 0 | 3 | 0 | 0 | **3** |
| Norbertino Eurakha Nandatoti | Norbertino Rakha | 0 | 3 | 0 | 0 | **3** |

---

### C. Penilaian Individual

#### 1. Dahayu Azhka Daeshawnda (Lead Frontend)
- **Konsistensi (30%):** 2/4 minggu aktif (W10, W11 saja) → 50
- **Substansi (40%):** 6 commits; React CRUD frontend dengan komponen + sorting → 70
- **Kesesuaian Peran (20%):** Frontend components sesuai → 75
- **Kualitas Pesan (10%):** Menggunakan conventional commits ("feat:", "fix:", "docs:") → 88

**Nilai: (0.30×50 + 0.40×70 + 0.20×75 + 0.10×88) = 15.0 + 28.0 + 15.0 + 8.8 = 66.8 → 67**
**Grade: B**

---

#### 2. Arthur Tirtajaya Jehuda (Lead Backend)
- **Konsistensi (30%):** 1/4 minggu aktif (W10 saja) → 30
- **Substansi (40%):** 3 commits; backend REST API CRUD dengan PostgreSQL → 68
- **Kesesuaian Peran (20%):** Backend setup sesuai → 75
- **Kualitas Pesan (10%):** Menggunakan conventional commits ("feat:", "docs:") → 88

**Nilai: (0.30×30 + 0.40×68 + 0.20×75 + 0.10×88) = 9.0 + 27.2 + 15.0 + 8.8 = 60.0 → 60**
**Grade: C**

---

#### 3. Norbertino Eurakha Nandatoti (Lead DevOps)
- **Konsistensi (30%):** 1/4 minggu aktif (W10 saja) → 30
- **Substansi (40%):** 3 commits; docs dan member info → 60
- **Kesesuaian Peran (20%):** Commit DevOps setup minimal → 65
- **Kualitas Pesan (10%):** Menggunakan conventional commits → 88

**Nilai: (0.30×30 + 0.40×60 + 0.20×65 + 0.10×88) = 9.0 + 24.0 + 13.0 + 8.8 = 54.8 → 55**
**Grade: C**

---

### D. Rekap Nilai

| Nama | NIM | Role | Nilai Individu | Nilai Kelompok | Rata-rata | Grade |
|---|---|---|---|---|---|---|
| Dahayu Azhka Daeshawnda | 10231027 | Lead Frontend | 67 | 60.75 | 63.88 | **BC** |
| Arthur Tirtajaya Jehuda | 10231019 | Lead Backend | 60 | 60.75 | 60.38 | **C** |
| Norbertino Eurakha Nandatoti | 10231071 | Lead DevOps | 55 | 60.75 | 57.88 | **C** |

### E. Catatan & Flag

- **FLAG:** Tidak ada commit di Minggu 1 (W9) dan Minggu 4 (W12). Kelompok baru mulai di W10.
- **FLAG:** Tidak ada implementasi JWT – kebutuhan Modul 4 tidak terpenuhi.
- **FLAG:** Field `"team"` masih `"cloud-team-XX"` – tidak diperbarui.
- **FLAG:** Hanya 3 anggota (minimum seharusnya 4).
- Kualitas pesan commit sangat baik (conventional commits) – satu kelebihan kelompok ini.
- Perlu konfirmasi apakah ada anggota ke-4 yang belum terdaftar.
