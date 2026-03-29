# Laporan Penilaian Tugas Terstruktur — Minggu 1-4
**Kelompok:** cc-kelompok-ignite
**Tanggal Penilaian:** 29 Maret 2026

---

## A. Identitas Kelompok

| Nama | NIM | Peran |
|------|-----|-------|
| Andini Permata Dewanti | 10231014 | Lead Backend |
| Putri Rahmawati | 10231074 | Lead Frontend |
| Desnita Dwi Putri | 10231030 | Lead DevOps |
| Krishandy Dhanysa Pratama | 10231050 | Lead QA & Docs |

> ⚠️ Endpoint `/team` masih menggunakan nama tim `"cloud-team-XX"` (placeholder template belum diubah).

---

## B. Rekap Kontribusi Git (TERVERIFIKASI)

| Anggota | Minggu 1 | Minggu 2 | Minggu 3 | Minggu 4 | Total Scope |
|---------|:---:|:---:|:---:|:---:|:---:|
| Desnita Dwi Putri | 4 | 7 | 3 | 5 | **19** |
| Andini Permata Dewanti | 5 | 4 | 3 | 6 | **18** |
| Krishandy Dhanysa Pratama | 3 | 1 | 1 | 1 | **6** |
| Putri Rahmawati | 2 | 0* | 0* | 0* | **2** |

> **Catatan Putri Rahmawati (10231074):** Mahasiswa menyampaikan bahwa laptopnya rusak selama periode ini:
> - **Minggu 2** → commit dilakukan dari laptop Lead QA & Docs (Krishandy)
> - **Minggu 3** → commit dilakukan dari laptop Lead Backend (Andini)
>
> **Bukti yang mendukung klaim (dari analisis git):**
> - Commit Andini tanggal 10 Mar (`feat: add React CRUD frontend with component architecture`) menambahkan 7 file frontend sekaligus — padahal Andini adalah Lead Backend. Sangat tidak lazim seorang Lead Backend commit seluruh komponen React.
> - Putri sendiri sudah menunjukkan kemampuan frontend sejak Minggu 1 (`feat: add React frontend with API integration`, 14 file, 24 Feb).
>
> **Status: ⏳ NILAI DALAM REVIEW — menunggu konfirmasi dosen**

---

## C. Penilaian Tugas Terstruktur Kelompok

| Minggu | Kriteria Utama | Skor | Catatan |
|--------|---------------|:---:|---------|
| **M1** | README **3320 baris** (terpanjang di antara semua kelompok!) ✅, /team nama tim masih "cloud-team-XX" | **85** | README luar biasa detailnya. Nilai dikurangi karena placeholder nama tim |
| **M2** | `main.py` 180 baris, CRUD ✅, auth.py ✅ | **91** | Backend solid dan konsisten |
| **M3** | 6 komponen React ✅, CRUD UI lengkap, 9 docs files | **90** | setup.sh tersedia — nilai tambah |
| **M4** | CORS whitelist ✅, .env ✅, JWT ✅ | **89** | Modul 4 selesai dengan baik |

**Total Tugas Kelompok: (85+91+90+89)/4 = 88.75 / 100 → A (Luar Biasa)**

---

## D. Penilaian Individu — Sikap & Profesionalisme

### 1. Desnita Dwi Putri (10231030) — Lead DevOps
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 19 total — distribusi sangat merata: 4/7/3/5) | 30/30 |
| Substansi: kontribusi substansial di semua area | 36/40 |
| Sesuai peran DevOps: aktif di infrastruktur, setup, dokumentasi | 19/20 |
| Commit message deskriptif | 8/10 |
| **Total** | **93/100 → A** |

### 2. Andini Permata Dewanti (10231014) — Lead Backend
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 18 total — distribusi baik: 5/4/3/6) | 30/30 |
| Substansi: backend files, auth, CRUD ✅ — catatan: commit Mar 10 berisi frontend components (kemungkinan milik Putri) | 33/40 |
| Sesuai peran Backend ✅ | 18/20 |
| Commit message deskriptif | 8/10 |
| **Total** | **89/100 → AB** |
> Catatan: Commit `feat: add React CRUD frontend with component architecture` (Mar 10) kemungkinan merupakan kontribusi Putri yang di-commit dari laptop Andini. Jika terkonfirmasi, kredit komponen tersebut berpindah ke Putri dan nilai Andini tetap tinggi berdasarkan backend work yang substansial.

### 3. Krishandy Dhanysa Pratama (10231050) — Lead QA & Docs
| Kriteria | Skor |
|----------|:---:|
| Konsistensi (commit setiap minggu ✅, 6 total — distribusi: 3/1/1/1) | 25/30 |
| Substansi: dokumentasi, testing screenshots | 27/40 |
| Sesuai peran QA & Docs ✅ | 15/20 |
| Commit message cukup | 7/10 |
| **Total** | **74/100 → B** |
> Aktif setiap minggu tapi kontribusi per minggu sangat rendah (1 commit per minggu di Minggu 2-4).

### 4. Putri Rahmawati (10231074) — Lead Frontend
> ⏳ **NILAI DALAM REVIEW — belum final**

**Nilai berdasarkan git saat ini (sebelum klarifikasi):**
| Kriteria | Skor |
|----------|:---:|
| Commit atas nama sendiri: 2 commit (Minggu 1 saja) | 5/30 |
| Substansi terverifikasi: scaffold Vite React (Feb 24) | 10/40 |
| Sesuai peran Frontend: setup awal ada, komponen tidak terverifikasi atas namanya | 5/20 |
| Commit message: minimal | 3/10 |
| **Total sementara** | **23/100 → E** |

**Estimasi nilai jika klaim TERKONFIRMASI:**
| Skenario | Estimasi Skor | Keterangan |
|----------|:-------------:|-----------|
| Klaim terbukti penuh (Minggu 2+3 via laptop orang lain) | **72–78 → B** | Konsistensi tetap dikurangi karena tidak gunakan akun sendiri |
| Klaim terbukti sebagian (Minggu 3 saja) | **55–65 → BC–B** | Minggu 2 masih kosong |

**Langkah verifikasi yang disarankan:**
1. Tanyakan Putri detail isi kode frontend yang dia tulis (viva/interview singkat)
2. Minta screenshot riwayat edit file di laptop pinjaman (VSCode recent files)
3. Cek apakah Putri bisa menjelaskan logika komponen React di repo (Header, ItemCard, ItemForm, dll)

---

## E. Catatan & Rekomendasi

**Yang Sudah Baik ✅**
- README 3320 baris — dokumentasi terbaik di antara semua kelompok
- Desnita dan Andini: distribusi commit sangat merata dan konsisten — contoh yang sangat baik
- Backend, frontend, dan JWT semuanya fungsional
- setup.sh tersedia

**Yang Perlu Ditindaklanjuti ⚠️**
1. **PENDING REVIEW:** Konfirmasi klaim Putri Rahmawati soal laptop rusak — lihat langkah verifikasi di bagian D.4
2. **Kebijakan ke depan:** Jika laptop pinjaman, mahasiswa harus set `git config user.email "NIM@student.itk.ac.id"` sebelum commit agar tetap tercatat atas namanya sendiri
3. Ganti nama tim `"cloud-team-XX"` di endpoint `/team` dengan nama kelompok yang sesungguhnya
4. Krishandy: tingkatkan kontribusi per minggu — 1 commit/minggu terlalu sedikit untuk Lead QA & Docs
