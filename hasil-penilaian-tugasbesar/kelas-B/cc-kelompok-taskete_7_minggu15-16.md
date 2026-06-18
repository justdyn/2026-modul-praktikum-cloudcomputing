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

**Reflection paper per anggota:** **tidak ada reflection paper** — `docs/member-*.md` hanya placeholder (≤138B). Nilai C18 dari komponen dokumentasi kelompok saja.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231012 | Amalia Tiara Rezfani | tanpa reflection; QA & Docs (kontributor F6 terbanyak, dokumentasi) | **74** |
| 10231046 | Irwan Maulana | tanpa reflection; Frontend | **72** |
| 10231072 | Noviansyah | tanpa reflection; Backend | **72** |
| 10231080 | Rayhan Iqbal 🎓 | tanpa reflection; DevOps | **72** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231012 | Amalia Tiara Rezfani | **74** |
| 10231046 | Irwan Maulana | **72** |
| 10231072 | Noviansyah | **72** |
| 10231080 | Rayhan Iqbal 🎓 (magang) | **72** |
