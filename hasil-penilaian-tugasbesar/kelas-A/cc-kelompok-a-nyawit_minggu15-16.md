# Laporan Penilaian Kelompok nyawit 🎓 (magang) – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 dinilai dosen. F6 = semua role prime (tanpa baseline floor). Nilai masuk **tabel magang terpisah** (NIM tidak di gradebook reguler).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nyawit (magang/konversi) |
| Repo | cc-kelompok-a-nyawit |
| Project | **Sistem Manajemen Aset IT** — pengelolaan infrastruktur hardware perusahaan |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Ilham Ahmad Fahriji | 10231042 | Lead Backend & DevOps |
| Putu Ngurah Semara | 10231075 | Lead Frontend & QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Audit security | `tools/audit_checklist.py` (skrip audit security otomatis) + `backend/app/core/security.py`; commit `feat: Security hardening, docs, and tooling` | 90 |
| Network & gateway | rate-limit di `nginx.conf` (+ test `test_nginx_config.py`); CORS config | 82 |
| Input validation | validation di 6 file | 80 |
| Container hardening | **tidak ada `USER` non-root** di Dockerfile | 68 |

**Nilai C17: 82** · **Grade: AB**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/api-contract.md`, `deployment-guide.md`, `uas-presentation-outline.md`, `release-notes-m3.md`, README. **Tidak ada `architecture.md`/diagram C4 formal** — dokumentasi arsitektur lebih lemah dibanding kelompok reguler. Base dokumentasi (65).

**Reflection paper per anggota:** **tidak ditemukan reflection paper** untuk kedua anggota.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231042 | Ilham Ahmad Fahriji | tanpa reflection paper; kontribusi dominan (security/docs/CI/CD) | **66** |
| 10231075 | Putu Ngurah Semara | tanpa reflection paper; kontribusi README + security | **64** |

---

### C. Ringkasan untuk Gradebook (Tabel Magang)

**C17 — Security (4%):** semua anggota **82**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231042 | Ilham Ahmad Fahriji | **66** |
| 10231075 | Putu Ngurah Semara | **64** |
