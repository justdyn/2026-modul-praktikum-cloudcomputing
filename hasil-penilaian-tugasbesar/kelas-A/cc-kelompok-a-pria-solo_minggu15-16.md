# Laporan Penilaian Kelompok pria-solo 🎓 (magang) – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor). Nilai masuk **tabel magang terpisah** (NIM tidak di gradebook reguler).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | pria-solo (magang/konversi) |
| Repo | cc-kelompok-a-pria-solo |
| Project | **Document Validator** — REST API validasi dokumen (OCR + ground truth), konteks magang Telkom Regional IV Kaltim |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Dyno Fadillah Ramadhani | 10231033 | Solo (Backend + Frontend + DevOps + QA) |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Container hardening | `USER` non-root di `backend/Dockerfile` + `frontend/Dockerfile` | 84 |
| Network & gateway | rate-limit di `services/gateway/nginx.conf` + `advance_review_service.py`; CORS config | 82 |
| Input validation | validation di 8 file (paling banyak) | 84 |
| Secrets management | env-based config; PHP upload/timeout limits via Docker config | 80 |

**Nilai C17: 82** · **Grade: AB**

> Catatan: dikerjakan solo dengan cakupan production (Laravel + service gateway) — security coverage tetap baik meski satu orang.

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (Container/Component terms), `docker-architecture.md`, `database-schema.md` + diagram, `api-documentation.md`, `final-checklist.md`, `viva-prep.md`, `uas-presentation-outline.md`. Base dokumentasi kuat untuk solo (80).

**Reflection paper:** `docs/reflection-dyno-fadillah-ramadhani.md` (95 baris) — lengkap.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231033 | Dyno Fadillah Ramadhani | `reflection-dyno-fadillah-ramadhani.md` (95 baris) | **84** |

---

### C. Ringkasan untuk Gradebook (Tabel Magang)

**C17 — Security (4%):** **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231033 | Dyno Fadillah Ramadhani | **84** |
