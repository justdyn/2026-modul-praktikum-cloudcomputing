# Laporan Penilaian Kelompok bismillah_a – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | bismillah_a |
| Repo | cc-kelompok-bismillah_a |
| Project | **Sistem Pelaporan Perundungan Kampus ITK** — Auth + Report Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Aditya Laksamana P Butar Butar | 10231006 | Lead Backend |
| Firni Fauziah Ramadhini | 10231038 | Lead Frontend |
| Muhammad Novri Aziztra | 10231066 | Lead DevOps |
| Salsabila Putri Zahrani 🎓 | 10231086 | Lead QA & Docs (magang) |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Container hardening | `USER` non-root di 3 Dockerfile (`backend`, `auth-service`, `report-service`) | 80 |
| Secrets management | env-based config; tidak ada hardcoded SECRET_KEY | 76 |
| Input validation | validation di service + CORS config (backend + auth-service) | 74 |
| Network & gateway | **rate limiting tidak ditemukan**; tanpa commit security hardening eksplisit di F6 | 66 |

**Nilai C17: 74** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota** (`docs/member-*.md` berisi Reflection Paper, encoding UTF-16): keempat anggota menulis (volume bervariasi).

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231006 | Aditya Laksamana P Butar Butar | reflection penuh (~6.5KB) — backend/microservices, troubleshooting Pydantic & Nginx | **84** |
| 10231038 | Firni Fauziah Ramadhini | reflection singkat (~1.5KB) | **76** |
| 10231066 | Muhammad Novri Aziztra | reflection penuh (~4KB) — DevOps | **82** |
| 10231086 | Salsabila Putri Zahrani 🎓 | reflection penuh (~4KB) — QA & Docs | **82** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **74**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231006 | Aditya Laksamana P Butar Butar | **84** |
| 10231038 | Firni Fauziah Ramadhini | **76** |
| 10231066 | Muhammad Novri Aziztra | **82** |
| 10231086 | Salsabila Putri Zahrani 🎓 (magang) | **82** |
