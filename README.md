# Jurassic Tokenization

[![semantic-release](https://img.shields.io/badge/semantic-release-e10079.svg?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

---

## Prerequisites

- [pyenv](https://github.com/pyenv/pyenv)
- [poetry](https://python-poetry.org/)

## Installation

---

### pip

```bash
pip install jurassic_tokenization
```

### poetry

```bash
poetry add jurassic_tokenization
```

## Usage

---

```python
import jurassic_tokenization

# Your code here
```

## Contribute

---

1. Clone the repository:

   ```bash
   git clone https://github.com/AI21Labs/jurassic-tokenization.git
   ```

2. Set up a virtual environment with the `init` script

   ```bash
   source ./init.sh
   ```

3. Run validation by leveraging [pre-commit](https://pre-commit.com)
   1. Install `pre-commit install --install-hooks -t pre-commit -t commit-msg`
   2. To run on-demand `pre-commit run -a`
      - `pre-commit run shellcheck -a --verbose --hook-stage manual` for recommendation
4. Submit a pull-request

### Run CI tasks locally

```bash
$ inv --list
Available tasks:

  clean          clean (remove) packages
  lint           python lint
  outdated       outdated packages
  test           Run unit tests
  update         update packages
  audit          run safety checks on project dependencies
```

## Publish

Package will be published to our _internal python registry_ defined by `_AR_PYTHON_REPO`.

- In order to publish from a side branch a release candidate, update your branch you should checkout to a branch named `dev` and commit to upstream. Please note that in order to be [PEP compliant](https://peps.python.org/pep-0440/#pre-releases) pre-release branches should be one of the following: `dev`, `alpha` or `beta`.
- Once merging to `master` a new version will be published by [semantic-release](https://github.com/semantic-release/semantic-release)
