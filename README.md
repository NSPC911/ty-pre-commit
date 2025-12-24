# ruff-pre-commit

[![ty](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ty/main/assets/badge/v0.json)](https://github.com/astral-sh/ty)
[![image](https://img.shields.io/pypi/v/ty/0.0.6.svg)](https://pypi.python.org/pypi/ty)
[![image](https://img.shields.io/pypi/l/ty/0.0.6.svg)](https://pypi.python.org/pypi/ty)
[![image](https://img.shields.io/pypi/pyversions/ty/0.0.6.svg)](https://pypi.python.org/pypi/ty)
[![Actions status](https://github.com/NSPC911/ty-pre-commit/workflows/main/badge.svg)](https://github.com/NSPC911/ty-pre-commit/actions)

A [pre-commit](https://pre-commit.com/) hook for [ty](https://github.com/astral-sh/ty).

Distributed as a standalone repository to enable installing Ruff via prebuilt wheels from
[ty](https://pypi.org/project/ty/).

### Using ty with pre-commit

To run ty's [checker](https://docs.astral.sh/ty/type-checking) via pre-commit, add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/NSPC911/ty-pre-commit
  # ty version.
  rev: v0.0.6
  hooks:
    # Run the linter.
    - id: ty-check
```

To avoid running on Jupyter Notebooks, remove `jupyter` from the list of allowed filetypes:

```yaml
repos:
- repo: https://github.com/NSPC911/ty-pre-commit
  # ty version.
  rev: v0.0.6
  hooks:
    # Run the linter.
    - id: ty-check
      types_or: [ python, pyi ]
```

## License

ty-pre-commit is licensed under the MIT License, until Astral makes their own repo.

- MIT license ([LICENSE](LICENSE) or <https://opensource.org/licenses/MIT>)
