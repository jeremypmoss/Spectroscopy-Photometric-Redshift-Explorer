# Spectroscopy & Photometric Redshift Explorer

A self-contained interactive astronomy teaching tool for exploring spectroscopy, redshift, broadband photometry, colour–redshift relations, and photometric-redshift degeneracy directly in a web browser.

The entire explorer runs from a single `index.html` file: no installation, server, package manager, or external JavaScript libraries are required.

## What it does

The explorer brings several related ideas together in one interactive page:

- **Wavelength and spectral colour** — enter a wavelength in nm, Å, or µm and see an approximate visible colour, frequency, photon energy, spectral region, and nearby reference line.
- **Spectral-line reference sets** — switch between major, hydrogen, nebular, stellar-absorption, and combined line catalogues. Clicking a visible line marker jumps directly to that wavelength.
- **Hydrogen-series explorer** — generate Lyman, Balmer, and Paschen wavelengths from the Rydberg relation and inspect their series limits.
- **Synthetic spectra** — compare schematic emission and absorption spectra using the selected line sets.
- **Redshift calculator** — convert between rest and observed wavelength using `λ_obs = λ_rest(1 + z)`.
- **Doppler velocity** — compare classical and relativistic longitudinal Doppler velocities for a wavelength shift.
- **Redshifted quasar visualiser** — move a source from `z = 0` to `z = 5` and watch spectral features pass through broadband filters.
- **Filter sets** — explore schematic versions of SDSS `ugriz`, Legacy Surveys `grz`, GALEX `FUV/NUV`, WISE `W1/W2`, or a combined UV–optical–IR set.
- **Synthetic photometry** — integrate the teaching spectrum through the selected filter profiles and calculate relative magnitudes and colour indices.
- **Colour–redshift tracks** — see how a selected colour evolves with redshift and click the curve to jump the whole explorer to that `z`.
- **Colour–colour tracks** — follow the synthetic quasar locus through two-colour space, including loops and self-approaches that illustrate photometric-redshift degeneracy.
- **Degeneracy finder** — identify the closest pair of substantially separated redshifts in the displayed colour–colour track.
- **Toy photometric-redshift estimator** — add configurable photometric noise and inspect a `P(z)`-style relative-likelihood curve, including secondary solutions and multimodal cases.
- **Interactive plot interrogation** — hover over the photometric-redshift likelihood curve to read the sampled `z`, relative likelihood, and Δχ².

## Running it

Download `index.html` and open it in a modern web browser.

That is all.

Because the page is fully self-contained, it can also be hosted directly with GitHub Pages.

## Suggested activities

A few useful teaching demonstrations:

1. Select **Hα** and increase redshift to watch the line move from the visible into the infrared.
2. Choose **Simple quasar spectrum** with **SDSS ugriz** and watch broad emission features move through the filters.
3. Compare the colour–redshift track for different filter combinations.
4. Inspect loops or close approaches in the colour–colour diagram and use the degeneracy finder to identify distinct redshifts with similar broadband colours.
5. Open the toy photometric-redshift estimator, increase the photometric uncertainty, and watch a narrow single solution broaden or develop secondary peaks.
6. Compare a sparse optical filter set with broader UV–optical–IR coverage to see qualitatively why extra wavelength coverage can reduce redshift ambiguity.

## Scientific scope and limitations

This is an **educational visualisation**, not a research-grade photometric-redshift code.

In particular:

- Displayed monochromatic colours are approximate sRGB representations. A monitor cannot reproduce the complete physical spectral locus.
- Broadband filter responses are schematic profiles centred on representative band wavelengths rather than published system-throughput curves.
- The quasar spectrum is a simplified power-law continuum with representative broad emission features.
- The Lyα forest and Lyman-limit behaviour use a deliberately simplified teaching prescription rather than a physical intergalactic-medium transmission model.
- Synthetic magnitudes and colours are relative and are intended to illustrate trends, not reproduce survey photometry.
- The toy `z_phot` estimator compares simplified synthetic colours over `0 ≤ z ≤ 5`; its likelihoods should not be interpreted as calibrated posterior probabilities.
- The Doppler panel uses a special-relativistic longitudinal Doppler interpretation and is conceptually distinct from a full cosmological distance–redshift relation.

These approximations are intentional: the goal is to make the underlying relationships visible and interactive without hiding them beneath a large physical or software model.

## Technical notes

- Vanilla HTML, CSS, and JavaScript
- No dependencies
- No network requests
- No build step
- Responsive desktop/mobile layout
- Canvas-based spectra and diagnostic plots
- Runs locally from a single file

## Licence

Released under the MIT License. See [`LICENSE`](LICENSE).
