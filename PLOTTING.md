# Scientific figures

Keep reusable plotting code in src/ and campaign figures in reports/.

- Answer one question per figure. Show measured effects, negatives, missing values, and uncertainty; never invent, hide, or smooth away evidence.
- Aggregate and resample at the independent unit; preserve pairing. Repeated observations are not independent replications.
- Captions state sample size, units, interval method/coverage, resampling unit, multiplicity, and limits. Separate estimate uncertainty from population spread.
- Use readable labels, accessible colors with redundant markers, and consistent axes. Bars start at zero; justify restricted line/point axes. Avoid decorative 3D, significance stars, and double axes.
- Treat connecting lines as guides unless a model is fitted; leave gaps for missing data.
- Export PDF/SVG and a 300-dpi PNG preview. Inspect at intended size for clipping, legibility, grayscale cues, and numerical agreement.
- Retain source tables, caption, accessible description, and a manifest of hashes, versions, dimensions, and rendering command. Pin plotting dependencies without silently upgrading the research runtime.
- Render completed analysis; do not rerun models or change statistics while plotting. Check the venue's current format before submission.
