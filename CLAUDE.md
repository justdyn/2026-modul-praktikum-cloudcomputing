# Konteks Project — Komputasi Awan SI2514027

Proyek ini berisi materi praktikum + sistem penilaian tugas besar untuk MK Komputasi Awan, ITK. **Kelas A** (12 kelompok) dan **Kelas B** (11 kelompok).

## Struktur Direktori Penting

- `[01-15]-modul.md` — modul praktikum per minggu (RPS)
- `student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-<nama>/` — repo kelas A (hasil `gh classroom clone -a 952202`, double-nest sudah dirapikan jadi 1 level)
- `student-repos/kelas-B/cc-kelompok-submissions/cc-kelompok-<nama>/` — repo kelas B (hasil `gh classroom clone -a 941045`). **Perhatikan:** path = `cc-kelompok-submissions` (bukan `cc-kelompok-b-submissions`), nama kelompok **tanpa** prefix `b-`.
- `hasil-penilaian/` — penilaian Fase 1 **versi modul lama** (jangan diubah, hanya rujukan)
- `hasil-penilaian-tugasbesar/kelas-A/` & `hasil-penilaian-tugasbesar/kelas-B/` — penilaian **tugas besar** (output utama)
  - `README.md` — master tabel rekap mahasiswa × 22 kolom + Adj + Total Adj
  - `cc-kelompok-[a-]<nama>_minggu1-4.md` — laporan F1 per kelompok
  - `cc-kelompok-[a-]<nama>_minggu5-7.md` — laporan F2
  - `cc-kelompok-[a-]<nama>_minggu9-11.md` — laporan F4
  - `nilai_kelas__SI2514027_2026-05-15.xlsx` — template gradebook (jangan diedit tanpa instruksi user)

## Mapping Fase → Modul → Kolom Gradebook

22 kolom, total bobot 100%. Detail di README masing-masing kelas section "Pemetaan Kolom Gradebook".

| Fase | Modul | Periode | Kolom Gradebook |
|---|---|---|---|
| **F1** | M1-4 Foundation | 24 Feb – 22 Mar 2026 | C01 Kuis (5%, manual), C02 Tugas kelompok (5%), C03 Git individu (5%) |
| **F2** | M5-7 Containerization | 23 Mar – 12 Apr 2026 | C04 Kuis (4%, manual), C05 Tugas kelompok (4%), C06 Git individu (4%) |
| **M8** | UTS | 13 – 19 Apr 2026 | C07–C10 (terisi di xlsx oleh dosen) |
| **F4** | M9-11 CI/CD | 20 Apr – 10 Mei 2026 | C11 Kuis (3%, manual), C12 Tugas kelompok (3%), C13 Git+PR individu (3%) |
| **F5** | M12-14 Microservices | ~11 Mei – 31 Mei 2026 (estimasi) | C14 Kuis (3%, manual), C15 Tugas ADR kelompok (3%), C16 Git+Arch individu (3%) |
| **F6** | M15-16 Final+UAS | ~1 Jun – 14 Jun 2026 (estimasi) | C17 Security (4%), C18 Dok C4 (6%), C19 Demo URL (6%), C20 Viva (7%, manual), C21 CI/CD demo (4%), C22 Dok final (8%) |

## Metodologi Penilaian (penting!)

**Sumber data:** semua dari GitHub repo (`git log`, file inspection, PR history) + xlsx Anda untuk UTS.

**Rubrik individu (C03/C06/C13):** Konsistensi 30% + Substansi 40% + Kesesuaian Peran 20% + Kualitas Pesan 10%.

**Baseline Floor 70 (role-aware):** untuk anggota dengan role off-phase yang masih punya kontribusi minimal (skor mentah ≥ 50), nilai dinaikkan ke 70. Anggota prime-time tetap dinilai ketat tanpa floor; absen total (skor < 50) tetap tanpa floor.

**Pemetaan prime time:**
- **F1**: Backend, Frontend, QA & Docs → prime. DevOps, Container, CI/CD, Deploy → off.
- **F2**: DevOps, Container, CI/CD, Deploy, Backend → prime. Frontend, QA & Docs → off.
- **F4**: CI/CD, DevOps, Deploy, QA & Docs → prime. Backend, Frontend → off.
- **F5 (M12-14 Microservices)**: Backend, DevOps, Container → prime. Frontend, QA & Docs → off (mereka tetap dukung tapi bukan rana utama).
- **F6 (M15-16 Final+UAS)**: SEMUA prime — fase akhir semua role harus deliver (security audit, docs C4, deployment, viva).

**Kolom Adjustment (Adj):** kosong di tabel master, diisi dosen manual ±10 poin berdasarkan observasi kelas yang tidak terlihat di repo (presentasi, diskusi, kontribusi non-commit).

## Aturan Penting

1. **Kolom kuis (C01/C04/C11/C14) dan viva (C08/C20) selalu kosong** — dosen isi manual saat sesi kelas.
2. **xlsx tidak boleh diedit** tanpa instruksi eksplisit user. README.md adalah single source of truth.
3. **Tidak ada nilai tanpa bukti dari repo** — setiap angka tertelusur ke commit log atau file inspection.
4. **Gaya tulisan to-the-point**: tidak ada framing "anti-halusinasi", "konteks tugas besar", "kolom diisi manual", referensi "Opsi A/B/C", atau legenda meta. Tulis hasilnya langsung.
5. **Output Section D laporan**: dua sub-tabel terpisah (skor kelompok + skor individu urut NIM). Angka bulat integer.
6. **Magang/konversi** dinilai dengan rubrik sama, tapi disajikan di **tabel terpisah** di README karena NIM tidak ada di gradebook xlsx reguler.

## Workflow Grading

Untuk menilai kelompok baru, gunakan skill `/nilai-kelompok <nama-kelompok>` atau ikuti [.claude/skills/nilai-kelompok/SKILL.md](.claude/skills/nilai-kelompok/SKILL.md).

## Status Pengisian (per 2026-06-04)

> ⚠️ **Selalu refresh clone sebelum menilai** (`git fetch` + `reset --hard origin/<default>`; extraordinary pakai `master`). Snapshot kelas A lama (15 Mei) stale — F5 student push belum masuk. Kelas B clone (per 4 Jun) sudah fresh.
>
> **F5 lengkap untuk kelas A (12) dan kelas B (11).** Kelas A: 9/12 dekomposisi microservices nyata; nexa modular-monolith; awit kode tak ter-wire; nyawit & team-agile gagal/abandoned. Kelas B: 10/11 dekomposisi nyata; kel6 = sama anggota hexagroup (F5 dari hexagroup). Sisa: F6.

> **F6 kelas A = 🔶**: C17 (Security) & C18 (Dok C4 + Reflection) sudah dinilai (clone fresh 18 Jun). C19–C22 diisi dosen. C15/C16 (F5) diverifikasi tetap. **Kelas A & B reguler F6 LENGKAP (C17–C22)** — C19–C22 dari `UAS - Kelas [A/B] Form Penilaian.xlsx`. Hanya mahasiswa magang (kelas A: nyawit/pria-solo/team-agile; kelas B: freepalestine/Salsabila/Rayhan) yang baru C17/C18 (tidak tercakup form UAS). Catatan: 5 typo NIM di form kelas B sudah dikoreksi via nama→gradebook.

### Kelas A — Reguler (9 kelompok, 40 mhs di xlsx termasuk 1 luar kelas)
| Kelompok | F1 | F2 | F4 | F5 | F6 |
|---|:---:|:---:|:---:|:---:|:---:|
| hexacore | ✅ | ✅ | ✅ | ✅ | ✅ |
| antek-antek-asing | ✅ | ✅ | ✅ | ✅ | ✅ |
| awit | ✅ | ✅ | ✅ | ✅ | ✅ |
| ethereal | ✅ | ✅ | ✅ | ✅ | ✅ |
| extraordinary | ✅ | ✅ | ✅ | ✅ | ✅ |
| miracle | ✅ | ✅ | ✅ | ✅ | ✅ |
| nexa | ✅ | ✅ | ✅ | ✅ | ✅ |
| steam | ✅ | ✅ | ✅ | ✅ | ✅ |
| suksesss | ✅ | ✅ | ✅ | ✅ | ✅ |

### Kelas A — Magang/konversi (3 kelompok, tabel terpisah di README, NIM tidak di xlsx)
| Kelompok | F1 | F2 | F4 | F5 | F6 |
|---|:---:|:---:|:---:|:---:|:---:|
| nyawit 🎓 | ✅ | ✅ | ✅ | ✅ | 🔶 |
| pria-solo 🎓 | ✅ | ✅ | ✅ | ✅ | 🔶 |
| team-agile 🎓 | ✅ | ✅ | ✅ | ✅ | 🔶 |

### Kelas B (36 mhs reguler di xlsx)
| Kelompok | F1 | F2 | F4 | F5 | F6 | Catatan |
|---|:---:|:---:|:---:|:---:|:---:|---|
| bismillah_a | ✅ | ✅ | ✅ | ✅ | ✅ | Salsabila magang (di tabel magang) |
| ccc_clan | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| freepalestine 🎓 | ✅ | ✅ | ✅ | ✅ | 🔶 | semua magang |
| harahetta-2 | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| hexagroup | ✅ | ✅ | ✅ | ✅ | ✅ | **5 anggota sama dengan kel6** — primary repo F2+F4 |
| ignite | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| kel6 | ✅ | ✅ | ✅ | ✅ | ✅ | **5 anggota sama dengan hexagroup** — primary repo F1 |
| nyawit_1 | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| sowelcloudspace | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| stranger_things | ✅ | ✅ | ✅ | ✅ | ✅ | reguler |
| taskete_7 | ✅ | ✅ | ✅ | ✅ | ✅ | Rayhan magang (di tabel magang) |

## Catatan Khusus untuk Future Work (F5 + F6)

### F5 (M12-14 Microservices)
- Periode commit: ~minggu 12-14 kalender 2026 (estimasi 11 Mei – 31 Mei)
- Deliverable kelompok: Architecture Decision Record (ADR), pemecahan monolith jadi microservices, inter-service communication, API gateway
- Skor C15 (kelompok) dari: jumlah service terpisah, ADR document quality, gateway config, service-to-service auth, observability per service
- Skor C16 (individu) dari: git log + architecture diagram contribution (siapa nyusun diagram, siapa implementasi service)
- Kuis C14 = manual dosen

### F6 (M15-16 Final + UAS)
- Periode commit: ~minggu 15-16 kalender 2026 (estimasi 1 Jun – 14 Jun)
- Deliverable: security audit + best practices (C17), dokumentasi C4 diagram + reflection paper (C18), production URL accessible (C19), demo CI/CD push→deploy (C21), reflection paper individual (C22)
- Viva C20 = manual dosen saat UAS
- Untuk C18 & C22 yang "Mix" (kelompok+individu), ada bagian kelompok (C4 diagram, README) dan bagian individu (reflection paper masing-masing)

### Workflow F5/F6 (sama dengan F1-F4)
1. Investigasi repo: cari `services/` folder, `gateway/`, `docker-compose.microservices.yml`, `docs/adr-*.md`, `docs/c4-*.md`, `reflection-<nama>.md`
2. Hitung commit per anggota per minggu di window F5/F6
3. Aplikasikan rubrik 4-komponen + baseline floor 70 untuk off-phase
4. Generate file `cc-kelompok-[a-]<nama>_minggu12-14.md` (F5) dan `cc-kelompok-[a-]<nama>_minggu15-16.md` (F6)
5. Update tabel master kelas-A/B README — kolom C14-C16 (F5) dan C17-C22 (F6)
6. Update CLAUDE.md status table
