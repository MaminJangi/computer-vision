# Computer Assignment 2

Fundamentals of Computer Vision, University of Tehran, fall semester 1405–1406.

**Group members:** Mohammad Amin Jangi and Narges Jafari.

CA2 reads short strings from cropped equipment labels using classical image processing. The pipeline preprocesses the crop, creates a text mask, segments and normalizes characters, and matches them against the supplied Mapset.

## Run

From `CA2/`, install the supplied dependencies and start JupyterLab:

```sh
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open [CV_HW2_Student.ipynb](CV_HW2_Student.ipynb) in that directory so it can find `data/`. The executed notebook includes the assignment brief, implementations, and analysis for A1–A4 and B1–B5. The editable Persian report is [CA2_Report.docx](CA2_Report.docx). Dependencies and course data are sufficient for offline execution after setup.

## Files

| Path | Contents |
| --- | --- |
| [`data/manifest.csv`](data/manifest.csv) and `data/inputs/` | 20 official noisy inputs with five `dev` and 15 `eval` samples |
| `data/original/`, `data/source_regions/`, and [`data/corruption.json`](data/corruption.json) | Original crops, equipment-label context, and reproducible corruption settings |
| `data/mapset/` | 360 independent templates covering 40 characters |
| `data/evaluation/` | Reference text, boxes, masks, and oracle crops for evaluation and controlled experiments |
| `data/diagnostic_part2/` | 17 supplementary masks and evaluation data for Part B |
| [`outputs/`](outputs/) | Generated masks, overlays, crops, evaluation tables, and frozen configuration |

## Assignment workflow

1. **Part A (40 points).** Inspect the data, reproduce one corruption, compare two preprocessing routes, and generate and validate their text masks. Compare both routes with a baseline that skips denoising.
2. **Part B (60 points).** Segment left-to-right character boxes, normalize crops and templates with the same function, implement normalized cross-correlation and Levenshtein distance in NumPy/Python, and evaluate and explain errors.
3. Tune on `dev`, save the selected configuration, and record predictions before reading final evaluation labels. Run the reference-mask and oracle controls separately. Report the 17 diagnostic masks outside the main 20-sample results.

## Submission

Submit the executed notebook and standalone report. Include any helper code and the generated `outputs/` folder with the required CSVs, masks, overlays, crops, and configuration. Package the files in `CV-HW2-std1-std2` and ZIP that folder for upload.

The notebook and data are course-provided materials. Mapset font notices are included in `data/mapset/`.
