# Patch 3: Intelligent Overview Sampling

## Change
- `rea_video.survey.overview_times()` keeps activity-weighted frame picks.
- When weighted quantiles collapse onto duplicate frame indices during concentrated activity, deterministic farthest-point temporal filling adds unique frames until the target count is reached (bounded by the number of frames).
- Sampling remains deterministic and preserves timeline coverage while retaining activity-biased selections.

## Validation
- Added regression test for a concentrated activity spike, uniqueness, sorting, and timeline coverage.
- `pytest`: 6 passed.
- `compileall`: passed.
- CLI help: passed.

This patch does not claim an end-to-end video accuracy or runtime benchmark; those require representative input videos.
