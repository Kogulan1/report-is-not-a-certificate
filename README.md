# The report is not a certificate

**Metric integrity and residual failures of a Gaussian-copula synthesizer for flat clinical tables**

Kogulan Natarajan · Gesalp AI ([gesalpai.ch](https://gesalpai.ch)), Winterthur, Switzerland · Kogulan1@gmail.com

**Status:** Unpublished manuscript, not peer-reviewed. Version of October 2026.

Prepared for the ETH AI Center Doctoral Fellowship 2027 (proposed mentors: Prof. Gunnar Rätsch and Prof. Florian Tramèr, ETH Zurich).

- 📄 Paper (PDF): [`Natarajan_2026_report_is_not_a_certificate.pdf`](Natarajan_2026_report_is_not_a_certificate.pdf)
- 🧾 LaTeX source: [`Natarajan_2026_report_is_not_a_certificate.tex`](Natarajan_2026_report_is_not_a_certificate.tex)

## Abstract

Synthetic data is often proposed as a way to share clinical tables without moving patient records. The evidence that accompanies a synthetic table is usually a quality report, and that report is only as trustworthy as the code that computes it. This manuscript studies the evaluation contract of Gesalp AI, a service that turns one de-identified flat clinical CSV into a synthetic table drawn from a Gaussian copula, together with a report of nine gated checks. Each check is PASS, WARN, FAIL, or N/A, and a check that could not be computed stays N/A. Three findings are reported. *Metric integrity:* until revision v2-35 (6 September 2026), a correlation check that crashed was stored as 0.0 and displayed as a perfect pass; we describe the defect and the rule that replaced it. *Calibration:* the pass bar for mean Kolmogorov–Smirnov (KS) distance (at most 0.10) is supported by a real-versus-real null at $`n \ge 200`$, and the pass bar for privacy gain (at least 0.87) is the fifth percentile of a 960-draw null in which the synthetic table is replaced by a disjoint real sample; the $`t`$-closeness failure line stays at 0.28. *Residual failures:* on a recorded 26-table gate (v2-46, 18 September 2026), 22 of 26 tables had no failing check, 12 of 26 had every measured check at PASS, and 26 of 26 passed KS. Wisconsin, Heart VA, and thyroid fail $`t`$-closeness at 0.324, 0.300, and 0.350 while their marginals and downstream classifier utility hold; we argue that on these tables the quasi-identifiers nearly determine the label. Mammographic masses fails duplicate rate, linkage, and outlier shielding. A completed run is not a GDPR or HIPAA determination, does not make a table anonymous, and carries no differential-privacy guarantee. We close with a research agenda for privacy-preserving clinical machine learning: paired $`t`$-closeness, holdout membership inference, and differentially private generation evaluated under the same checks.

## Building the PDF

The source is a single self-contained LaTeX file (no external `.bib` or figures). It compiles with XeLaTeX or [Tectonic](https://tectonic-typesetting.github.io/):

```sh
tectonic Natarajan_2026_report_is_not_a_certificate.tex
# or
xelatex Natarajan_2026_report_is_not_a_certificate.tex && xelatex Natarajan_2026_report_is_not_a_certificate.tex
```

It also compiles with pdfLaTeX (T1 + Latin Modern + cmap are loaded automatically).

## Suggested citation

> Natarajan, K. (2026). *The report is not a certificate: metric integrity and residual failures of a Gaussian-copula synthesizer for flat clinical tables.* Unpublished manuscript, not peer-reviewed. https://github.com/Kogulan1/report-is-not-a-certificate

```bibtex
@unpublished{natarajan2026report,
  author = {Natarajan, Kogulan},
  title  = {The report is not a certificate: metric integrity and residual failures of a {G}aussian-copula synthesizer for flat clinical tables},
  note   = {Unpublished manuscript, not peer-reviewed},
  year   = {2026},
  month  = oct,
  url    = {https://github.com/Kogulan1/report-is-not-a-certificate}
}
```

## License

Copyright © 2026 Kogulan Natarajan. All rights reserved.

The manuscript is shared publicly for reading and citation. No licence to reproduce, modify, or redistribute it is granted without the author's written permission.
