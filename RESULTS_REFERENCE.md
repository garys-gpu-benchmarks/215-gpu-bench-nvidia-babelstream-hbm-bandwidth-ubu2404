# Results: 215 BabelStream HBM Bandwidth

**Main goal:** Measure sustained BabelStream HBM bandwidth  
**Tools:** Compile babelstream.cu with nvcc; run bin/babelstream via collect_babelstream.py

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · AMD EPYC 9374F 32-Core Processor · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-12T23:00:53Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:29 · benchmark 00:01 · whole run 00:37
- **Source:** run 215_20261112_230053
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --block-size 256 --array-size 67108864 --warmup-iters 1 --num-iterations 20`

| # | Metric | Result |
|---|---|---|
| 1 | Copy bandwidth (bandwidth_gb_s_copy) | 3297.52222 |
| 2 | Mul bandwidth (bandwidth_gb_s_mul) | 3295.675909 |
| 3 | Add bandwidth (bandwidth_gb_s_add) | 3628.604573 |
| 4 | Triad bandwidth (bandwidth_gb_s_triad) | 3627.427714 |
| 5 | Dot bandwidth (bandwidth_gb_s_dot) | 2626.549685 |
<!-- /profile:smoke -->
