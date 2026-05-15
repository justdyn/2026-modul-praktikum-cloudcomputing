# Konteks Project — Komputasi Awan SI2514027

Proyek ini berisi materi praktikum + sistem penilaian tugas besar untuk MK Komputasi Awan, ITK.

## Struktur Direktori Penting

- `[01-15]-modul.md` — modul praktikum per minggu (RPS)
- `student-repos/kelas-A/cc-kelompok-a-submissions/cc-kelompok-a-submissions/cc-kelompok-a-<nama>/` — repo tugas besar tiap kelompok (12 kelompok kelas A), hasil `gh classroom clone -a 952202`
- `hasil-penilaian/` — penilaian Fase 1 **versi modul lama** (jangan diubah, hanya rujukan)
- `hasil-penilaian-tugasbesar/kelas-A/` — penilaian **tugas besar** (output utama)
  - `README.md` — master tabel rekap 40 mahasiswa × 22 kolom
  - `cc-kelompok-a-<nama>_minggu1-4.md` — laporan F1 per kelompok
  - `cc-kelompok-a-<nama>_minggu5-7.md` — laporan F2
  - `cc-kelompok-a-<nama>_minggu9-11.md` — laporan F4
  - `nilai_kelas__SI2514027_2026-05-15.xlsx` — template gradebook (jangan diedit lagi tanpa instruksi user)

## Mapping Fase → Modul → Kolom Gradebook

22 kolom, total bobot 100%. Detail lengkap di `hasil-penilaian-tugasbesar/kelas-A/README.md` section "Pemetaan Kolom Gradebook".

Singkat:
- **F1 (M1-4 Foundation):** C01 Kuis (5%, manual), C02 Tugas kelompok (5%), C03 Git individu (5%)
- **F2 (M5-7 Containerization):** C04 Kuis (4%, manual), C05 Tugas kelompok (4%), C06 Git individu (4%)
- **M8 UTS:** C07–C10 (diisi dosen manual di gradebook)
- **F4 (M9-11 CI/CD):** C11 Kuis (3%, manual), C12 Tugas kelompok (3%), C13 Git+PR individu (3%)
- **F5 (M12-14 Microservices):** C14 Kuis (3%, manual), C15 Tugas kelompok (3%), C16 Git+Arch individu (3%)
- **F6 (M15-16 Final+UAS):** C17 Security (4%), C18 Dok C4 (6%), C19 Demo URL (6%), C20 Viva (7%, manual), C21 CI/CD demo (4%), C22 Dok final (8%)

## Aturan Penting

1. **Kolom kuis (C01, C04, C11, C14) dan viva (C08, C20) selalu kosong** — dosen isi manual saat sesi kelas.
2. **xlsx tidak boleh diedit** tanpa instruksi eksplisit user. README.md adalah single source of truth.
3. **Tidak ada nilai tanpa bukti** — setiap angka di README harus tertelusur ke laporan kelompok (Section A untuk kelompok, Section C untuk individu).
4. **Gaya tulisan to-the-point**: tidak ada framing "anti-halusinasi", "tugas besar", "konteks", "diisi manual oleh dosen", atau legenda meta. Tulis hasilnya langsung.
5. **Output tabel ke gradebook**: angka bulat untuk skor kelompok & individu. Format tabel Section D: dua sub-tabel terpisah (kelompok + individu), urut NIM.

## Workflow Grading Tugas Besar

Untuk menilai kelompok, gunakan skill `/nilai-kelompok <nama-kelompok>` atau ikuti [.claude/skills/nilai-kelompok/SKILL.md](.claude/skills/nilai-kelompok/SKILL.md).

## Status Pengisian (per 2026-05-15)

| Kelompok | F1 | F2 | F4 | F5 | F6 |
|---|:---:|:---:|:---:|:---:|:---:|
**Reguler:**
| Kelompok | F1 | F2 | F4 | F5 | F6 |
|---|:---:|:---:|:---:|:---:|:---:|
| hexacore | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| antek-antek-asing | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| awit | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| ethereal | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| extraordinary | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| miracle | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| nexa | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| steam | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| suksesss | ✅ | ✅ | ✅ | ⬜ | ⬜ |

**Magang/konversi (tabel terpisah di README, NIM tidak di gradebook xlsx):**
| Kelompok | F1 | F2 | F4 | F5 | F6 |
|---|:---:|:---:|:---:|:---:|:---:|
| nyawit 🎓 | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| pria-solo 🎓 | ✅ | ✅ | ✅ | ⬜ | ⬜ |
| team-agile 🎓 | ✅ | ✅ | ✅ | ⬜ | ⬜ |
