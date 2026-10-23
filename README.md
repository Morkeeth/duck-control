# Duck Control

A readable Kaggle notebook for running the Tufa Labs Duck harness in ARC-AGI-3. The notebook prepares the Kaggle runtime, loads the attached Tufa Labs source bundle and model assets, runs the solver, and writes `submission.parquet` plus diagnostics to `/kaggle/working`.

The solver itself is not implemented in this repository. It comes from the attached `jeroencottaar/taaf-kaggle-source-share` dataset. This repository preserves the public notebook code and the Kaggle metadata needed to attach its declared inputs.

## Run it on Kaggle

1. Accept the rules for the [ARC-AGI-3 competition](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-3).
2. Confirm that your Kaggle account can access all three datasets listed in `kernel-metadata.json`.
3. Install and authenticate the [Kaggle command-line tool](https://github.com/Kaggle/kaggle-api).
4. Change the `id` in `kernel-metadata.json` to a notebook slug under your own Kaggle account.
5. Keep `is_private` set to `true` while testing.
6. Push the notebook, then use Kaggle's **Save & Run All** action with the configured NVIDIA RTX Pro 6000 GPU.

```bash
kaggle kernels push -p .
kaggle kernels status YOUR_USERNAME/YOUR_NOTEBOOK_SLUG
```

An interactive run uses the bundled offline competition environments. A real competition rerun uses the Kaggle gateway. The notebook automatically selects the correct mode.

## Result and source

The first notebook cell describes this as a more readable version of the notebook that produced Tufa Labs' reported milestone score of 1.21. It also states that this readable version has not reproduced that result. The source cell links both the [original Tufa Labs notebook](https://www.kaggle.com/code/jeroencottaar/taaf-duck-harness-kaggle) and the [competition write-up](https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-3/discussion/717133).

That 1.21 figure is a result attributed to the linked original notebook. It is not a result produced or independently verified by this repository snapshot.

## Repository contents

- `duck-control.ipynb`: notebook source, with outputs cleared.
- `kernel-metadata.json`: Kaggle runtime, competition, and dataset configuration.

The downloaded Kaggle snapshot contains no saved cell outputs, credentials, local home paths, wallet data, or personal email addresses.
