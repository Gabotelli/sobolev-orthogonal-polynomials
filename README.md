# Bachelor’s thesis: zeros of Sobolev orthogonal polynomials

Source files for my BSc thesis at Universidad Politécnica de Madrid, *Zeros of Sobolev Orthogonal Polynomials: Visualization and Analysis*. The work combines mathematical analysis with Maple computations and figures of polynomial zeros.

## Research overview / Main contribution

The thesis combines **theoretical analysis and computational experimentation in Maple** to study the location of zeros of Sobolev orthogonal polynomials. My computational contribution consists of Maple algorithms for constructing the polynomial families, computing and visualizing their zero sets, and comparing zero localization with multiplication-operator norms and singular values.

The experiments cover real and complex support configurations and help formulate and investigate conjectures in approximation theory. Numerical observations are distinguished from proven results in the manuscript; finite plots alone do not establish asymptotic claims.

## Maple files and reproduction

- `Sobolev4.mw` and `tfg6.mw`: substantial worksheets containing executable inputs and saved outputs.
- `tfg7.mw`: a smaller worksheet containing procedures and further calculations.
- `tfg7.maple`: a Maple workbook stored as a SQLite container, not a plain-text script.
- `presentacion.mw`: presentation-oriented plotting worksheet.
- The 55 remaining `.m` files are serialized Maple calculation states, beginning with `M7R0` and saved `D_matX` objects. They are **generated results/cache files**, not independent source programs.

Open the worksheets in a compatible Maple installation and inspect their input cells before execution. Some cells load saved results and assemble filenames dynamically; a portable, clean regeneration of every figure has not yet been verified. The existing figures remain available for compiling the manuscript and presentation.

See [the file-by-file Maple inventory](docs/maple-inventory.md) for sources, cached results, dependency gaps and the completed duplicate cleanup. Two exact duplicate states were removed; identical bytes remain under their descriptive filenames.

## Manuscript and presentation

- `latex/tfg_latex_etsiinf-2023.02.20/tfg_etsiinf_plantilla.tex` — main thesis document; `secciones/` contains the included chapters and bibliography, and `include/` contains the figures and title-page assets.
- `latex/presentacion.tex` — defense slides, with supporting sections in `latex/`.
- `maple/` — source worksheets, a workbook and saved calculation states for the numerical examples.

Compiled PDFs, TeX build output, template archives, working drafts and unreferenced animations have been removed. A suitable TeX installation is needed to regenerate the manuscript and slides; a clean build has not been verified here.
