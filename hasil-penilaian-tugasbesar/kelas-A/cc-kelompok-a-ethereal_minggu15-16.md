# Laporan Penilaian Kelompok ethereal – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ethereal |
| Repo | cc-kelompok-a-ethereal |
| Project | **Kelarin** — platform manajemen tugas akademik (Auth Service + Task Service + API Gateway) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Alsha Dwi Cahya | 10231011 | Lead Container |
| Amazia Devid Saputra | 10231013 | Lead Frontend |
| Andini Permata Sari | 10231015 | Lead QA & Docs |
| Ansellma Tita Pakartiwuri Putri | 10231017 | Lead Deploy & CI/CD |
| Tiya Mitra Ayu | 10231088 | Lead Backend |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | DATABASE_URL via env (railway); tidak ada hardcoded SECRET_KEY | 74 |
| Container hardening | `USER` non-root hanya di `backend/Dockerfile`, belum merata ke service | 70 |
| Network & gateway | CORS production fix (#84); **tidak ditemukan rate limiting** di nginx/gateway | 68 |
| Audit security | fokus F6 pada perbaikan gateway/Railway 502/CORS — tanpa commit hardening security eksplisit | 66 |

**Nilai C17: 70** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (Container/Component terms), `CI_CD_GUIDE.md`, `deployment-guide.md`, `operations-guide.md` (#76), `reliability-testing.md`. Base dokumentasi kuat (84).

**Reflection paper per anggota:** hanya Ansellma menulis reflection paper lengkap (`docs/member-ANSEL.md`, 68 baris, format Reflection Paper formal). Anggota lain hanya placeholder member doc (1 baris).

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | placeholder member doc | **72** |
| 10231013 | Amazia Devid Saputra | placeholder member doc | **70** |
| 10231015 | Andini Permata Sari | placeholder member doc (kontribusi dok operations/architecture) | **72** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | `member-ANSEL.md` (68 baris) — reflection paper formal, sudut CI/CD & Deploy | **88** |
| 10231088 | Tiya Mitra Ayu | placeholder member doc (kontribusi observability backend) | **73** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **70**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231011 | Alsha Dwi Cahya | **72** |
| 10231013 | Amazia Devid Saputra | **70** |
| 10231015 | Andini Permata Sari | **72** |
| 10231017 | Ansellma Tita Pakartiwuri Putri | **88** |
| 10231088 | Tiya Mitra Ayu | **73** |
