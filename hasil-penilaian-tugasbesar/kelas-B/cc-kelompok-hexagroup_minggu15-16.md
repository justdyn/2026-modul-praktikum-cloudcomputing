# Laporan Penilaian Kelompok hexagroup – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).
> **hexagroup = anggota identik dengan kel6**; kerja F6 ada di repo hexagroup (62 commit F6; repo kel6 berhenti April). Nilai berlaku untuk kelima anggota.

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexagroup (≡ kel6) |
| Repo | cc-kelompok-hexagroup (primary F6) |
| Project | Sistem administrasi surat & keuangan — Auth + Finance + Letters Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Achmad Bayhaqi | 10231001 | Lead Backend |
| Alfiani Dwiyuniarti | 10231010 | Lead DevOps |
| Indah Nur Fortuna | 10231044 | Lead Frontend |
| Nilam Ayu NandaStari Romdoni | 10231070 | Lead QA & Docs |
| Zahwa Hanna Dwi Putri | 10231092 | Lead CI/CD & Deploy |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Audit & rate limiting | `feat(security): add rate limiting gateway, secret audit, reflection paper` (#109/#111/#113); rate-limit `services/gateway/nginx.conf` | 86 |
| Secrets management | secret audit; env-based config | 84 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 80 |
| Input validation & CORS | validation di service; CORS backend + auth + finance-service | 82 |

**Nilai C17: 84** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi kuat (82).

**Reflection paper per anggota** (`docs/reflection-paper/<NIM>_<role>.md`): 4 dari 5 menulis reflection penuh; Achmad Bayhaqi hanya placeholder (35B).

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231001 | Achmad Bayhaqi | placeholder (35B) — tanpa reflection | **72** |
| 10231010 | Alfiani Dwiyuniarti | `10231010-LeadDevops.md` (~6.6KB) | **86** |
| 10231044 | Indah Nur Fortuna | `10231044-LeadFrontend.md` (~5.3KB) + kontributor F6 terbanyak | **86** |
| 10231070 | Nilam Ayu NandaStari Romdoni | `10231070-LeadQA&Docs.md` (~4.4KB) | **84** |
| 10231092 | Zahwa Hanna Dwi Putri | `10231092_LeadCICD&Deploy.md` (~8.7KB) — paling komprehensif | **88** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **84**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231001 | Achmad Bayhaqi | **72** |
| 10231010 | Alfiani Dwiyuniarti | **86** |
| 10231044 | Indah Nur Fortuna | **86** |
| 10231070 | Nilam Ayu NandaStari Romdoni | **84** |
| 10231092 | Zahwa Hanna Dwi Putri | **88** |
