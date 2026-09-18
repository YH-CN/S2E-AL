# S2E-AL

This is the official repository for **S2E-AL**, a source-aware AI-generated text detection method.

## Current release

Versioned training and validation data are provided under
[`datasets/supplemental_v1/`](datasets/supplemental_v1/). The files are
independently decompressible gzip JSONL shards. Their row counts, class/source
counts, byte sizes, and SHA256 checksums are recorded in
[`manifest.json`](datasets/supplemental_v1/manifest.json).

This public data package contains training, calibration, and benchmark
validation splits only. It does **not** contain the held-out test split, model
weights, API credentials, generated robustness-test data, or machine-specific
paths. See [`SOURCES_AND_LICENSES.md`](datasets/supplemental_v1/SOURCES_AND_LICENSES.md)
before using or redistributing the data.

Example extraction:

```bash
gzip -dc datasets/supplemental_v1/train_with_s2e.part-*.jsonl.gz > train_with_s2e.jsonl
gzip -dc datasets/supplemental_v1/calibration_with_s2e.part-*.jsonl.gz > calibration_with_s2e.jsonl
gzip -dc datasets/supplemental_v1/benchmark_validation.part-*.jsonl.gz > benchmark_validation.jsonl
sha256sum datasets/supplemental_v1/*.jsonl.gz
```

## Code availability

The complete source code, training and evaluation scripts, model
configurations, and full documentation will be made publicly available after
the paper is accepted.

Until then, this repository provides the data release and integrity metadata
needed to identify the experimental splits, while the code remains under
preparation for the camera-ready release.
