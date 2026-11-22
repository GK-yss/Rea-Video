# GitHub Release Preparation

Repository target: **GK-yss/Rea-Video**  
URL: https://github.com/GK-yss/Rea-Video

This preparation set adds repository hygiene, dependency manifests, contributor/security guidance, release checklists, and GitHub Actions CI/build workflows. The existing project README, license, notice, and upstream project attribution are retained.


## Added/updated files

- `.gitignore`: local environments, generated data, caches, media, and secrets exclusions
- `requirements.txt`: runtime dependencies aligned with `pyproject.toml`
- `requirements-dev.txt`: runtime + test/build tooling
- `CONTRIBUTING.md`: contributor workflow and test expectations
- `SECURITY.md`: responsible reporting guidance
- `.github/workflows/ci.yml`: compile, test, and CLI smoke test on Python 3.10/3.12
- `.github/workflows/release.yml`: source/wheel build and SHA-256 artifact generation
- `docs/release/GITHUB_RELEASE_CHECKLIST.md`: release gate
- `docs/release/GITHUB_REPOSITORY_SETUP.md`: target repository and safe push instructions


## Checks to run locally

```bash
python -m pip install -r requirements-dev.txt
python -m compileall -q rea_video
python -m pytest -q
python -m build
rea-video --help
```

## Important

No GitHub push, branch creation, or remote release was performed. Publishing requires confirmation of repository access and manual review of staged changes.
