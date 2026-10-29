# Studi Ablasi RNN, LSTM, GRU vs ANN untuk Prediksi Trafik Seluler Milan

Tugas Workshop Deep Learning — Teknik Telekomunikasi ITERA.

<!-- Ganti seluruh isian bertanda [ ... ] di bawah. Hapus komentar ini. -->

## Kelompok

| Peran | Nama | NIM |
|---|---|---|
| Ketua | [Grasia Okta Adelia] | [124400059] |
| Anggota | [Egista Marga Kola] | [124400003] |
| Anggota | [Muhammad Allam Dzaky] | [124400013] |

- **Kelas:** [RA]
- **Lokasi kelompok:** [3] — [Stadio San Rio] (3)
- **Laporan:** [`laporan-latex/main.pdf` atau `laporan-typst/main.pdf`]

## Cara Menjalankan

```bash
uv sync
uv run jupyter lab
```

Buka `tugas_ablasi.ipynb`, isi `LOKASI_KELOMPOK`, lalu jalankan semua sel. Semua run tercatat di `hasil/ablasi.csv`.

Perangkat yang kami pakai: [Jupyter Notebook, Visual Studio Code, dan Overleaf], total waktu training: 59.8 menit.

## Ringkasan Hasil

Hasil eksperimen menunjukkan bahwa konfigurasi terbaik memberikan pengaruh berbeda pada setiap arsitektur model. Pada lokasi Duomo, test MAE terbaik untuk ANN adalah 273,3, RNN 242,9, LSTM 247,3, dan GRU 233,8. Pada lokasi kelompok, Stadio San Siro, LSTM menghasilkan test MAE 10,9 ± 0,1, sedangkan GRU mencapai 11,4 ± 0,3; keduanya menunjukkan penurunan error dibandingkan konfigurasi acuan. Secara keseluruhan, hasil ini menunjukkan bahwa pemilihan arsitektur dan hiperparameter perlu mempertimbangkan karakteristik lokasi karena model dengan performa baik pada satu lokasi belum tentu memberikan hasil terbaik pada lokasi lain.

## Struktur

```
tugas_ablasi.ipynb      notebook eksperimen (di-commit beserta output)
data/                   data trafik per jam (Duomo + 10 lokasi tugas)
hasil/                  CSV seluruh run, tabel, dan grafik
laporan-latex/ atau laporan-typst/   sumber laporan + PDF
```

## Data

Telecom Italia Big Data Challenge (Barlacchi dkk., 2015, *Scientific Data*, lisensi ODbL), versi per jam dari Zhang dkk. (INFOCOM 2021). Disiapkan oleh pengajar di repo [mctosima/dl-workshop](https://github.com/mctosima/dl-workshop).
