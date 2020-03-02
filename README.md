# pre-commit-poetry-export
Export a [Poetry](https://python-poetry.org) project's `poetry.lock` to a pip-compliant `requirements.txt` with a pre-commit hook.


## Usage
To your [.pre-commit-config.yaml](https://pre-commit.com/#2-add-a-pre-commit-configuration) add:

```yaml
- repo: https://github.com/seandstewart/pre-commit-poetry-export
  rev: master
  hooks:
    - id: export-requirements
    - id: export-requirements-dev
```

This will export two files: `requirements.txt`, with only the main dependencies, and `requirements-dev.txt` with the dev dependencies included.
