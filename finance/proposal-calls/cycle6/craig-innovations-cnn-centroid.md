### CNN-based centroiding and FWHM estimation alongside photutils

**Proposal Category**: Innovations

### Project Team
Matt Craig will lead the project and do the development. The work builds on
the `ballet` CNN model developed by Lionel Garcia, which is now part of the
[`eloy` package](https://github.com/lgrcia/eloy). This could end up in `eloy`
itself or in a small standalone package -- Lionel and I are still sorting that
out. I will check with Larry Bradley about API compatibility with `photutils`.

### Project Description / Scope of Work
The centroiding and FWHM estimators in `photutils` offer tradeoffs between
speed and accuracy. A small convolutional neural network (CNN) can give a
centroid, FWHM and ellipticity for a star cutout much faster than a fit can.
This proposal would make that available through a `photutils`-compatible
interface, either in `eloy` or in a small standalone package.

I don't think the most useful part will be one set of weights that works for
everyone. I think it will be a straightforward "here is how to take our weights
and customize them for your setup", so the proposal includes tools and
documentation for doing that.

Some background:

- The `ballet` centroid model was introduced in `prose`
  ([Garcia et al. 2022](https://arxiv.org/abs/2111.02814)) and follows the
  design of [Herbel et al. 2018](https://arxiv.org/abs/1801.07615). In that
  paper it was as accurate as a 2D Gaussian fit on simulated stars, and it was
  used to reduce observations from TRAPPIST-South. In my own tests it is
  roughly 15–40 times faster than fitting a Gaussian to each star.
- `eloy` includes that centroid-only model. It needs JAX to run and was trained
  without realistic noise.
- Exploratory work aimed at smart telescope images is in
  [`bandaid`](https://github.com/mwcraig/bandaid) and
  [bandaid#188](https://github.com/mwcraig/bandaid/issues/188). It adds a way
  to run the model with only NumPy, training with realistic noise, and a model
  that also returns FWHM and ellipticity. So far this has only been tested on
  smart telescope images, which are tri-color Bayer pattern images with a small
  PSF.
- In that work, a model trained only on simulated stars underestimated FWHM by
  about 0.16 pixels. Fine-tuning on about 1,800 cutouts of bright stars from a
  few dozen of the telescope's own images took 11 minutes on a CPU and got rid
  of that bias. The training labels come from Gaussian fits to those same
  stars.

#### High Priority Objectives
+ I'll be brutally honest here: this is a small project that doesn't address any of the high priority objectives.

#### Project / Work / Deliverables

1. **Package.** Either an addition to `eloy` or a standalone, pip-installable
   package, `[name tbd]`, providing:
   + a `photutils`-compatible centroid function usable as `centroid_func`,
     plus a batched function for many stars at once;
   + an FWHM estimator and ellipticity estimator with the same cutout-based
     interface;
   + a NumPy-only option for running the models, in addition to the existing
     JAX path;
   + bundled pretrained models, including a set for monochrome images trained
     with realistic noise.

   *Deliverable:* a release on PyPI, of `eloy` or of the new package, with
   tests and documentation.
2. **Tuning the model to your own setup.** Tools and documentation for
   building a training set from your own images, fine-tuning the bundled
   weights and using the result. Tuning will require JAX. I will also test the
   minimum number of stars and images needed for training.
   *Deliverable:* documented workflow in the repository, demonstrated on
   monochrome images with well-resolved stars.
3. **Benchmarks.** A reproducible comparison against the `photutils`
   centroiders and `fit_fwhm` on simulated and real images (including crowded
   fields and low signal-to-noise), for both the bundled and the fine-tuned
   weights.
   *Deliverable:* benchmark notebook and summary in the docs.
4. **Integration.** The functionality will for sure be used by the AAVSO's
   smart telescope photometry application, currently at
   https://github.com/mwcraig/bandaid. It will likely be used by
   [`stellarphot`](https://github.com/feder-observatory/stellarphot).
   *Deliverable:* merged PRs or documented reason they were not.

### Approximate Budget
Currency: US $

- Minimum viable budget: 25 hours at $150/hour: $3,750. That covers
  deliverables 1, 2 and 4 and a smaller set of benchmarks.
- Full budget: 35 hours at $150/hour: $5,250
- Travel: none requested
- TOTAL: $3,750–$5,250

### Period of Performance

Jan 1, 2027–Dec 31, 2027.
