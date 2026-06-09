# 📊 Analisis Indikator Kemiskinan & Kesejahteraan Sosial
## Kabupaten/Kota di Sumatera Barat (2020–2025)

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![BPS](https://img.shields.io/badge/Sumber-BPS%20Sumbar-1565C0?style=flat-square)
![BNSP](https://img.shields.io/badge/Sertifikasi-BNSP%20Data%20Analyst-2E7D32?style=flat-square)

> **Author:** Cindy Nabila Putri  
> **Latar Belakang:** Statistisi Intern — BPS Provinsi Sumatera Barat  
> **Tujuan:** Portofolio Sertifikasi BNSP Data Analyst (SKKNI)

---

## 🎯 Business Question

1. Bagaimana tren kemiskinan di Sumatera Barat selama 2020–2025?
2. Kabupaten/kota mana yang memiliki performa terbaik dan terburuk?
3. Apakah IPM dan TPT berkorelasi dengan tingkat kemiskinan?
4. Apa rekomendasi berbasis data untuk pengambilan kebijakan?

---

## 🗂️ Struktur Repository

```
portofolio-kemiskinan-sumbar/
│
├── 📓 eda_kemiskinan_sumbar.ipynb     ← Notebook EDA utama (Unit 1–7)
│
├── 📁 data/
│   ├── raw/                           ← Data mentah dari BPS (tidak dimodifikasi)
│   │   ├── kemiskinan_kabkota.xlsx
│   │   ├── ipm_kabkota.xlsx
│   │   ├── tpt_kabkota.xlsx
│   │   └── garis_kemiskinan_kabkota.xlsx
│   └── cleaned/                       ← Data bersih siap analisis & Power BI
│       ├── data_sosek_sumbar_2020_2025.csv
│       ├── powerbi_sosek_sumbar.xlsx
│       └── powerbi_ranking_2025.xlsx
│
├── 📁 visualisasi/                    ← Output visualisasi dari notebook
│   ├── viz_tren_provinsi.png
│   ├── viz_ranking_kemiskinan_2025.png
│   ├── viz_scatter_korelasi.png
│   └── viz_heatmap_kemiskinan.png
│
├── 📄 data_dictionary.md              ← Kamus data & dokumentasi sumber
├── 📄 requirements.txt
└── 📄 README.md
```

---

## 📋 Mapping Unit Kompetensi BNSP

Project ini mencakup **8 unit kompetensi** skema Analis Data (SKKNI):

| # | Kode Unit | Judul Unit | Implementasi dalam Project |
|---|-----------|------------|---------------------------|
| 1 | J.62DMS00.001.1 | Identifikasi Kebutuhan Data | Identifikasi 4 indikator strategis BPS, definisi business question |
| 2 | J.62DMS00.004.1 | Merencanakan Integrasi Data | Merge 4 tabel (kemiskinan, IPM, TPT, GK) dengan data lineage |
| 3 | J.62DMI00.004.1 | Mengumpulkan Data | Download data publik BPS via Query Builder, dokumentasi sumber |
| 4 | J.62DMI00.005.1 | Menelaah Data | EDA: statistik deskriptif, visualisasi distribusi, korelasi antar indikator |
| 5 | J.62DMI00.006.1 | Memvalidasi Data | Cek missing values, outlier (IQR), validasi integritas antar indikator |
| 6 | J.62DMI00.007.1 | Menentukan Objek Data | Seleksi 19 kab/kota, 4 variabel, periode 2020–2025 |
| 7 | J.62DMI00.008.1 | Membersihkan Data | Standarisasi nama, reshape wide→long, handling duplikat (Kab/Kota Solok) |
| 8 | J.62DMS00.015.1 | Membuat Business Intelligence | Power BI dashboard interaktif dengan KPI, tren, ranking, korelasi |

---

## 🔍 Temuan Utama

| Indikator | 2020 | 2025 | Perubahan |
|-----------|------|------|-----------|
| % Penduduk Miskin Sumbar | 6.28% | 5.35% | ▼ −0.93 pp |
| IPM Sumbar | 74.29 | 77.27 | ▲ +2.98 poin |
| TPT Sumbar | 6.88% | 5.62% | ▼ −1.26 pp |

**Kab/Kota Kemiskinan Tertinggi (2025):** Kepulauan Mentawai (13.22%)  
**Kab/Kota Kemiskinan Terendah (2025):** Sawahlunto (2.72%)  
**Korelasi Kemiskinan vs IPM:** r = −0.87 (negatif kuat ✅ valid)

---

## 📊 Visualisasi

<table>
<tr>
<td><img src="visualisasi/viz_tren_provinsi.png" width="400"/></td>
<td><img src="visualisasi/viz_ranking_kemiskinan_2025.png" width="400"/></td>
</tr>
<tr>
<td align="center"><i>Tren Kemiskinan & IPM Provinsi</i></td>
<td align="center"><i>Ranking Kemiskinan per Kab/Kota (2025)</i></td>
</tr>
<tr>
<td><img src="visualisasi/viz_scatter_korelasi.png" width="400"/></td>
<td><img src="visualisasi/viz_heatmap_kemiskinan.png" width="400"/></td>
</tr>
<tr>
<td align="center"><i>Korelasi Kemiskinan vs IPM & TPT</i></td>
<td align="center"><i>Heatmap Kemiskinan 2020–2025</i></td>
</tr>
</table>

---

## 🛠️ Tools & Teknologi

| Tahap | Tools |
|-------|-------|
| Pengumpulan Data | BPS Query Builder (bps.go.id) |
| EDA & Cleaning | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| Notebook | Jupyter Notebook / Google Colab |
| Business Intelligence | Power BI Desktop |
| Version Control | Git / GitHub |

---

## ⚙️ Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/cindynabila/kemiskinan-sumbar-analysis.git
cd kemiskinan-sumbar-analysis
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Jalankan Notebook
```bash
jupyter notebook eda_kemiskinan_sumbar.ipynb
```
Atau buka di [Google Colab](https://colab.research.google.com/) dengan upload file `.ipynb` dan folder `data/`.

### 4. Buka Power BI Dashboard
- Buka file `dashboard/dashboard_kemiskinan_sumbar.pbix` di Power BI Desktop
- Atau akses via [Power BI Service](#) *(link menyusul)*

---

## 📁 Sumber Data

| Dataset | Sumber | Diunduh |
|---------|--------|---------|
| Persentase Penduduk Miskin | [BPS Sumbar — Susenas Maret](https://sumbar.bps.go.id) | 9 Juni 2026 |
| Indeks Pembangunan Manusia | [BPS Sumbar — LF SP2020](https://sumbar.bps.go.id) | 9 Juni 2026 |
| Tingkat Pengangguran Terbuka | [BPS Sumbar — Sakernas](https://sumbar.bps.go.id) | 9 Juni 2026 |
| Garis Kemiskinan | [BPS Sumbar — Susenas](https://sumbar.bps.go.id) | 9 Juni 2026 |

---

## 📬 Kontak

**Cindy Nabila Putri**  
📧 cindynabilaputri605@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/cindy-nabila-putri-193022181/)  
🐙 [GitHub](https://github.com/cindynabila)
