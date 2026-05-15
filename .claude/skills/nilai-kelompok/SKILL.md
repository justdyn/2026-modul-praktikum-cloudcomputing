---
name: nilai-kelompok
description: Menilai 1 kelompok tugas besar MK Komputasi Awan dengan rubrik Foundation (M1-4) + Containerization (M5-7) + CI/CD (M9-11). Investigasi repo kelompok, hitung commit per minggu per anggota, generate 3 file laporan markdown, dan update tabel master di README.md. Trigger saat user minta menilai kelompok tugas besar dengan input nama kelompok (mis. "/nilai-kelompok hexacore").
---

# Skill: Nilai Kelompok Tugas Besar — Komputasi Awan SI2514027

## Tujuan

Menghasilkan **3 file laporan markdown** + **update tabel master di README** untuk 1 kelompok kelas A, dengan rubrik 3 fase:

- **F1 (M1-4)** Foundation — README, /team, backend CRUD, frontend, auth+CORS+env
- **F2 (M5-7)** Containerization — Dockerfile, docker-compose, optimasi
- **F4 (M9-11)** CI/CD — Git workflow + PR, GitHub Actions YAML, tests + badge

> M8 (UTS) dinilai dosen manual — skip. F5 (M12-14) dan F6 (M15-16) akan ada skill terpisah saat diperlukan.

## Input

Nama kelompok (tanpa prefix `cc-kelompok-a-`). Contoh: `hexacore`, `antek-antek-asing`, `awit`, dst.

## Konteks

Sebelum mulai, baca **CLAUDE.md** di root project untuk peta direktori, mapping kolom gradebook (C01–C22), dan aturan penilaian.

Path repo kelompok:
```
student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-submissions/cc-kelompok-a-<nama>/
```

Path output:
```
hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-<nama>_minggu1-4.md
hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-<nama>_minggu5-7.md
hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-<nama>_minggu9-11.md
hasil-penilaian-tugasbesar/kelas-A/README.md  ← update tabel
```

## Periode Tanggal (kalender 2026)

| Fase | Tanggal | W |
|---|---|---|
| F1 W1 | 24 Feb – 1 Mar | Mg 1 |
| F1 W2 | 2 – 8 Mar | Mg 2 |
| F1 W3 | 9 – 15 Mar | Mg 3 |
| F1 W4 | 16 – 22 Mar | Mg 4 |
| F2 W5 | 23 – 29 Mar | W5 |
| F2 W6 | 30 Mar – 5 Apr | W6 |
| F2 W7 | 6 – 12 Apr | W7 |
| (M8 UTS) | 13 – 19 Apr | skip |
| F4 W9 | 20 – 26 Apr | W9 |
| F4 W10 | 27 Apr – 3 Mei | W10 |
| F4 W11 | 4 – 10 Mei | W11 |

## Langkah Eksekusi

### Step 1 — Investigasi Struktur Repo

```bash
cd "student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-submissions/cc-kelompok-a-<nama>" && \
echo "=== ROOT ===" && ls && \
echo "=== BACKEND ===" && ls backend 2>/dev/null && \
echo "=== FRONTEND ===" && ls frontend 2>/dev/null && \
echo "=== DOCS ===" && ls docs 2>/dev/null && \
echo "=== CI ===" && ls .github/workflows 2>/dev/null && \
echo "=== README ===" && head -80 README.md 2>/dev/null || head -80 readme.md
```

Catat:
- Nama project + domain (cek README)
- Anggota tim + NIM + role (cek tabel di README atau `/team` endpoint)
- Apakah `.github/workflows/ci.yml` ada (krusial untuk F4)
- Apakah `docker-compose.prod.yml` ada (krusial untuk F2)

### Step 2 — Investigasi Detail Backend/Frontend/Auth

```bash
# Cek /team endpoint
grep -nE "team|/team" backend/main.py | head -5
# Cek jumlah routes
grep -cE "@app\.(get|post|put|delete|patch)" backend/main.py
# Cek auth+CORS+env
grep -nE "CORSMiddleware|jwt|getenv|load_dotenv" backend/*.py | head -15
# Cek Dockerfile + compose
cat backend/Dockerfile frontend/Dockerfile docker-compose.yml | head -200
# Cek CI workflow (jika ada)
cat .github/workflows/*.yml 2>/dev/null
# Cek tests
ls backend/tests frontend/src/test 2>/dev/null
```

### Step 3 — Hitung Commit per Author per Minggu

```bash
# F1 (M1-4)
for w in "2026-02-24:2026-03-01" "2026-03-02:2026-03-08" "2026-03-09:2026-03-15" "2026-03-16:2026-03-22"; do
  start=${w%:*}; end=${w#*:}
  echo "--- $start to $end ---"
  git log --since="$start" --until="$end 23:59" --pretty=format:"%an" | sort | uniq -c
done

# F2 (M5-7) - W5/W6/W7 dengan tanggal Mar 23 / Mar 30 / Apr 6
# F4 (M9-11) - W9/W10/W11 dengan tanggal Apr 20 / Apr 27 / May 4

# Cek alias author (kadang 1 orang pakai >1 git name)
git log --pretty=format:"%an|%ae" | sort -u

# Cek PR ter-merge untuk F4
git log --grep="(#[0-9]\+)" --pretty=format:"%h|%ad|%s" --date=short
```

**Konsolidasi alias**: jika 1 email punya >1 nama (mis. `Haikal` + `FikriHaikal` + `ryota` semua email `haikalariadma07@gmail.com`), gabung jadi 1 orang. Cantumkan di section B laporan.

### Step 4 — Skor Rubrik per Fase

#### F1 (4 kriteria @ 25%)
- **M1 — README + Team + Project Brief**: kelengkapan problem statement, target user, /team endpoint, member docs
- **M2 — Backend CRUD domain-specific**: jumlah routes, layered structure, schemas/models, tests
- **M3 — Frontend domain-specific**: framework choice, struktur src/, halaman domain
- **M4 — Auth + CORS + .env**: JWT, CORS dari env, env management, .env.example

#### F2 (3 kriteria @ ~33%)
- **M5 — Dockerfile per service**: multi-stage, non-root user, healthcheck, slim base
- **M6 — Compose multi-container**: 3 services, healthcheck DB, depends_on condition, named volume, network
- **M7 — Optimasi & Production config**: docker-compose.prod.yml, image-comparison docs, production override

#### F4 (3 kriteria @ ~33%)
- **M9 — Git workflow + PR history**: jumlah PR ter-merge, CODEOWNERS, conventional commits, branch protection visible
- **M10 — CI YAML (GitHub Actions)**: file `ci.yml` ada? job count? cache? concurrency? coverage gate?
- **M11 — Tests + coverage + badge**: backend tests, frontend tests (Vitest/Jest), CI badge di README

**Tanpa CI workflow → M10 ≈ 25-30, sangat menurunkan nilai F4.**

#### Skor Individu (4 komponen)
| Komponen | Bobot | Indikator |
|---|---|---|
| Konsistensi | 30% | berapa minggu/total minggu aktif commit |
| Substansi | 40% | volume commit + kualitas output |
| Kesesuaian Peran | 20% | apakah commit sesuai role (Backend/Frontend/DevOps/QA) |
| Kualitas Pesan | 10% | deskriptif, conventional commits, ada konteks |

Formula: `Nilai = 0.30*Kons + 0.40*Subs + 0.20*Peran + 0.10*Pesan`. Bulatkan ke integer.

### Step 5 — Generate 3 File Laporan

Gunakan template dari kelompok pilot (hexacore atau antek-antek-asing) sebagai referensi format. Struktur tiap laporan:

```
# Laporan Penilaian Kelompok <nama> – Kelas A
## Fase X: Minggu Kuliah X–X (tanggal)

### Informasi Kelompok
(table dengan repo, project, anggota+NIM+role)

### A. Penilaian Kelompok – <topik>
(table kriteria @ bobot, nilai, catatan dengan bukti file:baris)
Nilai Kelompok: rata-rata
Grade: A/AB/B/BC/C/D/E (skala A≥86, AB 76-86, B 66-76, BC 56-66, C 51-56, D 41-51, E <41)

### B. Distribusi Kontribusi Individual (git log W?–W?)
(table per anggota per minggu, dengan catatan alias)

### C. Penilaian Individual
(per anggota: 4 komponen + Nilai + Grade)

### D. Ringkasan untuk Gradebook
**C<kode> — <nama kolom>:** semua anggota XX
**C<kode> — <nama kolom>:** table urut NIM
```

**Tips**:
- Section A: cantumkan bukti file path & line number (mis. `backend/main.py:181` untuk `/team`)
- Section B: jika W kosong seluruh tim, catat (mungkin libur Lebaran)
- Section D F4: laporan minggu9-11 boleh tambah **Section E: Tren Lintas Fase** seperti hexacore — table F1/F2/F4 per anggota.

### Step 6 — Update README Master Tabel

README pakai HTML table dengan grouped header. Generate ulang pakai Python:

```python
# File: hasil-penilaian-tugasbesar/kelas-A/README.md
# Lokasi: <table>...</table> setelah heading "Tabel Rekapitulasi Kelas A"

# Tambah entry baru di dict `graded` di bawah hexacore + antek-antek-asing:
graded = {
    # ... yang sudah ada ...
    '<NIM-1>': {'C02':X,'C03':X,'C05':X,'C06':X,'C12':X,'C13':X},
    # ... ulang per anggota
}

# Bobot: C01=5,C02=5,C03=5,C04=4,C05=4,C06=4,C07=6,C08=7,C09=4,C10=3,
#        C11=3,C12=3,C13=3,C14=3,C15=3,C16=3,C17=4,C18=6,C19=6,C20=7,C21=4,C22=8
# Total = sum(v*W[k]/100 for k,v in vals.items())

# Re-render tabel HTML lengkap dengan 40 mahasiswa,
# regex replace <table>...</table> di README.md.
```

Atau lebih sederhana: cari baris HTML tertentu di tabel (cari NIM mahasiswa target), edit cell-nya langsung pakai Edit tool. Tapi cara ini riskier — formula Total harus dihitung ulang manual.

**Direkomendasikan: regenerate seluruh tabel pakai script Python**, supaya formula Total akurat.

### Step 7 — Update Header & Mapping di README

Setelah tabel di-regenerate, update:
1. Baris "Status pengisian:" tambah nama kelompok baru
2. Section "Mapping Laporan → Kolom" tambah 6 baris (M1-4 A+C, M5-7 A+C, M9-11 A+C)
3. Section "Status Pengisian per Kelompok" ubah `⬜` jadi `✅` untuk F1/F2/F4

Update juga CLAUDE.md → Status Pengisian table.

## Output Check List

- [ ] 3 file laporan markdown (.md) di `hasil-penilaian-tugasbesar/kelas-A/`
- [ ] Tabel HTML di README updated, kolom Total recalculated
- [ ] Header README "Status pengisian" disebut kelompok baru
- [ ] Mapping Laporan → Kolom ditambah 6 baris baru
- [ ] Status Pengisian table di-update ✅
- [ ] CLAUDE.md Status table di-update ✅
- [ ] xlsx **tidak diedit**

## Gaya & Aturan (CRITICAL)

1. **To-the-point**: jangan tambah framing "anti-halusinasi", "konteks tugas besar", "kolom diisi manual", legenda meta.
2. **Bukti file**: setiap klaim di section A harus punya pointer file:line atau nama file.
3. **Bulatkan ke integer** untuk skor final kelompok & individu (kecuali Total yang 2 desimal).
4. **Urut NIM ascending** di setiap table individu di Section D.
5. **Skala grade**: A≥86, AB 76–<86, B 66–<76, BC 56–<66, C 51–<56, D 41–<51, E <41
6. **Hindari halusinasi**: kalau commit kosong di suatu minggu untuk seluruh tim, catat eksplisit (mungkin libur Lebaran). Jangan tebak.

## Contoh Referensi

Pilot yang sudah selesai sebagai template:
- `hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-hexacore_minggu1-4.md` — proyek bagus, semua deliverable lengkap (skor 87–94)
- `hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-antek-antek-asing_minggu9-11.md` — kasus tanpa CI workflow (skor F4 turun ke 48)

Kedua contoh menunjukkan rubrik mampu membedakan kualitas dengan jelas.
