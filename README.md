# Sistem Semakan Penghantaran Tugasan Murid

Aplikasi web ringkas untuk guru merekod penghantaran buku kerja atau tugasan murid, mengira mata terkumpul, dan memaparkan dashboard rekod untuk analisis serta cetakan.

## Fungsi Utama

- Dropdown kelas dan nama murid diambil daripada Google Sheet.
- Dropdown subjek diambil daripada Google Sheet.
- Rekod penghantaran murid:
  - Hantar + Lengkap: 3 mata
  - Hantar + Tidak Lengkap: 1 mata
  - Tidak Hantar + Tidak Hadir: 0 mata
  - Tidak Hantar + Tiada Sebab: -2 mata
- Dashboard rekod dengan tapisan kelas, subjek, julat tarikh dan nama tugasan.
- Kolum tarikh dinamik berdasarkan rekod.
- Fungsi cetak laporan dashboard.
- Simpan dan baca semula rekod melalui Google Apps Script.

## Struktur Fail

```text
.
├── index.html
├── README.md
└── apps-script
    └── Code.gs
```

## Konfigurasi Semasa

Sheet ID:

```text
1lUhVEAChZbZq7vR3za9W-kht1DDg7sOQNOni6C_SQvM
```

URL Apps Script:

```text
https://script.google.com/macros/s/AKfycbw4H6vct3919QXZuuQ-vOx_ytNWx7ZwOq_PO0sMdcPHiFnzM4Sbk54Qgbpshsy3kjXicw/exec
```

CSV Kelas & Nama Murid:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vSjpXrSnLktFCatKO1_6h0rPpUQBca9KpKDpfmYpvZnD5PZCvvT9BLUXVxbvysgevCVasrPMqzvhT1z/pub?gid=0&single=true&output=csv
```

CSV Subjek:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vSjpXrSnLktFCatKO1_6h0rPpUQBca9KpKDpfmYpvZnD5PZCvvT9BLUXVxbvysgevCVasrPMqzvhT1z/pub?gid=1032463980&single=true&output=csv
```

## Cara Publish Di GitHub Pages

1. Upload/replace fail `index.html`, `README.md`, dan folder `apps-script/Code.gs` ke repository GitHub.
2. Pergi ke `Settings > Pages`.
3. Pada bahagian `Build and deployment`, pilih:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
4. Klik `Save`.
5. Tunggu GitHub Pages update dan refresh laman web.

## Cara Setup Google Apps Script

1. Buka Google Sheet utama.
2. Pergi ke `Extensions > Apps Script`.
3. Padam kod sedia ada dan tampal kandungan daripada `apps-script/Code.gs`.
4. Klik `Save`.
5. Pergi ke `Deploy > Manage deployments`.
6. Klik `Edit`, pilih `New version`, kemudian `Deploy`.
7. Tetapan Web App:
   - Execute as: `Me`
   - Who has access: `Anyone`
8. Pastikan URL Web App yang digunakan ialah:

```text
https://script.google.com/macros/s/AKfycbw4H6vct3919QXZuuQ-vOx_ytNWx7ZwOq_PO0sMdcPHiFnzM4Sbk54Qgbpshsy3kjXicw/exec
```

## Google Sheet Sumber Dropdown

Data kelas dan nama murid perlu berada dalam format:

```text
KELAS, NAMA MURID
```

Data subjek perlu berada dalam format:

```text
BIL, SUBJEK
```

## Nota Penting

- Selepas mengubah `Code.gs`, deploy Apps Script sebagai versi baharu.
- Jika dashboard tidak memaparkan data terkini, refresh laman web.
- Pastikan Google Sheet sumber dropdown telah dipublish sebagai CSV.

## Konfigurasi Terkini

Sheet ID:

```text
1KVFO1HPPqBtROQFQSeQFsWViPEz3XxkWKufG1ZVmYs8
```

URL Apps Script:

```text
https://script.google.com/macros/s/AKfycby4pH1xTbs8c73fWS-0mrbQtZTDKBjCb-sqc-5jRLwiuzyCXt5BqKIhn3yoG2TeDnc1nQ/exec
```

CSV Kelas & Nama Murid:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQocZ8HAdgWAu1bBEqe6G3soT6TM8qd2y9c-aAciu3A-eOxdq9doiY5huo5vAqJRBQe2ezkH1xu_7tp/pub?gid=0&single=true&output=csv
```

CSV Subjek:

```text
https://docs.google.com/spreadsheets/d/e/2PACX-1vQocZ8HAdgWAu1bBEqe6G3soT6TM8qd2y9c-aAciu3A-eOxdq9doiY5huo5vAqJRBQe2ezkH1xu_7tp/pub?gid=1262893420&single=true&output=csv
```
