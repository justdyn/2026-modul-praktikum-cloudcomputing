# Laporan Penilaian Kelompok sowelcloudspace – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | sowelcloudspace |
| Repo | cc-kelompok-sowelcloudspace |
| Project | **Sowel Task** — to-do list kolaboratif, Auth + Task Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Anjas Geofany Diamare | 10231016 | Lead Backend |
| Arya Wijaya Saroyo | 10231020 | Lead DevOps |
| Cantika Ade Qutnindra Maharani | 10231024 | Lead Frontend |
| Meiske Handayani | 10231052 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Hardening & devops | `Feat/modul 15 security (#97)`, `Feature/final devops hardening (#76)` | 86 |
| Container hardening | `USER` non-root di 3 Dockerfile (`backend`, `auth-service`, `task-service`) | 86 |
| Network & gateway | rate-limit di `backend/main.py` + `services/gateway/nginx.conf`; `update form validation and handle rate limit errors (#98)` | 84 |
| Secrets & CORS | env-based config; CORS 3 service | 82 |

**Nilai C17: 84** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi kuat (82).

**Reflection paper per anggota:** keempat anggota menulis reflection paper di `docs/reflection-paper/<NIM>_*.md`.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231016 | Anjas Geofany Diamare | `docs/reflection-paper/10231016_LeadBackend.md` (~3.2KB) | **82** |
| 10231020 | Arya Wijaya Saroyo | `docs/reflection-paper/10231020_LeadDevOps.md` (~2.2KB) | **80** |
| 10231024 | Cantika Ade Qutnindra Maharani | `docs/reflection-paper/10231024_LeadFrontend.md` (~5.5KB) | **84** |
| 10231052 | Meiske Handayani | `docs/reflection-paper/10231052_LeadQADocs.md` (~4.1KB) | **84** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **84**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231016 | Anjas Geofany Diamare | **82** |
| 10231020 | Arya Wijaya Saroyo | **80** |
| 10231024 | Cantika Ade Qutnindra Maharani | **84** |
| 10231052 | Meiske Handayani | **84** |
