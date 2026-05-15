---
name: nilai-kelompok
description: Menilai 1 kelompok tugas besar MK Komputasi Awan untuk fase yang dipilih (F1 M1-4, F2 M5-7, F4 M9-11, F5 M12-14, atau F6 M15-16). Investigasi repo kelompok, hitung commit per minggu per anggota, aplikasi baseline floor role-aware, generate file laporan markdown, dan update tabel master di README.md kelas yang relevan. Trigger saat user minta menilai kelompok dengan input nama kelompok + fase (mis. "/nilai-kelompok hexacore F5" atau "/nilai-kelompok bismillah_a F1").
---

# Skill: Nilai Kelompok Tugas Besar — Komputasi Awan SI2514027

## Tujuan

Menghasilkan **file laporan markdown** untuk fase yang dipilih + **update tabel master di README** kelas yang relevan.

**Fase yang didukung:**
- **F1 (M1-4)** Foundation — README, /team, backend CRUD, frontend, auth+CORS+env
- **F2 (M5-7)** Containerization — Dockerfile, docker-compose, optimasi
- **F4 (M9-11)** CI/CD — Git workflow + PR, GitHub Actions YAML, tests + badge
- **F5 (M12-14)** Microservices — ADR, service decomposition, inter-service comm, gateway
- **F6 (M15-16)** Final + UAS — Security checklist, dokumentasi C4 + reflection paper, demo production URL, demo CI/CD end-to-end

> M8 (UTS) dinilai dosen manual — skip.

## Input

Nama kelompok + fase (opsional). Contoh:
- `/nilai-kelompok hexacore` — F1+F2+F4 default
- `/nilai-kelompok bismillah_a F5` — fase tertentu saja
- `/nilai-kelompok awit F6` — F6 saja

## Konteks Awal

Sebelum mulai, baca **CLAUDE.md** di root project untuk peta direktori, mapping kolom gradebook (C01–C22), aturan, dan metodologi penilaian.

### Path repo per kelas

**Kelas A:**
```
student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-submissions/cc-kelompok-a-<nama>/
```

**Kelas B** (perhatikan path beda, tidak ada prefix `b-`):
```
student-repos/kelas-B/cc-kelompok-submissions/cc-kelompok-<nama>/
```

### Path output

**Kelas A:**
```
hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-<nama>_minggu<X-Y>.md
hasil-penilaian-tugasbesar/kelas-A/README.md  ← update tabel + status
```

**Kelas B:**
```
hasil-penilaian-tugasbesar/kelas-B/cc-kelompok-<nama>_minggu<X-Y>.md
hasil-penilaian-tugasbesar/kelas-B/README.md  ← update tabel + status
```

## Periode Tanggal per Fase (kalender 2026)

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
| F5 W12 | 11 – 17 Mei | W12 |
| F5 W13 | 18 – 24 Mei | W13 |
| F5 W14 | 25 – 31 Mei | W14 |
| F6 W15 | 1 – 7 Jun | W15 |
| F6 W16 | 8 – 14 Jun | W16 |

## Langkah Eksekusi

### Step 1 — Investigasi Struktur Repo

```bash
# Kelas A
cd "student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-submissions/cc-kelompok-a-<nama>"
# Kelas B
cd "student-repos/kelas-B/cc-kelompok-submissions/cc-kelompok-<nama>"

echo "=== ROOT ===" && ls
echo "=== BACKEND ===" && ls backend 2>/dev/null
echo "=== FRONTEND ===" && ls frontend 2>/dev/null
echo "=== DOCS ===" && ls docs 2>/dev/null
echo "=== CI ===" && ls .github/workflows 2>/dev/null
echo "=== SERVICES (F5 indicator) ===" && ls services 2>/dev/null
echo "=== README ===" && head -80 README.md 2>/dev/null || head -80 readme.md
```

**Yang dicari per fase:**
- F1: README, /team endpoint, backend CRUD, frontend struktur, auth+CORS+env
- F2: Dockerfile per service, docker-compose.yml, docker-compose.prod.yml, image-comparison docs
- F4: `.github/workflows/ci.yml`, tests folder, CI badge di README, PR usage
- F5: `services/` folder, `docs/adr-*.md`, gateway config (nginx/traefik), inter-service auth, observability
- F6: `docs/c4-*.md`, `reflection-<nama>.md`, production URL di README, security audit notes, CI/CD push→deploy workflow

### Step 2 — Investigasi Detail Sesuai Fase

```bash
# Generic checks
grep -nE "team|/team" backend/main.py 2>/dev/null | head -5
grep -cE "@app\.(get|post|put|delete|patch)|@router\.(get|post|put|delete|patch)" backend/main.py backend/app/*.py 2>/dev/null
grep -nE "CORSMiddleware|jwt|getenv|load_dotenv|SECRET_KEY" backend/auth.py backend/main.py 2>/dev/null | head -15

# F2 checks
ls docker-compose*.yml backend/Dockerfile frontend/Dockerfile 2>/dev/null
ls docs/image-comparison*.md docs/docker-architecture*.md 2>/dev/null

# F4 checks
cat .github/workflows/*.yml 2>/dev/null
ls backend/tests frontend/src/test* 2>/dev/null

# F5 checks (microservices)
ls services/ 2>/dev/null
find . -name "adr-*.md" -o -name "ARCHITECTURE.md" 2>/dev/null
grep -rE "nginx|traefik|api-gateway" services/ docker-compose.yml 2>/dev/null | head -10

# F6 checks (final)
find . -name "c4-*.md" -o -name "reflection-*.md" -o -name "SECURITY.md" 2>/dev/null
grep -nE "ALLOWED_ORIGINS|rate.limit|RateLimit|input.validation" services/ backend/ 2>/dev/null | head -10
```

### Step 3 — Hitung Commit per Author per Minggu

```bash
# F1
for w in "2026-02-24:2026-03-01" "2026-03-02:2026-03-08" "2026-03-09:2026-03-15" "2026-03-16:2026-03-22"; do
  start=${w%:*}; end=${w#*:}
  echo "--- $start to $end ---"
  git log --since="$start" --until="$end 23:59" --pretty=format:"%an" | sort | uniq -c
done

# F2: 2026-03-23, 2026-03-30, 2026-04-06 (W5-W7)
# F4: 2026-04-20, 2026-04-27, 2026-05-04 (W9-W11)
# F5: 2026-05-11, 2026-05-18, 2026-05-25 (W12-W14)
# F6: 2026-06-01, 2026-06-08 (W15-W16)

# Cek alias author
git log --pretty=format:"%an|%ae" | sort -u

# Cek PR ter-merge dalam fase
git log --grep="(#[0-9]\+)" --since="<start>" --pretty=format:"%h|%ad|%s" --date=short
```

**Konsolidasi alias**: jika 1 email punya >1 nama (mis. `Haikal` + `FikriHaikal` semua email `haikalariadma07@gmail.com`), gabung jadi 1 orang. Cantumkan di section B laporan.

### Step 4 — Skor Rubrik per Fase

#### F1 (4 kriteria @ 25%)
- M1 README+Team+Brief · M2 Backend CRUD · M3 Frontend · M4 Auth+CORS+.env

#### F2 (3 kriteria @ ~33%)
- M5 Dockerfile per service · M6 Compose multi-container · M7 Optimasi + Production

#### F4 (3 kriteria @ ~33%)
- M9 Git workflow + PR · M10 CI YAML · M11 Tests + coverage + badge

**Tanpa CI workflow → M10 ≈ 25-30, sangat menurunkan nilai F4.**

#### F5 (3 kriteria @ ~33%)
- M12 ADR + service boundaries (`docs/adr-*.md`, decision rationale)
- M13 Microservices implementation (separate services, gateway, inter-service comm via HTTP REST + auth)
- M14 Architecture diagram + monitoring (service health, structured logging, circuit breaker)

#### F6 (komponen lebih kompleks)
- C17 Security checklist (4%): rate limiting, input validation, secret audit, no hardcoded SECRET_KEY, CORS production
- C18 Dokumentasi teknis (6%): README, C4 diagram, reflection paper (mix kelompok + individu)
- C19 Demo URL cloud (6%): production deployment accessible (Railway/Render URL alive)
- C21 Demo CI/CD end-to-end (4%): push → auto-deploy ke production
- C22 Dokumentasi final + reflection paper individual (8%): per-anggota reflection paper

#### Skor Individu — Rubrik 4 Komponen

| Komponen | Bobot | Indikator |
|---|---|---|
| Konsistensi | 30% | berapa minggu/total minggu fase aktif commit |
| Substansi | 40% | volume commit substantif + kualitas output |
| Kesesuaian Peran | 20% | apakah commit sesuai role |
| Kualitas Pesan | 10% | deskriptif, conventional commits, ada konteks |

Formula: `Nilai = 0.30*Kons + 0.40*Subs + 0.20*Peran + 0.10*Pesan`. Bulatkan ke integer.

### Step 5 — Aplikasi Baseline Floor 70 (role-aware)

Setelah dapat skor mentah, aplikasikan floor:

```
adjusted = max(raw, 70)  jika role off-phase AND raw >= 50
adjusted = raw           jika role prime-time atau raw < 50
```

**Pemetaan prime time per fase:**

| Fase | Prime time | Off-phase |
|---|---|---|
| F1 | Backend, Frontend, QA & Docs | DevOps, Container, CI/CD, Deploy |
| F2 | DevOps, Container, CI/CD, Deploy, Backend | Frontend, QA & Docs |
| F4 | CI/CD, DevOps, Deploy, QA & Docs | Backend, Frontend |
| F5 | Backend, DevOps, Container | Frontend, QA & Docs |
| F6 | SEMUA (final sprint, semua role kontribusi) | — |

> Skor mentah ditampilkan di laporan Section C. Skor post-floor masuk ke README master tabel.

### Step 6 — Generate File Laporan

Nama file:
- F1: `cc-kelompok-[a-]<nama>_minggu1-4.md`
- F2: `cc-kelompok-[a-]<nama>_minggu5-7.md`
- F4: `cc-kelompok-[a-]<nama>_minggu9-11.md`
- F5: `cc-kelompok-[a-]<nama>_minggu12-14.md`
- F6: `cc-kelompok-[a-]<nama>_minggu15-16.md`

(Prefix `a-` hanya untuk kelas A.)

Struktur laporan:

```markdown
# Laporan Penilaian Kelompok <nama> – Kelas <X>
## Fase <N>: Minggu Kuliah <X>–<Y> (tanggal) — <Nama Fase>

### Informasi Kelompok
| Field | Detail |
| Project | (nama project + 1 kalimat deskripsi) |
(table anggota + NIM + role)

### A. Penilaian Kelompok – <Topik>
| Kriteria | Bobot | Nilai | Catatan |
**Nilai Kelompok: rata-rata** · **Grade: A/AB/B/...**

### B. Distribusi Kontribusi Individual (git log W?–W?)
> Catatan alias jika ada
(table per anggota per minggu)

### C. Penilaian Individual
#### 1. <Nama> (Role)
- Konsistensi <%> · Substansi <%> · Peran <%> · Pesan <%>
**Nilai: <raw>** · **Grade: <X>**

### D. Ringkasan untuk Gradebook
**C<kode> — <nama kolom>:** semua anggota <skor kelompok>
**C<kode> — <nama kolom>:** table urut NIM (skor individu, post-floor untuk gradebook)

### E. Tren Lintas Fase (hanya di laporan terakhir per kelompok)
(table F1/F2/F4/F5/F6 per anggota)
```

**Skala grade:** A ≥ 86, AB 76–<86, B 66–<76, BC 56–<66, C 51–<56, D 41–<51, E < 41

**Tips:**
- Section A: cantumkan bukti file path & line number (mis. `backend/main.py:181` untuk `/team`)
- Section B: jika W kosong seluruh tim, catat (mungkin libur / sprint break)
- Section D: skor individu yang ditulis adalah **post-baseline-floor** (yang masuk gradebook)
- Section E hanya di laporan terakhir fase per kelompok (F1 laporan W1-4 boleh tidak ada section E, tapi F6 laporan W15-16 wajib ada section E lintas-fase)

### Step 7 — Update README Master Tabel

README pakai HTML table dengan grouped header (rowspan + colspan). Pendekatan: split by `## ` heading, regex replace tabel di section yang sesuai.

**Cara aman update:**
```python
import re
with open('README.md','r',encoding='utf-8') as f: c = f.read()
parts = c.split('## ')
new_parts = []
for part in parts:
    if part.startswith('Tabel Rekapitulasi'):  # reguler
        part = re.sub(r'<table>.*?</table>', new_reg_html, part, count=1, flags=re.DOTALL)
    elif part.startswith('Tabel Mahasiswa Magang'):  # magang
        part = re.sub(r'<table>.*?</table>', new_mag_html, part, count=1, flags=re.DOTALL)
    new_parts.append(part)
c = '## '.join(new_parts)
with open('README.md','w',encoding='utf-8') as f: f.write(c)
```

> ⚠️ **Jangan** pakai `re.sub(...count=1)` dua kali berurutan tanpa anchor — call kedua akan re-match tabel pertama yang baru di-replace (bug pernah terjadi).

### Step 8 — Update Status & Header

Setelah tabel ter-regenerate, update:
1. Header "Status pengisian:" tambah nama kelompok + fase baru
2. Section "Mapping Laporan → Kolom" tambah row baru
3. Section "Status Pengisian per Kelompok" ubah `⬜` jadi `✅`
4. Update **CLAUDE.md** Status Pengisian table

## Output Checklist

- [ ] File laporan markdown untuk fase yang dipilih
- [ ] Tabel HTML di README updated dengan skor post-baseline-floor
- [ ] Kolom Adj tetap kosong (untuk dosen)
- [ ] Header README "Status pengisian" disebut kelompok+fase baru
- [ ] Mapping Laporan → Kolom ditambah row baru
- [ ] Status Pengisian table di-update ✅
- [ ] CLAUDE.md Status table di-update ✅
- [ ] xlsx **tidak diedit**

## Gaya & Aturan (CRITICAL)

1. **To-the-point**: jangan tambah framing "anti-halusinasi", "konteks tugas besar", "kolom diisi manual oleh dosen", "Opsi A/B/C", atau legenda meta. Tulis hasilnya langsung.
2. **Bukti file**: setiap klaim di section A harus punya pointer file:line atau nama file.
3. **Bulatkan ke integer** untuk skor final (kecuali Total 2 desimal di README master).
4. **Urut NIM ascending** di setiap table individu di Section D.
5. **Skala grade**: A≥86, AB 76–<86, B 66–<76, BC 56–<66, C 51–<56, D 41–<51, E <41
6. **Hindari halusinasi**: kalau commit kosong di suatu minggu untuk seluruh tim, catat eksplisit. Jangan tebak.
7. **Magang students** (NIM tidak di gradebook xlsx) → laporan tetap dibuat, tapi nilai masuk ke **tabel magang terpisah** di README, bukan tabel reguler.

## Contoh Referensi

Pilot yang sudah selesai sebagai template:
- `hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-hexacore_minggu1-4.md` — proyek bagus, semua deliverable lengkap (skor 87–94)
- `hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-antek-antek-asing_minggu9-11.md` — kasus tanpa CI workflow (skor F4 turun ke 48)
- `hasil-penilaian-tugasbesar/kelas-B/cc-kelompok-bismillah_a_minggu9-11.md` — kasus terbaik kelas B F4 dengan CI+CD lengkap (skor 94)
- `hasil-penilaian-tugasbesar/kelas-A/cc-kelompok-a-team-agile_minggu9-11.md` — kasus magang abandoned (skor 25)

Rubrik mampu membedakan kualitas dengan jelas: kelompok lengkap deliverable → A; kelompok tanpa CI → D; kelompok abandoned → E.
