# Scientific figures

Read before plotting. Reusable plotting code belongs in src/; figures, source tables, captions, and manifests belong in the campaign's reports/ directory.

- One figure answers one question. Show measured effects, negative outcomes, missing values, and uncertainty honestly; never invent or selectively omit observations.
- Aggregate and resample at the independent experimental unit. Preserve pairing. Do not treat repeated observations from one subject/system as independent replications.
- State sample size, interval method/coverage, resampling unit, multiplicity, units, and relevant limitations. Distinguish estimate uncertainty from population spread.
- Use readable labels, accessible colors with redundant markers/line styles, white background, and consistent scales. Bars start at zero; justify restricted point/line axes. Avoid decorative 3D, significance stars, and double axes.
- Captions explain evidence and provenance. Lines between observations are guides unless a fitted model is declared. Do not connect missing observations or smooth away unfavorable results.
- Export vector PDF/SVG and a 300-dpi PNG preview at intended physical size. Inspect legibility, clipping, color/grayscale distinctions, and numerical agreement.
- Retain source data tables, accessible text descriptions, captions, and a manifest with hashes, software versions, dimensions, and rendering command. Pin plotting dependencies when selected; do not upgrade the research runtime silently.
- Render completed analysis artifacts. Plotting must not rerun models or silently recompute statistics. Check the target venue's current format before submission.
