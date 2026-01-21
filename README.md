# Verification-gated persuasion

This repository provides code, data, and analysis notebooks to reproduce the
experiments and figures reported in the paper:

**Scaffolding or override: verification governs responses to corrupted reasoning traces**  

The repository is organized to support full reproduction of all main figures
(Fig. 1–5) and Extended Data figures (ED Fig. 1–3).

---

## Repository structure

````text
verification-gated-persuasion/
├── figures/        # Final PDF figures used in the manuscript
├── notebooks/      # Jupyter notebooks for each experiment
└── results/        # Raw and aggregated experiment outputs
````

---

## Figures

The `figures/` directory contains the final PDF figures exactly as used in the manuscript.

### Main Figures
- `fig1_overview.pdf` — Overview of scaffolding vs. override regimes
- `fig2_verification_quality.pdf` — Verification × trace quality interaction (core result)
- `fig3_verification_cost.pdf` — Verification cost within-domain analyses
- `fig4_failure_modes.pdf` — Adoption vs. distraction failure modes
- `fig5_mitigations.pdf` — Recovery and mitigation experiments

### Extended Data Figures
- `ed_fig1_authority.pdf` — Authority cues do not modulate CIF
- `ed_fig2_sequential.pdf` — No accumulation across repeated exposure
- `ed_fig3_confidence.pdf` — Confidence does not predict CIF

Each PDF contains one figure per page, following Nature-style conventions.

---

## Notebooks

The `notebooks/` directory contains one Jupyter notebook per experiment.
Notebook names correspond directly to experiment identifiers referenced in the paper.

Key notebooks include:

- `CoT_A1_E2_complexity.ipynb` — Verification cost by problem complexity
- `CoT_A1_E4_errortype.ipynb` — Verification cost by error detectability
- `CoT_A1_E6_trace_quality.ipynb` — Trace quality effects (open-ended tasks)
- `CoT_A1_E6prime_trace_quality_MC.ipynb` — Trace quality effects (multiple-choice tasks)
- `CoT_A1_E7_sequential.ipynb` — Sequential exposure analysis
- `CoT_A1_E8_domain.ipynb` — Domain-level generalization
- `CoT_A1_E9_confidence.ipynb` — Confidence vs. CIF analysis
- `CoT_A1_E10_recovery.ipynb` — Recovery and mitigation experiments

Additional notebooks (e.g., format swap or exploratory analyses) are included
for completeness but are not required to reproduce the main figures.

---

## Results

The `results/` directory contains all raw outputs and aggregated summaries
produced by the notebooks.

Each experiment has a dedicated subdirectory (e.g.,
`exp_A1_E6_trace_quality_20260120/`) containing:

- `checkpoints/` — model outputs and intermediate results
- `results/` — aggregated metrics and summaries (JSON)
- `traces/` — stored reasoning traces used in the experiments
- `.png` files — intermediate visualizations generated during analysis

The file `all_summaries.json` provides a consolidated summary across experiments.

---

## Figure-to-experiment mapping

The following mapping links manuscript figures to experiment directories:

- **Fig. 1** → `exp_B_domain_generalization_20260120`
- **Fig. 2** → `exp_A1_E6_trace_quality_20260120`,  
               `exp_A1_E6prime_trace_quality_MC_20260120`
- **Fig. 3** → `exp_A1_E2_complexity_20260120`,  
               `exp_A1_E4_errortype_20260120`
- **Fig. 4** → `exp_A1_E6_trace_quality_20260120`
- **Fig. 5** → `exp_A1_E10_recovery_20260120`

- **ED Fig. 1** → `exp_A1_E5_source_20260120`
- **ED Fig. 2** → `exp_A1_E7_sequential_20260120`
- **ED Fig. 3** → `exp_A1_E9_confidence_20260120`

---

## Notes

- All experiments were conducted with deterministic decoding (temperature = 0).
- The repository is organized for reproducibility of the manuscript figures.
- Exploratory or preliminary analyses are included for transparency but do not
  affect the reported results.

---

## Data and code availability

A Zenodo DOI will be provided upon release.  
All code and data necessary to reproduce the reported results are included in this repository.
