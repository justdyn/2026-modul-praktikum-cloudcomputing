# Laporan Penilaian Kelompok miracle – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | miracle |
| Repo | cc-kelompok-a-miracle |
| Project | **Donor Manajemen** — sistem manajemen pendonor darah (Auth + Item Service + API Gateway) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Avhilla Catton Andalucia | 10231021 | Lead Container |
| Betran | 10231023 | Lead QA & Docs |
| Chelsy Olivia | 10231025 | Lead CI/CD & Deploy |
| Debora Intania Subekti | 10231029 | Lead Backend |
| Yosan Pratiwi | 10231091 | Lead Frontend |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | env-based config; tidak ada hardcoded SECRET_KEY | 80 |
| Network & gateway | `fix nginx.conf for duplicate, rate limiting, and upstream (#83)`; rate-limit di `nginx.conf`, `docker-compose.yml`, `backend/main.py` | 82 |
| Container hardening | `USER` non-root di `backend/Dockerfile`; belum merata ke seluruh service | 76 |
| Input validation | validation di service + CORS config | 80 |

**Nilai C17: 80** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (Container/Component terms), `database-schema.md`, ERD diagram, `api-contract.md` final (#77), `final-checklist.md` (#79), README baru (#84). Base dokumentasi kuat (82).

**Reflection paper per anggota** (`docs/member-*.md` — berisi *Refleksi Teknis & Analitis* lengkap, bukan sekadar log): kelima anggota menulis.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | `member-Avhilla.md` (67 baris) | **84** |
| 10231023 | Betran | `member-BETRAN.md` (57 baris) + README & docs final | **84** |
| 10231025 | Chelsy Olivia | `member-Chelsy.md` (49 baris) — CI/CD | **82** |
| 10231029 | Debora Intania Subekti | `member-intan.md` (57 baris) — refleksi backend/database-per-service paling kuat | **86** |
| 10231091 | Yosan Pratiwi | `member-YOSAN.md` (57 baris) — frontend/status page | **82** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **80**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231021 | Avhilla Catton Andalucia | **84** |
| 10231023 | Betran | **84** |
| 10231025 | Chelsy Olivia | **82** |
| 10231029 | Debora Intania Subekti | **86** |
| 10231091 | Yosan Pratiwi | **82** |
