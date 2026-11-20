# Results: 125 DistilBERT NLP Training Baseline

**Main goal:** Measure DistilBERT classification training throughput  
**Tools:** Run inline DistilBertForSequenceClassification training on synthetic tokens

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_149 · recorded 2026-11-19). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-149-generic · driver 7.1.9.31600000
- **Run:** 2026-11-19T22:04:04Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 01:28 · benchmark 00:02 · whole run 01:43
- **Source:** run 125_20261119_220404
- **Command:** `bash run_benchmark.sh --smoke --model-name distilbert-base-uncased --sequence-len 32 --batch-size 2 --learning-rate 5.0000000000000002E-5 --weight-decay 0.01 --num-iterations 2 --gradient-accumulation 1 --warmup-iters 1`

| # | Metric | Result |
|---|---|---|
| 1 | Training throughput (samples_per_sec) | 37.55810779179284 |
| 2 | Training step time, ms (step_time_ms) | 53.25081899991346 |
| 3 | Token throughput (tokens_per_sec) | 1201.859449337371 |
| 4 | Peak GPU memory (peak_gpu_memory_gb) | 1.512544256 |
<!-- /profile:smoke -->
