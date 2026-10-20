# Green Screen Sprite Cleaner

A Python-based chroma-key cleanup tool designed to run in **Google Colab**. It removes solid green-screen, magenta, blue, or custom-colored backgrounds from AI-generated game sprites and animation frames while minimizing color spill, unwanted outlines, and edge artifacts.

---

## Features

- **Automatic Background-Color Detection** — Samples image borders and background regions to identify the dominant chroma-key color automatically.
- **Manual Background-Color Selection** — Choose from preset chroma keys (**Green**, **Magenta**, **Blue**) or specify a **Custom** target color.
- **Adjustable Cleanup Sliders** — Fine-tune color tolerance, edge erosion/feathering, spill suppression, and alpha matte thresholds.
- **Interactive Image Previews** — Inspect before-and-after comparisons and alpha edges directly inside the notebook before exporting.
- **Batch Image Processing** — Apply your configured cleanup settings across an entire sequence of animation frames or sprite sheets in one pass.
- **Transparent PNG Output** — Exports clean 32-bit RGBA PNG images with original width and height dimensions preserved.
- **Downloadable ZIP Export** — Packages all processed frames into a single archive for immediate download.

---

## Usage (Google Colab — No Local Installation Required)

> **Note:** This repository is initialized for `green_screen_sprite_cleaner.ipynb`, which will be added from Google Colab. Once the notebook is present in the repository, follow the steps below.

1. **Open in Google Colab**
   - Launch [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and open `Deanx270/green-screen-sprite-cleaner` -> `green_screen_sprite_cleaner.ipynb` (or upload `green_screen_sprite_cleaner.ipynb` directly to Colab).
2. **Run the Setup & Interface Cells**
   - Execute the notebook cells in order (`Runtime -> Run all` or `Shift + Enter` per cell) to load dependencies and launch the interactive widget UI.
3. **Upload Images**
   - Use the upload prompt/widget to upload a single sprite, multiple animation frames, or a `.zip` archive of frames.
4. **Configure Background & Cleanup Settings**
   - Leave background detection on **Auto**, or manually select **Green**, **Magenta**, **Blue**, or a **Custom** color.
   - Adjust the cleanup sliders to eliminate background halos, color spill, and jagged edges.
5. **Preview Results**
   - Check the interactive preview output on sample frames to verify clean alpha transparency and edge quality.
6. **Batch Process & Export**
   - Run the batch processor to convert all uploaded images into transparent PNGs (preserving original dimensions) and download the resulting `.zip` archive.

---

## Technologies Used

- **Python** — Core language and processing pipeline
- **OpenCV (`cv2`)** — Color-space conversion, masking, and morphological edge operations
- **NumPy** — Vectorized pixel and alpha-channel array operations
- **Pillow (`PIL`)** — Image I/O and lossless RGBA PNG export
- **SciPy** — Spatial filtering and matte refinement utilities
- **ipywidgets** — Interactive sliders, selectors, and preview controls in Google Colab

---

## License

This project is licensed under the [MIT License](LICENSE) (© 2026 Deanx270).
