# Laporan Penilaian Kelompok pria-solo (magang) – Kelas A
## Fase 5: Minggu Kuliah 12–14 (11 – 31 Mei 2026) — Microservices

---

### Informasi Kelompok

| Field | Detail |
|---|---|
| Nama Kelompok | pria-solo 🎓 (magang/konversi, solo) |
| Repo | cc-kelompok-a-pria-solo |
| Project | **Document Validator** — REST API validasi dokumen (OCR + ground truth), konteks magang Telkom Regional IV Kaltim |
| Fase | M12 (ADR + service boundaries) → M13 (implementasi microservices) → M14 (architecture diagram + monitoring) |

**Anggota:**

| Nama | NIM | Role | F5 prime? |
|---|---|---|---|
| Dyno Fadillah Ramadhani | 10231033 | Solo (Backend + Frontend + DevOps + QA) | ✅ prime |

---

### A. Penilaian Kelompok – Microservices

| Kriteria | Bobot | Nilai | Catatan |
|---|---|---|---|
| **M12 – ADR + service boundaries** | 33% | **68** | `docs/architecture.md` (99 baris) mendokumentasikan topologi gateway + service. Ringkas tapi ada. |
| **M13 – Implementasi microservices** | 33% | **62** | `services/gateway/nginx.conf` sebagai API gateway. `docker-compose.yml`: `gateway` + `document-service` (backend) + `frontend` + `db`. Gateway di depan satu backend service — dekomposisi minimal (belum dipecah ke beberapa domain service terpisah). Konteks solo + magang. |
| **M14 – Architecture diagram + monitoring** | 34% | **55** | Diagram ringkas di dokumen. Tidak ada metrics/monitoring per service. |

**Nilai Kelompok: (68 + 62 + 55) / 3 = 61.67 → 62**
**Grade Kelompok: BC**

---

### B. Distribusi Kontribusi Individual (git log W12–W14)

> **Alias:** Dyno = `justdyn`/`Dyno Fadillah Ramadhani`.

| Nama | Git Name | W12 | W13 | W14 | Total |
|---|---|:---:|:---:|:---:|:---:|
| Dyno Fadillah Ramadhani | justdyn / Dyno Fadillah Ramadhani | 0 | 8 | 4 | **12** |

---

### C. Penilaian Individual

#### 1. Dyno Fadillah Ramadhani (Solo — prime)
- Konsistensi 75 · Substansi 78 · Peran 85 · Pesan 78
- 12 commit, 2/3 minggu (W12 kosong), solo mengerjakan gateway + arsitektur + compose. Beban penuh satu orang.

**Nilai: 79** · **Grade: AB**

---

### D. Ringkasan untuk Gradebook (tabel magang)

**C14 — Kuis (3%):** kosong (dosen manual).

**C15 — Tugas ADR + microservices (3%):** **62**

**C16 — Kontribusi + architecture diagram (3%):**

| NIM | Nama | Skor |
|---|---|:---:|
| 10231033 | Dyno Fadillah Ramadhani | **79** |
