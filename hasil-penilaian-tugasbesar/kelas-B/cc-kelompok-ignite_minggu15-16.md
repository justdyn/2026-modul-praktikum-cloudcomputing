# Laporan Penilaian Kelompok ignite – Kelas B
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup: **C17 (Security, kelompok)** & **C18 (Dok C4 + Reflection, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | ignite |
| Repo | cc-kelompok-ignite |
| Project | **E-commerce / Inventory** — katalog produk + statistik inventori, Auth + Item Service + API Gateway |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Andini Permata Dewanti | 10231014 | Lead Backend |
| Desnita Dwi Putri | 10231030 | Lead Frontend |
| Krishandy Dhanysa Pratama | 10231050 | Lead DevOps |
| Putri Rahmawati | 10231074 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Container hardening | `USER` non-root di `backend/Dockerfile` | 70 |
| Input validation & CORS | validation di 4 file; CORS backend + auth + item-service | 70 |
| Secrets management | env-based config; tidak ada hardcoded SECRET_KEY | 70 |
| Network & gateway | **rate limiting tidak ditemukan**; tanpa commit security hardening eksplisit di F6 | 62 |

**Nilai C17: 68** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md`, README. Base dokumentasi memadai (80).

**Reflection paper per anggota:** **tidak ada reflection paper** — `docs/member-*.md` hanya placeholder (≤154B, sebatas header nama/role). Nilai C18 dari komponen dokumentasi kelompok saja.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231014 | Andini Permata Dewanti | tanpa reflection; Backend (kontribusi arch doc) | **74** |
| 10231030 | Desnita Dwi Putri | tanpa reflection | **72** |
| 10231050 | Krishandy Dhanysa Pratama | tanpa reflection | **72** |
| 10231074 | Putri Rahmawati | tanpa reflection; QA & Docs (kontributor F6 terbanyak, dokumentasi) | **76** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **68**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231014 | Andini Permata Dewanti | **74** |
| 10231030 | Desnita Dwi Putri | **72** |
| 10231050 | Krishandy Dhanysa Pratama | **72** |
| 10231074 | Putri Rahmawati | **76** |
