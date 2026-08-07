# UChicago AI Weather Model Reforecast Archive

A multi-model archive of long-range reforecasts from AI weather
models, initialized 2000–2025 and rolled out to 50 days — beyond the
models' traditional forecast lengths — at daily cadence on a global
0.25° grid. The archive supports benchmarking
of AI weather models, training of downstream ML models, and multi-model
blending. It also powers [AI-Almanac](https://ai-almanac.org),
UChicago-LAUDE's interactive, human-centered forecast platform.
Real-time forecasts initialized from operational ECMWF IFS analyses are
planned alongside the reforecasts.

This repository holds the source for the archive's documentation site,
published with GitHub Pages from [`docs/`](docs/) at
<https://envfluids.github.io/reforecast/>. It does not contain the
forecast data itself.

## Documentation

Full data documentation lives in [`docs/`](docs/): an
[overview](docs/index.html) of the models, archive structure,
zarr format, and sizing methodology, plus
documentation of every model's variables, units, temporal aggregation, and
measured storage cost.

## Data format

One zarr store per model per initialization
(`forecasts_<model>/init_YYYYMMDDT00.zarr`), float32, dimensions
`(time, [number,] prediction_timedelta, lat, lon)`.

## Contact

Adam Marchakitus — marchakitus@uchicago.edu — University of Chicago
