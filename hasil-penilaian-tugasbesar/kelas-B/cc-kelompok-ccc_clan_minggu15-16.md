# Laporan Penilaian Kelompok ccc_clan – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ccc_clan |
| Repo | cc-kelompok-ccc_clan |
| Project | **SIPILIH** — Sistem Informasi Pemilihan Digital (e-voting), Auth + Candidate Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Ade Ayu Kholifah Putri | 10231004 | Lead QA & Docs |
| Dzakwan Fatih Fadhilah | 10231034 | Lead Backend |
| Muhammad Dani | 10231062 | Lead DevOps |
| Risky Nur Fatimah Bahar | 10231084 | Lead Frontend |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Audit & validation | `feat: add rate limiting and request validation` (PR #48 feature/security-audit) | 84 |
| Network & gateway | rate-limit di `backend/services/gateway/nginx.conf` | 82 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 80 |
| Secrets & CORS | env-based config; CORS di backend | 80 |

**Nilai C17: 82** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota:** **tidak ada reflection paper** — file `docs/member-*.md` hanya placeholder (≤154B). Nilai C18 dari komponen dokumentasi kelompok saja.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231004 | Ade Ayu Kholifah Putri | tanpa reflection; QA & Docs (kontribusi dokumentasi kelompok) | **72** |
| 10231034 | Dzakwan Fatih Fadhilah | tanpa reflection | **72** |
| 10231062 | Muhammad Dani | tanpa reflection | **72** |
| 10231084 | Risky Nur Fatimah Bahar | tanpa reflection | **70** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231004 | Ade Ayu Kholifah Putri | **72** |
| 10231034 | Dzakwan Fatih Fadhilah | **72** |
| 10231062 | Muhammad Dani | **72** |
| 10231084 | Risky Nur Fatimah Bahar | **70** |
