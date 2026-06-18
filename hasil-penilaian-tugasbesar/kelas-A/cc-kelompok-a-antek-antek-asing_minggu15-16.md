# Laporan Penilaian Kelompok antek-antek-asing – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | antek-antek-asing |
| Repo | cc-kelompok-a-antek-antek-asing |
| Project | **Antick Async** — helpdesk internal manajemen tiket (Auth + Item Service + API Gateway) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Muhammad Athala Romero | 10231059 | Lead Backend |
| Muhammad Bagas Setiawan | 10231061 | Lead Frontend |
| Muhammad Fikri Haikal Ariadma | 10231063 | Lead DevOps |
| Nanda Aulia Putri | 10231067 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | `chore(security): move secrets to environment variables`; tidak ada SECRET_KEY hardcoded | 92 |
| Container hardening | `USER` non-root di 3 Dockerfile (`backend`, `auth-service`, `item-service`) | 90 |
| Network & gateway | `feat(gateway): add rate limiting and abuse protection`; rate-limit `services/gateway/nginx.conf`; CORS production fix (#24) | 92 |
| Audit & validation | `chore(devops): security audit fixes` (#28); `feat(security): strengthen validation and authentication rules`; validation di 7 file | 90 |

**Nilai C17: 90** · **Grade: A**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (Container/Component terms), `api-contract.md`, `deployment-guide.md`, `docker-architecture.md`, `operations-guide.md` (#30). Base dokumentasi kuat (85).

**Reflection paper per anggota** (`docs/*_reflectionpaper.md`): keempat anggota menulis, volume tinggi.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231059 | Muhammad Athala Romero | `athala_reflectionpaper.md` (135 baris) — backend & observability | **88** |
| 10231061 | Muhammad Bagas Setiawan | `bagas_reflectionpaper.md` (64 baris) — frontend, paling ringkas | **83** |
| 10231063 | Muhammad Fikri Haikal Ariadma | `fikri_reflectionpaper.md` (162 baris) — DevOps/security | **88** |
| 10231067 | Nanda Aulia Putri | `nanda_reflectionpaper.md` (274 baris) — paling komprehensif, QA & reliability | **90** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **90**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231059 | Muhammad Athala Romero | **88** |
| 10231061 | Muhammad Bagas Setiawan | **83** |
| 10231063 | Muhammad Fikri Haikal Ariadma | **88** |
| 10231067 | Nanda Aulia Putri | **90** |
