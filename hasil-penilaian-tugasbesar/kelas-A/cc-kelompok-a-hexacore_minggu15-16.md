# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 6: Minggu Kuliah 15–16 (1 – 14 Jun 2026) — Final + UAS

> Lingkup laporan ini: **C17 (Security checklist, kelompok)** dan **C18 (Dokumentasi C4 + Reflection paper, Mix per anggota)**. C19–C22 (Demo URL, Viva, CI/CD demo, Dok final) dinilai dosen. F6 = semua role prime (tanpa baseline floor).

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Repo | cc-kelompok-a-hexacore |
| Project | **LenteraPustaka** — sistem peminjaman buku (Auth Service + Library Service + API Gateway) |

**Anggota:**

| Nama | NIM | Role |
|---|---|---|
| Khanza Nabila Tsabita | 10231049 | Lead DevOps |
| Maulana Malik Ibrahim | 10231051 | Lead Backend |
| Micka Mayulia Utama | 10231053 | Lead Frontend |
| Muhammad Aqila Ardhi | 10231057 | Lead QA & Docs |

---

### A. C17 — Security Checklist & Best Practices (Kelompok)

| Kriteria | Bukti | Nilai |
|---|---|:---:|
| Secrets management | `Chore/cleanup secrets (#53)`, `final polish backend - security` (#54); SECRET_KEY dari env, tidak ada hardcoded | 90 |
| Container hardening | `USER` non-root di `backend/Dockerfile`, `services/auth-service/Dockerfile`, `services/library-service/Dockerfile` | 90 |
| Network & gateway | rate-limit + proxy headers di `services/gateway/nginx.conf`; CORS production diperbaiki (#58) | 88 |
| Input validation | Pydantic validation di 4 file service (auth/library schemas) | 84 |

**Nilai C17: 88** · **Grade: A**

---

### B. C18 — Dokumentasi C4 + Reflection Paper (Mix, per anggota)

**Komponen kelompok (C4 + README):** `docs/architecture.md` (diagram Mermaid topologi + Container/Component terms), `api-contract.md`, `deployment-guide.md`, `docker-architecture.md`, README final lengkap. Base dokumentasi kuat (88).

**Reflection paper per anggota** (`docs/reflection-*.md`): keempat anggota menulis.

| NIM | Nama | Reflection | C18 |
|---|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | `reflection-khanza.md` (33 baris) — sudut DevOps/deployment | **88** |
| 10231051 | Maulana Malik Ibrahim | `reflection-maulana.md` (53 baris) — paling substantif, dekomposisi backend | **90** |
| 10231053 | Micka Mayulia Utama | `reflection-micka.md` (41 baris) — adaptasi frontend ke gateway | **86** |
| 10231057 | Muhammad Aqila Ardhi | `reflection-aqila.md` (31 baris) + dok arsitektur (#31) | **86** |

---

### C. Ringkasan untuk Gradebook

**C17 — Security (4%):** semua anggota **88**

**C18 — Dok C4 + Reflection (6%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | **88** |
| 10231051 | Maulana Malik Ibrahim | **90** |
| 10231053 | Micka Mayulia Utama | **86** |
| 10231057 | Muhammad Aqila Ardhi | **86** |
