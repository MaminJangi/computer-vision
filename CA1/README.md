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
| 2 | Document noise, manual filtering, edges, and PSNR | [Q2.ipynb](Q2.ipynb) | [Q2.html](Q2.html) |
| 3 | Video noise, median filtering, and Gaussian filtering | [Q3.ipynb](Q3.ipynb) | [Q3.html](Q3.html) |

Questions 1, 2, and 3 are complete and included.

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
├── Q2.ipynb
├── Q2.html
├── Q3.ipynb
├── Q3.html
├── requirements.txt
└── outputs/
    ├── Q1/
    ├── Q2/
    └── Q3/
```

Saved figures and results are organized by question under `outputs/`. Each notebook contains its methods, parameter choices, results, analysis, and relevant references; detailed experimental settings are kept in the reports rather than repeated here.

## Submission

The notebooks, HTML reports, source inputs, and generated videos for all three questions are present. The assignment requests a submission folder named `CV-HW1-810102429-810101601`.

## References

- [Pillow: grayscale conversion](https://pillow.readthedocs.io/en/stable/reference/Image.html#PIL.Image.Image.convert)
- [Matplotlib: RGB-to-HSV conversion](https://matplotlib.org/stable/api/_as_gen/matplotlib.colors.rgb_to_hsv.html)
- [OpenCV: smoothing images](https://docs.opencv.org/4.13.0/d4/d13/tutorial_py_filtering.html)

The assignment PDF and input files are course-provided materials; this repository does not add a license to those materials.
