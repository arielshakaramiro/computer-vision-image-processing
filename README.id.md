# Computer Vision & Image Processing

Catatan belajar, source code, dan eksperimen langsung seputar **Computer Vision & Image Processing** — dari dasar-dasar pakai OpenCV sampai deploy API beneran pakai FastAPI.

*(Untuk dokumentasi utama dalam Bahasa Inggris, lihat [README.md](README.md))*

## Isi Repo

- `notebook/CV_1_Image_Processing.ipynb` — 5 operasi dasar image processing (cropping, grayscale, channel split, convolution, line detection), plus edge detection lanjutan (Sobel, Laplacian, Canny + Gaussian Blur), dibungkus jadi API pakai FastAPI dan di-deploy langsung dari Google Colab + ngrok

## Tech Stack

Python · OpenCV · FastAPI · Pillow · NumPy · Google Colab · ngrok

## Hasil

Kelima operasi dasar sudah divalidasi jalan end-to-end pakai `TestClient` FastAPI, dan dua endpoint (`/grayscale/` beserta versi gambar langsungnya `/grayscale-image/`) sudah tervalidasi tambahan lewat deployment publik sungguhan (Google Colab → ngrok → Swagger UI), dikonfirmasi lewat response HTTP asli dengan header `content-type: image/jpeg` dan `server: uvicorn`.

| Operasi | Input → Output | Endpoint |
|---|---|---|
| Cropping | Gambar → gambar terpotong | `/crop/` |
| Grayscale | Gambar berwarna → hitam-putih | `/grayscale/` |
| Channel Split | 1 gambar → 3 gambar per channel | `/channel_split/` |
| Convolution | Gambar → gambar terfilter | `/convolution/` |
| Line Detection | Gambar → gambar dengan garis tertandai | `/line_detection/` |

Tiap endpoint di atas juga punya versi response gambar langsung (mis. `/grayscale-image/`) buat testing cepat lewat browser/Swagger UI.

## Kredit Gambar

Ilustrasi Spider-Man yang dipakai sebagai contoh gambar di seluruh proyek ini diambil dari [Pinterest](https://id.pinterest.com/pin/828169819021977010/), dipakai murni untuk keperluan demonstrasi teknik image processing. Karakter Spider-Man adalah hak cipta Marvel/Sony.

## Penulis

Muhammad Ariel Shakaramiro

## Lisensi

MIT — lihat [LICENSE](LICENSE).
