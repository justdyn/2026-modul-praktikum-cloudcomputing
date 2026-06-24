# Laporan Penilaian Kelompok stranger_things – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | stranger_things |
| Repo | cc-kelompok-stranger_things |
| Project | Sistem manajemen jadwal imunisasi — Auth + Item Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Ahmad Daffa Alfattah | 10231008 | Lead Backend |
| Cintya Widhi Astuti | 10231026 | Lead DevOps |
| Nazwa Amelia Zahra | 10231068 | Lead Frontend |
| Verina Rahma Dinah | 10231090 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Hardening | `chore: final polish — security, docs, UAS preparation (#62)` | 82 |
| Network & gateway | rate-limit di `services/gateway/nginx.conf` | 82 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 78 |
| Input validation & CORS | validation di service; CORS backend + auth + item-service | 78 |

**Nilai C17: 80** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota:** keempat anggota menulis reflection paper di `docs/reflection paper/<NIM>_*.md`.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231008 | Ahmad Daffa Alfattah | `docs/reflection paper/10231008_LeadBackend.md` | **82** |
| 10231026 | Cintya Widhi Astuti | `docs/reflection paper/10231026_LeadDevOps.md` | **82** |
| 10231068 | Nazwa Amelia Zahra | `docs/reflection paper/10231068_LeadFrontend.md` | **82** |
| 10231090 | Verina Rahma Dinah | `docs/reflection paper/10231090_LeadQADocs.md` | **84** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **80**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231008 | Ahmad Daffa Alfattah | **82** |
| 10231026 | Cintya Widhi Astuti | **82** |
| 10231068 | Nazwa Amelia Zahra | **82** |
| 10231090 | Verina Rahma Dinah | **84** |
