# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Aplikasi | LenteraPustaka (manajemen perpustakaan) |
| Repo | cc-kelompok-a-hexacore |
| Kelas | A |

**Anggota (dari `/team` endpoint):**

| Nama | NIM | Role |
|---|---|---|
| Maulana Malik Ibrahim | 10231051 | Lead Backend |
| Micka Mayulia Utama | 10231053 | Lead Frontend |
| Khanza Nabila Tsabita | 10231049 | Lead DevOps |
| Muhammad Aqila Ardhi | 10231057 | Lead QA & Docs |

---

### A. Penilaian Kelompok (Kualitas Kode & Deliverable)

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| M1 – README + /team endpoint | 25% | 90 | /team lengkap dengan field `"app": "LenteraPustaka"`, README detail, setup.sh tersedia |
| M2 – Backend CRUD | 25% | 92 | 27 route (POST/PUT/DELETE/PATCH) – paling komprehensif di kelas; multi-entitas (buku, member, transaksi, denda) |
| M3 – React Frontend | 25% | 90 | Komponen lengkap + folder `hooks/` + folder `ui/` (custom UI library) |
| M4 – JWT + CORS + .env | 25% | 90 | JWT 3 file terpisah, CORSMiddleware, .env.example ✓ |

**Nilai Kelompok: (90 + 92 + 90 + 90) / 4 = 90.50**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W9–W12)

> W9 = Minggu 1 (24 Feb–1 Mar), W10 = Minggu 2 (2–8 Mar), W11 = Minggu 3 (9–15 Mar), W12 = Minggu 4 (16–22 Mar)

> **Catatan alias:** `mightyqilo13` dan `mightyqila13` = Muhammad Aqila Ardhi (NIM 10231057, dua akun GitHub, email yang sama). `x3naline` = Khanza Nabila Tsabita (email identik `nabilacaca.101099@gmail.com`).

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Maulana Malik Ibrahim | Maulana Malik Ibrahim | 8 | 13 | 10 | 6 | **37** |
| Khanza Nabila Tsabita | Khanza nabila t + x3naline | 5 | 2 | 7+1 | 6 | **21** |
| Micka Mayulia Utama | micka | 6 | 4 | 5 | 3 | **18** |
| Muhammad Aqila Ardhi | mightyqilo13 + mightyqila13 | 3+2 | 1 | 2 | 0 | **8** |

---

### C. Penilaian Individual

#### 1. Maulana Malik Ibrahim (Lead Backend)
- **Konsistensi (30%):** 4/4 minggu aktif → 95
- **Substansi (40%):** 37 commits – tertinggi kelompok; backend CRUD 27 routes, auth, denda – sangat substantif → 97
- **Kesesuaian Peran (20%):** Commit "Fix Testing denda", "Fix Blokir Member", "Fix Role Business Rules" – sesuai Backend → 95
- **Kualitas Pesan (10%):** Deskriptif tapi kadang informal ("modul 3 don") → 80

**Nilai: (0.30×95 + 0.40×97 + 0.20×95 + 0.10×80) = 28.5 + 38.8 + 19.0 + 8.0 = 94.3 → 94**
**Grade: A**

---

#### 2. Khanza Nabila Tsabita (Lead DevOps)
- **Konsistensi (30%):** 4/4 minggu aktif → 93
- **Substansi (40%):** 21 commits; DevOps mencakup setup Docker, CI/CD, dokumentasi → 88
- **Kesesuaian Peran (20%):** Commit terkait setup environment dan infrastructure → 88
- **Kualitas Pesan (10%):** Cukup deskriptif → 82

**Nilai: (0.30×93 + 0.40×88 + 0.20×88 + 0.10×82) = 27.9 + 35.2 + 17.6 + 8.2 = 88.9 → 89**
**Grade: A**

---

#### 3. Micka Mayulia Utama (Lead Frontend)
- **Konsistensi (30%):** 4/4 minggu aktif → 92
- **Substansi (40%):** 18 commits; frontend components + hooks + ui library → 87
- **Kesesuaian Peran (20%):** Commit "Frontend part 3", "Frontend part 4" sesuai role → 85
- **Kualitas Pesan (10%):** Sebagian umum ("Frontend part 4") → 70

**Nilai: (0.30×92 + 0.40×87 + 0.20×85 + 0.10×70) = 27.6 + 34.8 + 17.0 + 7.0 = 86.4 → 86**
**Grade: A**

---

#### 4. Muhammad Aqila Ardhi (Lead QA & Docs)
- **Konsistensi (30%):** 3/4 minggu aktif (tidak ada W12) → 75
- **Substansi (40%):** 8 commits; kontribusi terbatas dibanding anggota lain → 72
- **Kesesuaian Peran (20%):** Commit terkait testing dan docs – sesuai QA role → 78
- **Kualitas Pesan (10%):** Kurang konsisten → 70

**Nilai: (0.30×75 + 0.40×72 + 0.20×78 + 0.10×70) = 22.5 + 28.8 + 15.6 + 7.0 = 73.9 → 74**
**Grade: B**

---

### D. Rekap Nilai

| Nama | NIM | Role | Nilai Individu | Nilai Kelompok | Rata-rata | Grade |
|---|---|---|---|---|---|---|
| Maulana Malik Ibrahim | 10231051 | Lead Backend | 94 | 90.50 | 92.25 | **A** |
| Khanza Nabila Tsabita | 10231049 | Lead DevOps | 89 | 90.50 | 89.75 | **A** |
| Micka Mayulia Utama | 10231053 | Lead Frontend | 86 | 90.50 | 88.25 | **A** |
| Muhammad Aqila Ardhi | 10231057 | Lead QA & Docs | 74 | 90.50 | 82.25 | **AB** |

### E. Catatan

- Kelompok dengan kontribusi teknis terkaya di Kelas A: 27 routes CRUD, aplikasi perpustakaan dengan fitur denda, seeder data, dan custom UI hooks.
- Muhammad Aqila Ardhi perlu meningkatkan frekuensi dan konsistensi kontribusi.
- W13 commits (Maulana 1, Khanza 1) dikecualikan dari Fase 1.
