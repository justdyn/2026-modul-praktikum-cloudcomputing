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

**Reflection paper per anggota:** keempat anggota menulis reflection paper di folder `docs/reflection/` (per-NIM `10231043_Frontend.md`, `10231045_Backend.md`, `10231047_DevOps.md`, + `reflection_paper.md`).

| NIM | Nama | Reflection / kontribusi dok | C18 |
|---|---|---|:---:|
| 10231043 | Incha Raghil | `docs/reflection/10231043_Frontend.md` (~2.9KB) | **80** |
| 10231045 | Irfan Zaki Riyanto | `docs/reflection/10231045_Backend.md` (~4.2KB) + penyusun README/architecture | **84** |
| 10231047 | Jonathan Cristopher Jetro | `docs/reflection/10231047_DevOps.md` (~3KB) | **80** |
| 10231048 | Jonathan Joseph Yudita Tampubolon | `docs/reflection/reflection_paper.md` (~6KB) + `final-checklist.md` | **80** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **84**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231043 | Incha Raghil | **80** |
| 10231045 | Irfan Zaki Riyanto | **84** |
| 10231047 | Jonathan Cristopher Jetro | **80** |
| 10231048 | Jonathan Joseph Yudita Tampubolon | **80** |
