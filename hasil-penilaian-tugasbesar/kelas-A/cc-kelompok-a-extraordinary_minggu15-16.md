# Laporan Penilaian Kelompok extraordinary – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | extraordinary |
| Repo | cc-kelompok-a-extraordinary (branch `master`) |
| Project | **Temuin** — sistem lost & found kampus (Auth + Item + Engagement Service) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Nicholas Christian Samuel Manurung | 10231069 | Lead Frontend |
| Pangeran Borneo Silaen | 10231073 | Lead DevOps |
| Raisha Alika Irwandira | 10231077 | Lead Backend |
| Rani Ayu Dewi | 10231079 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | secrets via env; `Sprint 8 Backend - Security Hardening & Cleanup (#119)` | 88 |
| Container hardening | `USER` non-root di **5 Dockerfile** (backend, frontend, auth, engagement, item-service) — paling lengkap | 92 |
| Network & gateway | rate-limit di `gateway/nginx.conf`; CD safety + image hardening (DO-8.1) | 88 |
| Input validation | validation di 7 file service | 86 |

**Nilai C17: 88** · **Grade: A**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** README + UAS roadmap (#126), `api-contract.md`, `deployment-guide.md`, `docker-guide.md`, 8 sprint QA report (`sprint-0X-qa-report.md`), `final-checklist.md`. Base dokumentasi kuat (80).

**Reflection paper per anggota** (`docs/reflections/`): keempat anggota menulis.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231069 | Nicholas Christian Samuel Manurung | `reflection-frontend-nicholas.md` (77 baris) | **82** |
| 10231073 | Pangeran Borneo Silaen | `reflection-devops-pangeran.md` (68 baris) | **82** |
| 10231077 | Raisha Alika Irwandira | `reflection-backend-raisha.md` (78 baris) | **82** |
| 10231079 | Rani Ayu Dewi | `reflection-qa-rani.md` (63 baris) + finalisasi README/UAS roadmap | **84** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **88**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231069 | Nicholas Christian Samuel Manurung | **82** |
| 10231073 | Pangeran Borneo Silaen | **82** |
| 10231077 | Raisha Alika Irwandira | **82** |
| 10231079 | Rani Ayu Dewi | **84** |
