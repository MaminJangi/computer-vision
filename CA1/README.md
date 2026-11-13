# Computer Assignment 1

Fundamentals of Computer Vision, University of Tehran, fall semester 1405–1406.

| Group member | Student number |
| --- | --- |
| Mohammad Amin Jangi | 810102429 |
| Narges Jafari | 810101601 |

## Contents

| Question | Topic | Notebook | HTML report |
| --- | --- | --- | --- |
| 1 | Color spaces, segmentation, contrast, and illumination | [Q1.ipynb](Q1.ipynb) | [Q1.html](Q1.html) |
| 3 | Video noise, median filtering, and Gaussian filtering | [Q3.ipynb](Q3.ipynb) | [Q3.html](Q3.html) |

Questions 1 and 3 are complete. Question 2 is handled separately by the teammate and is not included here yet.

## Run

Use Python 3.12 and install the dependencies from this directory:

```sh
python -m pip install -r requirements.txt
```

Open the notebooks in a Jupyter-compatible editor, select the Python environment, and run cells from top to bottom. If a notebook server is needed, install JupyterLab separately with `python -m pip install jupyterlab` and start it with `python -m jupyterlab` from this directory. Core dependency versions match the environment used for these reports.

The HTML reports include their figures and equations and can be opened directly in a browser without running the notebooks. GitHub serves HTML files as source/downloads; download a report to view its rendered form locally.

## Files

```text
CA1/
├── CV-HW1-Fani.pdf
├── HW1_Files/
│   ├── Peppers.png
│   ├── scanned_document.png
│   └── park_video.mp4
├── Q1.ipynb
├── Q1.html
├── Q3.ipynb
├── Q3.html
├── requirements.txt
└── outputs/
    ├── Q1/
    └── Q3/
```

Question 3 generates `noisy_video.mp4`, `filtered_video_1.mp4` (median), and `filtered_video_2.mp4` (Gaussian) under `outputs/Q3/`. All three retain 450 frames at 30 FPS, 1280 × 720 pixels, and 15 seconds. Noise is added to 5% of spatial pixel positions, split equally between salt and pepper, using a fixed random seed of 42.

The reports discuss parameter choices and limitations, including the Gaussian filter's weakness against salt-and-pepper noise. References appear next to the relevant explanations in the notebooks.

## Submission

The notebooks, HTML reports, source inputs, and generated videos for Questions 1 and 3 are present. Add the teammate's Question 2 work before assembling the complete course submission. The assignment requests a submission folder named `CV-HW1-810102429-810101601`.

## References

- [Pillow: grayscale conversion](https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.convert)
- [Matplotlib: RGB-to-HSV conversion](https://matplotlib.org/stable/api/_as_gen/matplotlib.colors.rgb_to_hsv.html)
- [OpenCV: smoothing images](https://docs.opencv.org/4.13.0/d4/d13/tutorial_py_filtering.html)

The assignment PDF and input files are course-provided materials; this repository does not add a license to those materials.
