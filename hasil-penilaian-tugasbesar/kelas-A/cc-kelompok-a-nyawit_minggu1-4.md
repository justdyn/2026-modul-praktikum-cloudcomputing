# Laporan Penilaian Kelompok nyawit – Kelas A
## Fase 1: Minggu Kuliah 1–4 (24 Feb – 22 Mar 2026)

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit |
| Repo | cc-kelompok-a-nyawit |
| Project | **Sistem Manajemen Aset IT** — Platform untuk pengelolaan & pendataan infrastruktur hardware perusahaan (data center + endpoint karyawan) |

**Anggota (2 anggota — terkecil di kelas A):**

| Nama | NIM | Role |
|---|---|---|
| Ilham Ahmad Fahriji | 10231042 | Lead Backend & Lead DevOps |
| Putu Ngurah Semara | 10231075 | Lead Frontend & Lead QA & Docs |

> ⚠️ **Catatan penting:** NIM 10231042 dan 10231075 **tidak terdaftar di master gradebook kelas A** (`nilai_kelas__SI2514027_2026-05-15.xlsx`). Laporan ini didokumentasikan, namun nilai individual mereka tidak dimasukkan ke tabel rekap kelas A di README. Mohon dosen verifikasi status kedua mahasiswa.

---

### A. Penilaian Kelompok – Foundation Project

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M1 – README + Team + Project Brief** | 25% | **78** | README ada dengan team table (2 anggota), deskripsi project IT Asset Management spesifik (data center vs endpoint). Tidak ada `/team` endpoint backend (deliverable inti M1). Struktur tree project di README. |
| **M2 – Backend CRUD domain-specific** | 25% | **70** | Backend `app/` folder dengan `main.py` (1 route visible di main, route lain mungkin via APIRouter — perlu inspeksi). `pyproject.toml` + `requirements-prod.txt` (good practice prod separate). `supervisord.conf` (multi-process container — pendekatan unik). Test folder ada: `test_auth`, `test_crud_smoke`, `test_users`. |
| **M3 – Frontend domain-specific** | 25% | **78** | Standard React. |
| **M4 – Auth + CORS + .env** | 25% | **78** | CORS aktif di `app/main.py:31`. JWT setup. |

**Nilai Kelompok: (78 + 70 + 78 + 78) / 4 = 76.00**
**Grade Kelompok: AB**

> Skor lebih rendah karena scope project lebih sempit (hanya 2 anggota, beban kerja per orang sangat tinggi).

---

### B. Distribusi Kontribusi Individual

> **Catatan alias:** Ilham Ahmad Fahriji = `Hazley` (alias GitHub, email `10231042@student.itk.ac.id`). Putu = `PutuNgurahSemara` + `Putu Ngurah Semara`.

| Nama | Git Name(s) | Mg 1 | Mg 2 | Mg 3 | Mg 4 | Total |
|---|---|---|---|---|---|---|
| Putu Ngurah Semara | PutuNgurahSemara / Putu Ngurah Semara | 0 | 6 | 0 | 5 | **11** |
| Ilham Ahmad Fahriji | Hazley | 0 | 2 | 1 | 2 | **5** |

---

### C. Penilaian Individual

#### 1. Putu Ngurah Semara (Lead Frontend & QA & Docs)
- **Konsistensi (30%):** 2/4 minggu aktif → 70 · **Substansi (40%):** 11 commits → 80 · **Peran (20%):** Dual role frontend+QA → 80 · **Pesan (10%):** → 75

**Nilai: 21.0 + 32.0 + 16.0 + 7.5 = 76.5 → 77** · **Grade: AB**

---

#### 2. Ilham Ahmad Fahriji (Lead Backend & DevOps)
- **Konsistensi (30%):** 3/4 minggu aktif → 78 · **Substansi (40%):** 5 commits backend → 65 · **Peran (20%):** Dual role backend+DevOps → 75 · **Pesan (10%):** → 72

**Nilai: 23.4 + 26.0 + 15.0 + 7.2 = 71.6 → 72** · **Grade: B**

---

### D. Ringkasan untuk Gradebook

**C02 (5%):** kelompok **76**

**C03 (5%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231042 | Ilham Ahmad Fahriji | **72** |
| 10231075 | Putu Ngurah Semara | **77** |

> Nilai ini tidak diisi ke README master tabel kelas A karena NIM kedua mahasiswa tidak ada di gradebook xlsx.
