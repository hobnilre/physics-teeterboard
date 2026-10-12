# Physics of the teeterboard

Contact, rotation and work in a loaded descent. **Local edition; not published.**

## What this article adds, and why it matters

How do two falling weights transfer work through a teeterboard? This six-page
article develops the event in part 1 of
[Mad Scientist 1](https://github.com/hobnilre/physics-mad-scientist-1), from its
illustrative human launch to the geometry, unilateral contact, torque and
receiver law of the computed lever. Five vector figures and six tables connect
the derivation to the actual contact history, endpoint stores and signal scales.

Independent calculations reproduce 6.994139 J of receiver work and event COP
1.188267 with the companion's fixed height reference. The weights finish below
that reference: their further descent, remaining elastic energy and bearing
heat explain the work account. Comparisons show how load and contact stiffness
affect the result. A load cell, encoder and driver-height measurements can
separate the transfers. The article also retains the distinct preparation and
reset account; numerical predictions and assumed measurement bounds are clearly
identified.

<!-- article-tools:translations:start -->
## Translations

- Svenska: [PDF](sv/physics-teeterboard-sv.pdf) · [Markdown](sv/physics-teeterboard-sv.md)

<!-- article-tools:translations:end -->

## Article and build

[Read the article (PDF)](physics-teeterboard.pdf) ·
[Manuscript source](physics-teeterboard.md)

Install GNU Make, GNU Coreutils, Pandoc, XeLaTeX and the TeX Gyre fonts, including
the LaTeX packages used by `preamble.tex`, `preamble-local.tex` and the standalone
TikZ/PGFPlots figures. Run `make pdf` to build both editions from this repository;
no sibling repository, private research file or network access is required.
`make -B pdf` forces a rebuild. Figure data are embedded in local TeX inputs.

The title date is pinned in `ARTICLE_DATE` and in each edition's metadata.
The first-page PDF creation time advances on rebuild. The GitHub address is a
planned destination; this delivery is committed only locally. Intermediates go
to ignored `build/`; `BUILD_DIR=/absolute/path` selects another directory.
`make clean` removes that build directory and preserves the article PDFs.

The shared article-tools theme is installed as independent build inputs in
`article-style.yaml`, `preamble.tex` and `figures/figure-style.tex`.
Article-specific definitions belong in `preamble-local.tex`; Swedish labels and
figures live in `sv/`. The scientific calculations and review records are kept
outside this publication checkout.
