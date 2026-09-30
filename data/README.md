# Data Tugas 1

## Dataset yang Dipilih

Isi informasi berikut sebelum Milestone 1.

| Item | Isi |
|---|---|
| Nama dataset | `[Flood Prediction Dataset]` |
| Sumber | `[https://www.kaggle.com/datasets/farahfirdausa/flood-prediction-dataset]` |
| Lisensi/ketentuan pakai | `[MIT License]` |
| Ukuran | `[> 1.000.000 baris]` |
| Periode data | `[2003 s.d 2015]` |
| Unit analisis | `[Satu titik grid koordinat lokasi (lon, lat) pada satu tanggal kejadian tertentu di Sulawesi Selatan]` |

## Deskripsi Singkat
Dataset ini dibuat untuk pemodelan prediksi banjir di Sulawesi Selatan. Deskripsi di halaman sumber menyebut data berasal dari berbagai sumber pemerintah, pengamatan satelit (MODIS), dan pemantauan lokal. Setiap baris memiliki label kejadian banjir.

## Deskripsi Kolom
| Kolom | Keterangan |
|---|---|
| `date` | Tanggal kejadian/citra |
| `lon`, `lat` | Koordinat titik grid (derajat) |
| `flooded` | Penanda genangan pada titik tersebut |
| `jrc_perm_water` | Float (0/1) | Penanda badan air permanen, nilai 1 menandakan wilayah tersebut terdeteksi sebagai air permanen(selalu digenangi air, nilai 0 menandakan wilayah tersebut daratan kering |
| `precip_1d` | Curah hujan 1 hari (satuan mm) |
| `precip_3d` | Curah hujan akumulasi 3 hari (satuan mm) |
| `NDVI` | Indeks vegetasi, skala sekitar -2000 s.d. 10000 (skala MODIS ×10.000) |
| `NDWI` | Indeks air, skala sekitar -1 s.d. 1 |
| `landcover` | Kelas tutupan lahan (kategori 1-17) |
| `elevation` | Ketinggian |
| `slope` | Kemiringan lereng |
| `aspect` | Arah hadap lereng (derajat, 0-360) |
| `upstream_area` | Luas area hulu |
| `TWI` | Topographic Wetness Index |
| `target` | Label banjir |

## Tempat Mencari Dataset

Pilih dataset Indonesia yang legal digunakan, dapat didokumentasikan sumbernya, dan memenuhi batas ukuran tugas.

| Situs | Kegunaan |
|---|---|
| [Satu Data Indonesia](https://data.go.id/) | Portal data terbuka lintas instansi pemerintah Indonesia. |
| [Badan Pusat Statistik](https://www.bps.go.id/) | Statistik sosial, ekonomi, kependudukan, dan data wilayah. |
| [BMKG Data Online](https://dataonline.bmkg.go.id/) | Data cuaca, iklim, gempa bumi, dan observasi meteorologi. |
| [Hugging Face Datasets](https://huggingface.co/datasets) | Dataset publik yang dapat dicari berdasarkan topik, bahasa, atau ukuran. |
| [Kaggle Datasets](https://www.kaggle.com/datasets) | Katalog dataset publik; periksa lisensi dan dokumentasi pembuatnya. |
| [Google Dataset Search](https://datasetsearch.research.google.com/) | Mesin pencari untuk menemukan dataset dari berbagai portal. |

## Cara Memperoleh Data

1. Buka URL sumber di atas.
2. Unduh file ke folder `data/raw/` tanpa mengubah data mentah.
3. Catat nama file dan checksum bila tersedia.
4. Ubah variabel `DATA_PATH` pada `notebooks/01_data_profiling.ipynb` agar menunjuk ke file tersebut.

## Aturan Penyimpanan

- Jangan commit dataset mentah atau hasil olahan berukuran besar ke Git.
- File pada `data/raw/` adalah data asli dan tidak boleh diubah.
- Simpan hasil transformasi yang dapat direproduksi pada `data/processed/`.
