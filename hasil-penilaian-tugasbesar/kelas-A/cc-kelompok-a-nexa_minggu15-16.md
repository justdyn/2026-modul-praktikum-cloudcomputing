# Laporan Penilaian Kelompok nexa – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nexa |
| Repo | cc-kelompok-a-nexa |
| Project | **Studyfy** — Learning Management System (LMS) berbasis cloud |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Dhiya Afifah | 10231031 | Lead Frontend |
| Dzaky Rasyiq Zuhair | 10231035 | Lead Backend |
| Gabriel Karmen Sanggalangi | 10231039 | Lead QA & Docs |
| Ika Agustin Wulandari | 10231041 | Lead DevOps |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | env-based config; tidak ada hardcoded SECRET_KEY | 70 |
| Container hardening | `USER` non-root hanya di `backend/Dockerfile` | 68 |
| Network & gateway | CORS config (#27); **tidak ditemukan rate limiting** di nginx/gateway | 62 |
| Audit security | tidak ada commit/dok security hardening eksplisit di F6 | 62 |

**Nilai C17: 66** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (Container/Component terms, #30), `operations-guide.md`, `reliability-testing.md`, `deployment-guide.md`. Base dokumentasi memadai (80).

**Reflection paper per anggota** (`docs/reflection-paper/`): keempat anggota menulis (volume bervariasi).

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231031 | Dhiya Afifah | `reflection-dhiya.md` (20 baris) — paling ringkas | **74** |
| 10231035 | Dzaky Rasyiq Zuhair | `reflection-dzaky.md` (50 baris) — backend/microservices | **82** |
| 10231039 | Gabriel Karmen Sanggalangi | `reflection-gabriel.md` (50 baris) + ops/reliability docs (#) | **84** |
| 10231041 | Ika Agustin Wulandari | `reflection-wulan.md` (28 baris) — DevOps/compose cluster | **78** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **66**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231031 | Dhiya Afifah | **74** |
| 10231035 | Dzaky Rasyiq Zuhair | **82** |
| 10231039 | Gabriel Karmen Sanggalangi | **84** |
| 10231041 | Ika Agustin Wulandari | **78** |
