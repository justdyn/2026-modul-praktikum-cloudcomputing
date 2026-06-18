# Laporan Penilaian Kelompok awit – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | awit |
| Repo | cc-kelompok-a-awit |
| Project | **PalmTrack Cloud (PalmChain)** — monitoring pengangkutan TBS kelapa sawit |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Adam Ibnu Ramadhan | 10231003 | Lead Backend |
| Adhyasta Firdaus | 10231005 | Lead CI/CD & Deployment |
| Adonia Azarya Tamalonggehe | 10231007 | Lead QA & Documentation |
| Alfian Fadillah Putra | 10231009 | Lead Frontend |
| Varrel Kaleb Ropard Pasaribu | 10231089 | Lead DevOps & Container |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | env-based config (Supabase DATABASE_URL via env); tidak ada hardcoded SECRET_KEY | 78 |
| Hardening | `chore: final polish — security hardening, gateway networks, and cleanup (#50)` oleh Varrel | 76 |
| Network & gateway | rate-limit di `backend/main.py`; CORS di backend + auth/item-service; nginx proxy routes | 74 |
| Container | **tidak ada `USER` non-root** di Dockerfile service | 68 |

**Nilai C17: 75** · **Grade: B**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture/architecture.md`, `CHANGELOG.md` (#53), dokumentasi observability (#51). Base dokumentasi memadai (78).

**Reflection paper per anggota:** hanya 1 anggota menulis reflection paper formal. Adam & Adonia punya laporan kontribusi (`docs/members/member-*.md`); Adhyasta & Varrel hanya placeholder.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | log kontribusi `member-[Adam...].md` (46 baris), tanpa reflection paper | **70** |
| 10231005 | Adhyasta Firdaus | placeholder (1 baris) | **66** |
| 10231007 | Adonia Azarya Tamalonggehe | log kontribusi `member-[Adonia...].md` (43 baris) | **70** |
| 10231009 | Alfian Fadillah Putra | `Reflection - [Alfian Fadillah Putra].md` (25 baris) — satu-satunya reflection formal | **80** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | placeholder (1 baris) | **66** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **75**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231003 | Adam Ibnu Ramadhan | **70** |
| 10231005 | Adhyasta Firdaus | **66** |
| 10231007 | Adonia Azarya Tamalonggehe | **70** |
| 10231009 | Alfian Fadillah Putra | **80** |
| 10231089 | Varrel Kaleb Ropard Pasaribu | **66** |
