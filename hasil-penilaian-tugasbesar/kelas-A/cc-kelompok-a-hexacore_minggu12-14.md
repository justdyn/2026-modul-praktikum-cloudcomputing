# Laporan Penilaian Kelompok hexacore – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | hexacore |
| Repo | cc-kelompok-a-hexacore |
| Project | **LenteraPustaka** — sistem peminjaman buku, didekomposisi dari monolith menjadi Auth Service + Library Service + API Gateway |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Khanza Nabila Tsabita | 10231049 | Lead DevOps | ✅ prime |
| Maulana Malik Ibrahim | 10231051 | Lead Backend | ✅ prime |
| Micka Mayulia Utama | 10231053 | Lead Frontend | off-phase |
| Muhammad Aqila Ardhi | 10231057 | Lead QA & Docs | off-phase |

---

### A. Penilaian Kelompok – Microservices

> 3 kriteria @ ~33%.

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **88** | `docs/architecture.md` komprehensif: diagram Mermaid topologi, alokasi 6 container + port, **API contract** per service, batas domain jelas (Auth domain vs Library domain) dengan **database terisolasi per service** (`auth_db` :5433, `item_db` :5434). Rationale dekomposisi tertulis. Minus: bukan format ADR formal (tidak ada section Context/Decision/Consequences/Alternatives), lebih ke spesifikasi arsitektur. Dokumen di-commit 2 Jun (#31), sedikit lewat window F5 (final push). |
| **M13 – Implementasi microservices** | 33% | **94** | Dekomposisi penuh ke **2 service FastAPI + 1 API Gateway**: `services/auth-service`, `services/library-service`, `services/gateway` (nginx). Gateway `services/gateway/nginx.conf` routing lengkap (`/auth`,`/users`,`/verify` → auth; `/books`,`/categories`,`/transactions`,`/fines`,`/upload` → library; `/` → frontend) dengan proxy headers. **Inter-service comm** via `services/library-service/auth_client.py` (httpx async, retry 3x + exponential backoff, timeout 5s, panggil `/verify` ke auth-service). `docker-compose.yml`: 6 container (gateway, frontend, 2 service, 2 DB) + healthcheck + depends_on. Inti dekomposisi (#26) in-window 23 Mei. |
| **M14 – Architecture diagram + monitoring** | 34% | **90** | Diagram Mermaid di `docs/architecture.md`. **Observability**: `metrics.py` (MetricsCollector thread-safe — request/error count, latency p-samples), `logging_middleware.py` (structured logging + correlation_id), `circuit_breaker.py` (state CLOSED/OPEN/HALF_OPEN, fail-fast, cooldown 30s) di library-service. Healthcheck per service di compose. Minus: commit monitoring/observability final (#38) + arch doc (#31) landed 2–4 Jun (early-June final push), sedikit lewat window. |

**Nilai Kelompok: (88 + 94 + 90) / 3 = 90.67 → 91**
**Grade Kelompok: A**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> W12 = 11–17 Mei, W13 = 18–24 Mei, W14 = 25–31 Mei.
>
> **Alias:** Khanza = `x3naline` (email `nabilacaca.101099@gmail.com`); Micka = `mickamayulia`; Aqila = `mightyqila13`; Maulana commit dengan nama asli (email `10231051@student.itk.ac.id`). Semua dikonsolidasi.
>
> **W12 kosong untuk seluruh tim** — sprint microservices baru jalan W13 (commit pertama 19 Mei).

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Khanza Nabila Tsabita | x3naline | 0 | 5 | 1 | **6** |
| Maulana Malik Ibrahim | Maulana Malik Ibrahim | 0 | 3 | 1 | **4** |
| Micka Mayulia Utama | mickamayulia | 0 | 2 | 0 | **2** |
| Muhammad Aqila Ardhi | mightyqila13 | 0 | 1 | 0 | **1** |

> Catatan: dokumentasi arsitektur (#31, Aqila) di-commit 2 Jun → masuk window F6, tidak dihitung di F5. Monitoring/observability final (#38, Maulana) juga 4 Jun → window F6.

---

### C. Penilaian Individual

#### 1. Khanza Nabila Tsabita (Lead DevOps — prime)
- **Konsistensi (30%):** 2/3 minggu aktif (W12 kosong seluruh tim) → 70
- **Substansi (40%):** 6 commit, deliverable DevOps inti: CD pipeline auto-deploy Railway (#19), gateway sync + service healthchecks + Makefile microservices (#28), compose resilience (#32), perbaikan production API URL (#21,#23) → 92
- **Kesesuaian Peran (20%):** 100% commit DevOps/gateway/compose — sangat sesuai role prime F5 → 96
- **Kualitas Pesan (10%):** conventional commits (`feat(devops):`, `fix(devops):`, `chore:`) deskriptif → 90

**Nilai: (0.30×70 + 0.40×92 + 0.20×96 + 0.10×90) = 21 + 36.8 + 19.2 + 9.0 = 86.0 → 86**
**Grade: A**

#### 2. Maulana Malik Ibrahim (Lead Backend — prime)
- **Konsistensi (30%):** 2/3 minggu aktif → 70
- **Substansi (40%):** 4 commit, paling crusial: **dekomposisi monolith → Auth + Item Service (#26)**, centralized env-based config (#24), items/fines stats endpoints + unit test di library-service (#29), reliability patterns / circuit breaker (#30) → 94
- **Kesesuaian Peran (20%):** Backend prime, 100% commit di domain service → 96
- **Kualitas Pesan (10%):** conventional, scoped (`feat(backend):`) deskriptif → 92

**Nilai: (0.30×70 + 0.40×94 + 0.20×96 + 0.10×92) = 21 + 37.6 + 19.2 + 9.2 = 87.0 → 87**
**Grade: A**

#### 3. Micka Mayulia Utama (Lead Frontend — off-phase)
- **Konsistensi (30%):** 1/3 minggu aktif (hanya W13) → 50
- **Substansi (40%):** 2 commit, integrasi frontend ke gateway + handle 503/504 microservice downtime (#27), optimasi frontend production → 72
- **Kesesuaian Peran (20%):** Frontend off-phase, tapi kontribusi relevan (adaptasi frontend ke API gateway) → 76
- **Kualitas Pesan (10%):** sebagian conventional, satu commit non-conventional (`feat: optimasi frontend untuk production`) → 80

**Nilai mentah: (0.30×50 + 0.40×72 + 0.20×76 + 0.10×80) = 15 + 28.8 + 15.2 + 8.0 = 67.0 → 67**
**Off-phase + raw ≥ 50 → baseline floor 70.**
**Nilai gradebook: 70** · **Grade: B**

#### 4. Muhammad Aqila Ardhi (Lead QA & Docs — off-phase)
- **Konsistensi (30%):** 1/3 minggu aktif (hanya W13) → 50
- **Substansi (40%):** 1 commit in-window (Docs/milestone2 release, #25). Dokumentasi arsitektur microservices + API contract (#31) di-commit 2 Jun → dihitung di F6, bukan F5 → 56
- **Kesesuaian Peran (20%):** QA & Docs off-phase, kontribusi docs relevan → 70
- **Kualitas Pesan (10%):** deskriptif → 76

**Nilai mentah: (0.30×50 + 0.40×56 + 0.20×70 + 0.10×76) = 15 + 22.4 + 14.0 + 7.6 = 59.0 → 59**
**Off-phase + raw ≥ 50 → baseline floor 70.**
**Nilai gradebook: 70** · **Grade: B**

> 📌 Kontribusi dokumentasi arsitektur utama Aqila (#31) jatuh 2 Jun (window F6) — akan terhitung saat penilaian F6. Floor 70 melindungi role off-phase yang tetap punya kontribusi in-window.

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis identifikasi service boundaries (3%):** kosong (diisi dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **91**

**C16 — Kontribusi mingguan + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231049 | Khanza Nabila Tsabita | **86** |
| 10231051 | Maulana Malik Ibrahim | **87** |
| 10231053 | Micka Mayulia Utama | **70** |
| 10231057 | Muhammad Aqila Ardhi | **70** |
