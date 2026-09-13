# Computer Vision & Image Processing

Learning notes, source code, and hands-on experiments on **Computer Vision & Image Processing**, covering the fundamentals with OpenCV through to deploying a working API with FastAPI.

## What's Inside

- `notebook/CV_1_Image_Processing.ipynb` — 5 core image processing operations (cropping, grayscale, channel split, convolution, line detection), plus advanced edge detection (Sobel, Laplacian, Canny + Gaussian Blur), wrapped into a FastAPI service and deployed live via Google Colab + ngrok

## Tech Stack

Python · OpenCV · FastAPI · Pillow · NumPy · Google Colab · ngrok

## Results

All 5 core operations were verified end-to-end using FastAPI's `TestClient`, and two endpoints (`/grayscale/` and its raw-image variant `/grayscale-image/`) were additionally verified through a live public deployment (Google Colab → ngrok → Swagger UI), confirmed via real HTTP responses with `content-type: image/jpeg` and `server: uvicorn` headers.

| Operation | Input → Output | Endpoint |
|---|---|---|
| Cropping | Image → cropped image | `/crop/` |
| Grayscale | Color image → black & white | `/grayscale/` |
| Channel Split | 1 image → 3 per-channel images | `/channel_split/` |
| Convolution | Image → filtered image | `/convolution/` |
| Line Detection | Image → image with lines marked | `/line_detection/` |

Each endpoint above also has a raw-image-response counterpart (e.g. `/grayscale-image/`) for quick browser/Swagger UI testing.

## Image Credit

The Spider-Man illustration used as the example image throughout this project was sourced from [Pinterest](https://id.pinterest.com/pin/828169819021977010/), used purely for demonstrating image-processing techniques. Spider-Man is a trademark/copyright of Marvel/Sony.

## Author

Muhammad Ariel Shakaramiro

## License

MIT — see [LICENSE](LICENSE).
