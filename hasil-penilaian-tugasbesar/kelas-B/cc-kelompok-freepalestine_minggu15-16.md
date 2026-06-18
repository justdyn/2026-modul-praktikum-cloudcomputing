# Laporan Penilaian Kelompok freepalestine 🎓 (magang) – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. Nilai masuk **tabel magang terpisah** (NIM tidak di gradebook reguler).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | freepalestine (magang/konversi) |
| Repo | cc-kelompok-freepalestine |
| Project | Aplikasi cloud-native FastAPI + React — Auth + Dashboard Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Ariel Itsbat Nurhaq | 10231018 | Lead Backend & Frontend |
| Muhammad Khoiruddin Marzuq | 10231065 | Lead DevOps |
| Raditya Yudianto | 10231076 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Container hardening | `USER` non-root di 3 Dockerfile (`backend`, `auth-service`, `dashboard-service`) | 84 |
| Network & gateway | rate-limit di `services/gateway/nginx.conf` | 82 |
| Secrets & CORS | env-based config; CORS di backend + auth-service | 80 |
| Input validation | validation di service | 80 |

**Nilai C17: 82** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** README + dokumentasi; `architecture.md` formal tidak ditemukan (dokumentasi arsitektur lebih ringan). Base (75).

**Reflection paper per anggota** (`docs/member-*.md` = reflection paper penuh): ketiga anggota menulis, volume tinggi.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231018 | Ariel Itsbat Nurhaq | `member-ariel.md` (118 baris) — paling komprehensif | **84** |
| 10231065 | Muhammad Khoiruddin Marzuq | `member-irud.md` (64 baris) — DevOps | **78** |
| 10231076 | Raditya Yudianto | `member-radit.md` (74 baris) — QA & Docs | **80** |

---

### C. Ringkasan untuk Gradebook (Tabel Magang)

**C17 — Security (4%):** semua anggota **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231018 | Ariel Itsbat Nurhaq | **84** |
| 10231065 | Muhammad Khoiruddin Marzuq | **78** |
| 10231076 | Raditya Yudianto | **80** |
