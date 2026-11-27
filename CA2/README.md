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

Open [CV_HW2_Student.ipynb](CV_HW2_Student.ipynb) in that directory so it can find `data/`. The notebook contains the assignment brief, supplied examples, and implementation and analysis prompts. Dependencies and course data are sufficient for offline execution after setup.

## Files

| Path | Contents |
| --- | --- |
| [`data/manifest.csv`](data/manifest.csv) and `data/inputs/` | 20 official noisy inputs with five `dev` and 15 `eval` samples |
| `data/original/`, `data/source_regions/`, and [`data/corruption.json`](data/corruption.json) | Original crops, equipment-label context, and reproducible corruption settings |
| `data/mapset/` | 360 independent templates covering 40 characters |
| `data/evaluation/` | Reference text, boxes, masks, and oracle crops for evaluation and controlled experiments |
| `data/diagnostic_part2/` | 17 supplementary masks and evaluation data for Part B |
| [`outputs/`](outputs/) | Location for generated artifacts |

## Assignment workflow

1. **Part A (40 points).** Inspect the data, reproduce one corruption, compare two preprocessing routes, and generate and validate their text masks. Compare both routes with a baseline that skips denoising.
2. **Part B (60 points).** Segment left-to-right character boxes, normalize crops and templates with the same function, implement normalized cross-correlation and Levenshtein distance in NumPy/Python, and evaluate and explain errors.
3. Tune on `dev`, save the selected configuration, and record predictions before reading final evaluation labels. Run the reference-mask and oracle controls separately. Report the 17 diagnostic masks outside the main 20-sample results.

## Submission

Submit the notebook executed from a fresh kernel with explanations and analysis in its designated cells. The assignment introduction also asks for a standalone, step-by-step report covering each method, parameter choice, intermediate and final results, and failure cases. Include any helper code and the generated `outputs/` folder. Package the files in `CV-HW2-std1-std2` and ZIP that folder for upload.

The notebook and data are course-provided materials. Mapset font notices are included in `data/mapset/`.
