# Laporan Penilaian Kelompok taskete_7 – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | taskete_7 |
| Repo | cc-kelompok-taskete_7 |
| Project | **Sistem Manajemen SDM Cuti Karyawan** — Auth + Item Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Amalia Tiara Rezfani | 10231012 | Lead QA & Docs |
| Irwan Maulana | 10231046 | Lead Frontend |
| Noviansyah | 10231072 | Lead Backend |
| Rayhan Iqbal 🎓 | 10231080 | Lead DevOps (magang) |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Audit & validation | `feat: implement security best practices and input validation` (PR #48 feature/secret-audit) | 84 |
| Network & gateway | rate-limit di `services/gateway/nginx.conf` | 82 |
| Container hardening | `USER` non-root di `backend/Dockerfile` | 80 |
| Secrets & CORS | secret audit; CORS backend + auth + item-service | 82 |

**Nilai C17: 82** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota:** keempat anggota menulis reflection paper di `docs/reflection-paper/<NIM>_*.md` (5.6–11.8KB).

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231012 | Amalia Tiara Rezfani | `docs/reflection-paper/10231012-LeadQAandDocs.md` (~5.6KB) | **82** |
| 10231046 | Irwan Maulana | `docs/reflection-paper/10231046-LeadFrontend.md` (~8.9KB) | **84** |
| 10231072 | Noviansyah | `docs/reflection-paper/10231072-LeadBackend.md` (~11.8KB) | **86** |
| 10231080 | Rayhan Iqbal 🎓 | `docs/reflection-paper/10231080-LeadDevOpsandCICD.md` (~9.9KB) | **84** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231012 | Amalia Tiara Rezfani | **82** |
| 10231046 | Irwan Maulana | **84** |
| 10231072 | Noviansyah | **86** |
| 10231080 | Rayhan Iqbal 🎓 (magang) | **84** |
