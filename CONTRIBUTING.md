# Contributing

Thanks for contributing to Rea-Video. Before opening a pull request:

1. Create a focused branch from `main`.
2. Keep changes scoped and explain the problem they solve.
3. Use Python 3.10 or newer.
4. Install development dependencies with `python -m pip install -r requirements-dev.txt`.
5. Run `python -m pytest -q` and `python -m compileall -q rea_video`.
6. For CLI changes, include or update tests and documentation.
7. Do not commit API keys, local media, model caches, generated reports, or personal configuration.


## Pull requests

Describe the motivation, notable changes, how to test, and any compatibility or dependency implications. Include screenshots or sample output for UI/report changes where useful. Avoid attaching large source videos; use small synthetic fixtures whenever possible.
