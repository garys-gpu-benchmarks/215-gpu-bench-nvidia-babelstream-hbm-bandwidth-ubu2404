# Results: 215 BabelStream HBM Bandwidth

**Main goal:** Measure sustained BabelStream HBM bandwidth  
**Tools:** Compile babelstream.cu with nvcc; run bin/babelstream via collect_babelstream.py

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_140 · recorded 2026-11-13). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 PCIe (81559 MiB) · Intel(R) Xeon(R) Platinum 8352Y CPU @ 2.20GHz · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-13T20:45:51Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 01:09 · benchmark 00:02 · whole run 01:21
- **Source:** run 215_20261113_204551
- **Command:** `bash run_benchmark.sh --smoke --device-id 0 --block-size 256 --array-size 67108864 --warmup-iters 1 --num-iterations 20`

| # | Metric | Result |
|---|---|---|
| 1 | Copy bandwidth (bandwidth_gb_s_copy) | 1835.722146 |
| 2 | Mul bandwidth (bandwidth_gb_s_mul) | 1833.360117 |
| 3 | Add bandwidth (bandwidth_gb_s_add) | 1895.909082 |
| 4 | Triad bandwidth (bandwidth_gb_s_triad) | 1896.63433 |
| 5 | Dot bandwidth (bandwidth_gb_s_dot) | 1961.312728 |
<!-- /profile:smoke -->
