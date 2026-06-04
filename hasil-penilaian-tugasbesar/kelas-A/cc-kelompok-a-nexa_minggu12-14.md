# Laporan Penilaian Kelompok nexa – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | nexa |
| Repo | cc-kelompok-a-nexa |
| Project | **Studyfy** — Learning Management System (LMS) berbasis cloud |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Dhiya Afifah | 10231031 | Lead Frontend | off-phase |
| Dzaky Rasyiq Zuhair | 10231035 | Lead Backend | ✅ prime |
| Gabriel Karmen Sanggalangi | 10231039 | Lead QA & Docs | off-phase |
| Ika Agustin Wulandari | 10231041 | Lead DevOps | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **72** | `docs/architecture.md` (757 baris): sangat lengkap — 3 diagram Mermaid, daftar service, kontrak API, panduan debug per service. **Tapi** secara eksplisit menyatakan pakai *"arsitektur **modular monolith** dengan domain service separation di dalam satu aplikasi backend"* — bukan dekomposisi microservices. Dok di-commit 3 Jun (#30), window F6. |
| **M13 – Implementasi microservices** | 33% | **35** | Tidak ada folder `services/`, tidak ada gateway, tidak ada inter-service comm. `docker-compose.yml` tetap monolith (`db`/`backend`/`frontend`). Boundary hanya di dalam satu aplikasi — tidak ada service yang deployable terpisah. |
| **M14 – Architecture diagram + monitoring** | 34% | **52** | Diagram arsitektur ada di dokumen, tapi tidak ada implementasi/monitoring per service karena tidak ada microservices. |

**Nilai Kelompok: (72 + 35 + 52) / 3 = 53.00 → 53**
**Grade Kelompok: BC**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Dhiya = `Dhiya`; Dzaky = `dzaky`/`Dzaky`/`Sourremon`; Gabriel = `Gabriel Karmen`; Ika = `Ika`.
>
> Dokumentasi arsitektur (#30, Gabriel) di-commit 3 Jun → masuk window F6, tidak dihitung di F5.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Dhiya Afifah | Dhiya | 0 | 3 | 0 | **3** |
| Dzaky Rasyiq Zuhair | dzaky / Sourremon | 0 | 2 | 0 | **2** |
| Gabriel Karmen Sanggalangi | Gabriel Karmen | 0 | 0 | 0 | **0** |
| Ika Agustin Wulandari | Ika | 0 | 0 | 0 | **0** |

---

### C. Penilaian Individual

#### 1. Dzaky Rasyiq Zuhair (Lead Backend — prime)
- Konsistensi 45 · Substansi 68 · Peran 78 · Pesan 72
- 2 commit, 1/3 minggu, refactor domain backend (modular monolith).

**Nilai: 64** · **Grade: BC** (prime, tanpa floor)

#### 2. Dhiya Afifah (Lead Frontend — off-phase)
- Konsistensi 50 · Substansi 65 · Peran 70 · Pesan 72
- 3 commit, 1/3 minggu.

**Nilai mentah: 62** → off-phase + raw ≥ 50 → **baseline floor 70**
**Nilai gradebook: 70** · **Grade: B**

#### 3. Gabriel Karmen Sanggalangi (Lead QA & Docs — off-phase)
- **0 commit** di window F5 (dokumentasi arsitektur #30 di-commit 3 Jun → dihitung di F6).

**Nilai: 28** · **Grade: E** (absen di window F5, raw < 50 → tanpa floor)

#### 4. Ika Agustin Wulandari (Lead DevOps — prime)
- **0 commit** di window F5 — absen di fase microservices padahal role DevOps prime.

**Nilai: 25** · **Grade: E** (absen total, tanpa floor)

> 📌 Kontribusi dokumentasi arsitektur utama Gabriel (#30) jatuh 3 Jun (window F6) — akan terhitung saat penilaian F6.

---

### D. Ringkasan untuk Gradebook

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** semua anggota **53**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231031 | Dhiya Afifah | **70** |
| 10231035 | Dzaky Rasyiq Zuhair | **64** |
| 10231039 | Gabriel Karmen Sanggalangi | **28** |
| 10231041 | Ika Agustin Wulandari | **25** |
