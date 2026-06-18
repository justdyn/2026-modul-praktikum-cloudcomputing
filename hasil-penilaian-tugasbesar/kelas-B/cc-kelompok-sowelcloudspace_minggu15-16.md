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

**Reflection paper per anggota:** **tidak ada reflection paper** — `docs/member-*.md` hanya placeholder (≤154B). Nilai C18 dari komponen dokumentasi kelompok saja.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231016 | Anjas Geofany Diamare | tanpa reflection; Backend | **74** |
| 10231020 | Arya Wijaya Saroyo | tanpa reflection; DevOps | **74** |
| 10231024 | Cantika Ade Qutnindra Maharani | tanpa reflection; kontributor F6 terbanyak (frontend) | **76** |
| 10231052 | Meiske Handayani | tanpa reflection; QA & Docs (kontribusi dokumentasi) | **76** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **84**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231016 | Anjas Geofany Diamare | **74** |
| 10231020 | Arya Wijaya Saroyo | **74** |
| 10231024 | Cantika Ade Qutnindra Maharani | **76** |
| 10231052 | Meiske Handayani | **76** |
