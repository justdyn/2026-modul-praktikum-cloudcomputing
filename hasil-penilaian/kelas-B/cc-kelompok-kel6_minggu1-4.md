# Laporan Penilaian Tugas Terstruktur — Minggu 1-4
**Kelompok:** cc-kelompok-kel6
**Tanggal Penilaian:** 29 Maret 2026

---

## A. Identitas Kelompok

| Nama | NIM | Peran |
|------|-----|-------|
| Achmad Bayhaqi | 10231001 | Lead Backend |
| Indah Nur Fortuna | 10231044 | Lead Frontend |
| Alfiani Dwiyuniarti | 10231010 | Lead DevOps |
| Zahwa Hanna Dwi Putri | 10231092 | Lead CI/CD & Deploy |
| Nilam Ayu NandaStari Romdoni | 10231070 | Lead QA & Docs |

> Kelompok 5 orang (Zahwa sebagai Lead CI/CD split dari DevOps — sesuai ketentuan RPS untuk tim 5 orang).

> ⚠️ **KRITIS:** Endpoint `/team` masih berisi **data placeholder** ("Nama 1", "NIM1") — tugas Minggu 1 fundamental tidak selesai!
> ⚠️ Achmad Bayhaqi menggunakan **2 akun git** (AchmadLyraa + Achmad Bayhaqi) dengan email yang berbeda tapi mengarah ke akun GitHub yang sama. Commit dihitung gabungan.
> ⚠️ Terdapat subfolder `cc-kelompok-kel6/` di dalam root repo — struktur tidak rapi.

---

## B. Rekap Kontribusi Git (TERVERIFIKASI)

| Anggota | Minggu 1 (W9) | Minggu 2 (W10) | Minggu 3 (W11) | Minggu 4 (W12) | Total Scope |
|---------|:---:|:---:|:---:|:---:|:---:|
| Nilam Ayu NandaStari | 7 | 4 | 5 | 2 | **18** |
| Achmad Bayhaqi (gabungan) | 8+4=12 | 0+4=4 | **0** ⚠️ | 1+2=3 | **19** |
| Alfiani Dwiyuniarti | 5 | 2 | 1 | 1 | **9** |
| Zahwa Hanna Dwi Putri | 2 | 1 | 3 | 2 | **8** |
| Indah Nur Fortuna | 2 | 2 | 1 | 2 | **7** |

> ⚠️ Achmad Bayhaqi tidak ada commit di Minggu 3 (W11).

---

## C. Penilaian Tugas Terstruktur Kelompok

| Minggu | Kriteria Utama | Skor | Catatan |
|--------|---------------|:---:|---------|
| **M1** | README 606 baris ✅, **/team PLACEHOLDER** ⛔ (Nama 1/NIM1), subfolder cc-kelompok-kel6 ada | **60** | Endpoint /team adalah syarat wajib Minggu 1 — tidak dipenuhi |
| **M2** | `main.py` 159 baris (terpendek), CRUD ✅, auth.py ✅ | **88** | CRUD ada tapi main.py lebih ramping dari rata-rata |
| **M3** | 7 komponen React ✅ (+ Toast component) | **89** | Frontend cukup lengkap |
| **M4** | CORS whitelist ✅, .env ✅, JWT ✅ | **86** | Modul 4 fungsional |

**Total Tugas Kelompok: (60+88+89+86)/4 = 80.75 / 100 → B (Memuaskan)**

> Nilai Minggu 1 diberikan 60 karena endpoint `/team` — yang merupakan deliverable utama Minggu 1 — masih berisi placeholder template. Ini adalah kesalahan fatal yang tidak dapat diabaikan.

---

## D. Penilaian Individu — Sikap & Profesionalisme

### 1. Nilam Ayu NandaStari Romdoni (10231070) — Lead QA & Docs
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 18 total) | 30/30 |
| Substansi: README, dokumentasi, testing — konsisten | 34/40 |
| Sesuai peran QA & Docs ✅ | 18/20 |
| Commit message deskriptif | 8/10 |
| **Total** | **90/100 → A** |

### 2. Achmad Bayhaqi (10231001) — Lead Backend
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (⚠️ W11 tidak ada commit — 3 dari 4 minggu aktif, 19 total gabungan) | 22/30 |
| Substansi: backend files, auth, CRUD — kontribusi terbanyak | 35/40 |
| Sesuai peran Backend ✅ | 18/20 |
| ⚠️ 2 akun git berbeda (AchmadLyraa + Achmad Bayhaqi) perlu diseragamkan | 6/10 |
| **Total** | **81/100 → AB** |

### 3. Alfiani Dwiyuniarti (10231010) — Lead DevOps
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 9 total) | 27/30 |
| Substansi: setup, infrastruktur, frontend helper | 28/40 |
| Sesuai peran DevOps: kontribusi infrastruktur ada | 14/20 |
| Commit message cukup | 7/10 |
| **Total** | **76/100 → AB** |

### 4. Zahwa Hanna Dwi Putri (10231092) — Lead CI/CD & Deploy
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 8 total) | 26/30 |
| Substansi: kontribusi cukup merata di semua minggu | 27/40 |
| Sesuai peran CI/CD: belum ada Pipeline (wajar Wk9-11) | 14/20 |
| Commit message cukup | 7/10 |
| **Total** | **74/100 → B** |

### 5. Indah Nur Fortuna (10231044) — Lead Frontend
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 7 total) | 26/30 |
| Substansi: frontend files, components — kontribusi ada | 27/40 |
| Sesuai peran Frontend: ada kontribusi di komponen ✅ | 14/20 |
| Commit message cukup | 7/10 |
| **Total** | **74/100 → B** |

---

## E. Catatan & Rekomendasi

**Yang Sudah Baik ✅**
- Tim 5 orang dengan pembagian peran yang jelas termasuk CI/CD terpisah
- Semua 5 anggota aktif setiap minggu (kecuali Achmad W11)
- README 606 baris, cukup komprehensif
- Backend dan JWT fungsional

**Yang Perlu Diperbaiki ⚠️ (KRITIS)**
1. **WAJIB SEGERA:** Update endpoint `/team` dengan data asli semua anggota — ini deliverable Minggu 1 yang belum selesai!
2. Hapus atau pindahkan subfolder `cc-kelompok-kel6/` yang ada di dalam root repo
3. Achmad: konsolidasikan ke 1 akun git; pastikan tidak ada minggu yang terlewat
4. Main.py yang lebih ramping dibanding kelompok lain — perlu ditambah validasi dan dokumentasi endpoint
