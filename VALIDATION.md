# Validation

The nine code cells in `OpenCV_Image_Processing.ipynb` were executed in order
in a fresh Python namespace using the bundled `church.png`. Matplotlib used a
headless backend to capture real figures. This checks the code; it is not a test
of the Jupyter browser interface.

Tested environment:

- Python 3.12.14
- OpenCV 5.0.0 (`opencv-python-headless`)
- NumPy 2.3.5
- Matplotlib 3.10.8

Results:

| Check | Observed result |
| --- | --- |
| Input | 1536 × 1024 pixels; loaded as three-channel BGR, uint8 |
| Resize | 1280 × 853 pixels |
| Grayscale | 1536 × 1024 pixels; one channel |
| ROI crop | 720 × 770 pixels |
| Mean grayscale intensity | 80.83 → 112.69 out of 255 |
| Annotation | Pixels changed on a copy of the original |
| PNG round trips | All five saved processed images decoded and matched their arrays |
| Comparison grid | Saved and decoded successfully with OpenCV and Pillow |
| Original preservation | Input-file SHA-256 unchanged; original array still matches the input |
| Notebook outputs | All nine cells completed; no error outputs |

The ROI is selected manually for this input. The earlier `final_church_image.png`
is included as a separate coursework example and is not reproduced by the new
pipeline because its original logo asset is not part of this project.
