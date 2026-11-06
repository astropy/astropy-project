### CNN-based centroiding and FWHM estimation alongside photutils

**Proposal Category**: Innovations

### Project Team
Matt Craig will lead the project and do the development. The work builds on
the `ballet` CNN model developed by Lionel Garcia as part of the [`eloy`
package](https://github.com/lgrcia/eloy); I will coordinate with him on reuse of the model and training
approach, and with Larry Bradley on API compatibility and possible photutils integration.

### Project Description / Scope of Work
The centroiding and FWHM estimators in `photutils` offer tradeoffs between speed and accuracy. The `ballet` model in `eloy` is a small
convolutional neural network, trained on simulated stellar cutouts, that
returns a centroid for a cutout and is comparable in accuracy to a 2D Gaussian fit at a much higher speed.

- Exploratory work aimed primarily at smart telescope images is at https://github.com/mwcraig/bandaid/issues/188 and that package itself.
- The work in that repository focuses and will continue to focus on smart telescope images for the foreseeable future. These telescopes produce tri-color Bayer pattern images with a small PSF. One motivation for this proposal is to extend the work to ensure it also works well for monochrome images with well-resolved stars.
- This proposal packages that capability as a small, standalone package or as an addition to `photutils`. It would also extended the CNN to return an elipticity and FWHM estimate. In addition, it would provide a documented workflow for retraining the model on new data, which leads to better accuracy.


#### High Priority Objectives
+ I'll be brutally honest here: this is a small project that doesn't address any of the high priority objectives.

#### Project / Work / Deliverables

1. **Package.** A pip-installable package, `[name tbd]`, or an addition to photutils, providing:
   + a `photutils`-compatible centroid function usable as `centroid_func`;
   + an FWHM estimator and ellipticity estimator with the same cutout-based interface;
   + one or more bundled pretrained model.
   *Deliverable:* first release on PyPI with tests and documentation.
2. **Training and retraining tools.** Scripts and documentation for
   regenerating the training set and retraining the model.
   *Deliverable:* documented training workflow in the repository.
3. **Benchmarks.** A reproducible comparison against the `photutils`
   centroiders on simulated and real images (including crowded fields and
   low signal-to-noise).
   *Deliverable:* benchmark notebook and summary in the docs.
4. **Integration.** The functionality will for sure be used by the AAVSO's smart telescope photometry application, currently at https://github.com/mwcraig/bandaid. It will likely be used by [`stellarphot `](https://github.com/feder-observatory/stellarphot).
   *Deliverable:* merged PRs or documented reason they were not.

### Approximate Budget
Currency: US $

- Total effort: 25 hours at $150/hour: $3750
- Hours/effort split between proposer and potential collaborators
- Travel: none requested
- TOTAL: $3750

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
