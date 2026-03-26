## arve-ext

`arve-ext` is a modified version of the [ARVE](https://github.com/almoulla/arve) package with minor QOL changes and added hooks to handle certain spectrograph-specific data elements. Currently, we have added compatibility for NEID and HPF. For data from other spectrographs, this package is intended to be fully backwards compatible with `ARVE` v0.8.0.

## Important changes from base version

* Applies separate barycentric corrections to each NEID order. This accounts for chromatic variations in the flux-weighted midpoint of each exposure.
* Allow user to easily restrict analysis to lines within the free spectral range (FSR) of each order using an input FSR file
* Enables the user to compute a reference spectrum from a list of input files passed as an argument and not just when reading all data in a directory.
* Enables the user to specify an input telluric model
* Added HPF compatibility and data ingestion. This includes directly computing order-level barycentric correction with `barycorrpy`.

## Installation

To install this revised version of `ARVE`:

```
git clone https://github.com/afgupta/arve-ext
cd arve-ext
pip install .
```

Note that the package maintains the same internal name of `arve`, so I would recommend using a dedicated environment if you already have the main `ARVE` package installed and want to avoid overwriting it.

## Documentation

See <https://arve.readthedocs.io>

## Citation

If you make use of `ARVE`, please cite the following publication:

[Al Moulla 2025, A&A, 701, A266](https://ui.adsabs.harvard.edu/abs/2025A%26A...701A.266A)
