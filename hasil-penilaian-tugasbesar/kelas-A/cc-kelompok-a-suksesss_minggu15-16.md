# Laporan Penilaian Kelompok suksesss – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | suksesss |
| Repo | cc-kelompok-a-suksesss |
| Project | **SafeSpace** — layanan bimbingan konseling (Auth Service + Item Service) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Rendy Rifandy Kurnia | 10231081 | Lead Backend |
| Riska Fadlun Khairiyah Purba | 10231083 | Lead Frontend |
| Rizki Abdul Aziz | 10231085 | Lead DevOps |
| Siti Nur Azizah Putri Awni | 10231087 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | env-based config; backend secret/database url eksplisit (compose override); tidak ada hardcoded SECRET_KEY | 76 |
| Network & gateway | `integrate nginx reverse proxy and configure cors origins (#46)`; **rate limiting tidak ditemukan** | 70 |
| Container hardening | `USER` non-root di `backend/Dockerfile`; belum merata ke service | 72 |
| Input validation | validation di 5 file | 76 |

**Nilai C17: 74** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` + `arsitektur-sistem.md` (Container/Component terms), `database-schema.md`, `api-contract.md`, `final-checklist.md`, `reliability-testing.md`. Base dokumentasi kuat (80).

**Reflection paper per anggota** (`docs/reflection-paper/<NIM>_<role>.md`): keempat anggota menulis.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231081 | Rendy Rifandy Kurnia | `10231081_LeadBackend.md` (92 baris) — paling substantif | **86** |
| 10231083 | Riska Fadlun Khairiyah Purba | `10231083_Frontend.md` (24 baris) — paling ringkas | **76** |
| 10231085 | Rizki Abdul Aziz | `10231085-LeadDevOps.md` (32 baris) | **78** |
| 10231087 | Siti Nur Azizah Putri Awni | `10231087-LeadQADocs.md` (51 baris) + dok arsitektur/reliability | **82** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **74**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231081 | Rendy Rifandy Kurnia | **86** |
| 10231083 | Riska Fadlun Khairiyah Purba | **76** |
| 10231085 | Rizki Abdul Aziz | **78** |
| 10231087 | Siti Nur Azizah Putri Awni | **82** |
