# Laporan Penilaian Kelompok steam – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | steam |
| Repo | cc-kelompok-a-steam |
| Project | **Inti Rupa** — asisten cerdas (summarizer + image generator) (Auth Service + AI Service + API Gateway) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Incha Raghil | 10231043 | Lead Frontend |
| Irfan Zaki Riyanto | 10231045 | Lead Backend |
| Jonathan Cristopher Jetro | 10231047 | Lead DevOps |
| Jonathan Joseph Yudita Tampubolon | 10231048 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Container hardening | `security: jalankan kontainer auth dan ai service sebagai non-root user` (14 Jun); `USER` di 2 Dockerfile service | 86 |
| Input validation | `feat: perkuat input validation di auth-service schemas` (14 Jun); validation di service | 84 |
| Network & gateway | rate-limit di `services/gateway/nginx.conf` + `nginx.dev.conf`; CORS config 3 service | 84 |
| Secrets management | `.env.example` lengkap; tidak ada hardcoded SECRET_KEY | 82 |

**Nilai C17: 84** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (diagram Mermaid), `api-contract.md`, `final-checklist.md` (#56), `reliability-testing.md` (#55), README arsitektur microservices lengkap (revisi besar 14 Jun). Base dokumentasi kuat (80).

**Reflection paper per anggota:** hanya satu reflection paper formal di `docs/reflection/reflection_paper.md` (ditulis Jonathan Joseph, Lead QA & Docs). Anggota lain belum punya reflection terpisah; kontribusi dokumentasi besar oleh Irfan (README + architecture.md, 14 Jun).

| NIM | Nama | Reflection / kontribusi dok | C18 |
|---|---|---|:---:|
| 10231043 | Incha Raghil | tanpa reflection paper; kontribusi frontend docs | **72** |
| 10231045 | Irfan Zaki Riyanto | tanpa reflection paper formal, tapi penyusun utama README + `architecture.md` + `api-contract.md` final | **84** |
| 10231047 | Jonathan Cristopher Jetro | tanpa reflection paper; gateway/Railway docs | **76** |
| 10231048 | Jonathan Joseph Yudita Tampubolon | `reflection_paper.md` (27 baris) + `final-checklist.md` + `architecture.md` | **80** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **84**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231043 | Incha Raghil | **72** |
| 10231045 | Irfan Zaki Riyanto | **84** |
| 10231047 | Jonathan Cristopher Jetro | **76** |
| 10231048 | Jonathan Joseph Yudita Tampubolon | **80** |
