# wis2node-malawi-observations

## Overview

wis2node Malawi observations data ingest plugin

## Installation

The easiest way to install wis2node-malawi-observations is via the Python [pip](https://pip.pypa.io/en/stable/)
utility:

```bash
# via PyPI
pip install wis2node-malawi-observations

# directly from GitHub
pip install https://github.com/wmo-cop/wis2node-malawi-observations/archive/main.zip
```

### Requirements
- Python 3
- [virtualenv](https://virtualenv.pypa.io/)

### Dependencies
Dependencies are listed in [requirements.txt](requirements.txt). Dependencies
are automatically installed during wis2node-malawi-observations installation.

### Installing wis2node-malawi-observations

```bash
# setup virtualenv
python3 -m venv --system-site-packages wis2node-malawi-observations
cd wis2node-malawi-observations
source bin/activate

# clone codebase and install
git clone https://github.com/wmo-cop/wis2node-malawi-observations.git
cd wis2node-malawi-observations
python setup.py build
python setup.py install
```

## Running

- install into wis2node container/environment
- update `WIS2NODE_DATADIR_DATA_MAPPINGS` (see sample `data-mappings.yml`)


## Development

### Running Tests

```bash
# install dev requirements
pip install -r requirements-dev.txt

# run tests like this:
python tests/run_tests.py

# or this:
python setup.py test
```

## Releasing

```bash
python setup.py sdist bdist_wheel --universal
twine upload dist/*
```

### Code Conventions

* [PEP8](https://www.python.org/dev/peps/pep-0008)

### Bugs and Issues

All bugs, enhancements and issues are managed on [GitHub](https://github.com/wmo-cop/wis2node-malawi-observations/issues).

## Contact

* [Tom Kralidis](https://github.com/tomkralidis)
