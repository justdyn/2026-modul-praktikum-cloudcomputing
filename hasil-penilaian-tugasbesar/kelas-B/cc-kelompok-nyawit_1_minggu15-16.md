# Laporan Penilaian Kelompok nyawit_1 – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit_1 |
| Repo | cc-kelompok-nyawit_1 |
| Project | Sistem procurement — Auth + Procurement Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Andi Adam Firdaus | 10211014 | Lead DevOps |
| Ahmad Baihaqi | 10221063 | Lead DevOps |
| Az-Zahra Atikah Nurhaliza | 10231022 | Lead QA & Docs |
| Muchlis Wahyu Saputra | 10231054 | Lead Backend |
| Ranaya Chintya Mahitsa | 10231078 | Lead Frontend |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Input validation | validation di **13 file** service (terbanyak di kelas B) | 80 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 74 |
| Secrets & CORS | env-based config (`core/config.py`); CORS di `app/main.py` | 74 |
| Network & gateway | **rate limiting tidak ditemukan** | 66 |

**Nilai C17: 74** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture/`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota** (`docs/members/member-[*].md` berisi reflection/kontribusi substantif): kelima anggota menulis.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10211014 | Andi Adam Firdaus | `member-[adam].md` (52 baris) — DevOps | **80** |
| 10221063 | Ahmad Baihaqi | `member-[ahmad-baihaqi].md` (54 baris) — DevOps | **80** |
| 10231022 | Az-Zahra Atikah Nurhaliza | `member-[Zahra].md` (46 baris) — QA & Docs | **80** |
| 10231054 | Muchlis Wahyu Saputra | `member-[Muchlis].md` (113 baris) — paling komprehensif, Backend | **86** |
| 10231078 | Ranaya Chintya Mahitsa | `member-[Ranaya].md` (42 baris) — Frontend | **78** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **74**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10211014 | Andi Adam Firdaus | **80** |
| 10221063 | Ahmad Baihaqi | **80** |
| 10231022 | Az-Zahra Atikah Nurhaliza | **80** |
| 10231054 | Muchlis Wahyu Saputra | **86** |
| 10231078 | Ranaya Chintya Mahitsa | **78** |
