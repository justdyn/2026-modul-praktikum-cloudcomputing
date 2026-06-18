# Laporan Penilaian Kelompok harahetta-2 – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | harahetta-2 |
| Repo | cc-kelompok-harahetta-2 |
| Project | **Sewain** — platform rental, Auth + Item Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Achmad Zaki Zaidan | 10231002 | Backend |
| Djaky Abbyyu Fauzan Timumum | 10231032 | Frontend/Support |
| Muhammad Alif Setiawan | 10231056 | DevOps/Backend |
| Riqqah Khalda Karina | 10231082 | QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Input validation | validation di **11 file** service (paling banyak di kelas B) | 82 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 74 |
| Secrets & CORS | env-based config; CORS di backend + auth + chat-service | 76 |
| Network & gateway | **rate limiting tidak ditemukan** | 68 |

**Nilai C17: 76** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota** (`docs/reflection-*.md`): keempat anggota menulis, volume tinggi.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231002 | Achmad Zaki Zaidan | `reflection-Zaki.md` (204 baris) — paling komprehensif | **86** |
| 10231032 | Djaky Abbyyu Fauzan Timumum | `reflection-Djaky.md` (140 baris) | **84** |
| 10231056 | Muhammad Alif Setiawan | `reflection-Alif.md` (101 baris) — DevOps | **84** |
| 10231082 | Riqqah Khalda Karina | `reflection-paper-Riqqah.md` (48 baris) | **80** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **76**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231002 | Achmad Zaki Zaidan | **86** |
| 10231032 | Djaky Abbyyu Fauzan Timumum | **84** |
| 10231056 | Muhammad Alif Setiawan | **84** |
| 10231082 | Riqqah Khalda Karina | **80** |
