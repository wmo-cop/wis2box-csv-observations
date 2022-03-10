# wis2box-csv-observations

## Overview

[wis2box](https://github.com/wmo-im/wis2box) CSV observations data ingest plugin

## Installation

The easiest way to install wis2box-csv-observations is via the Python [pip](https://pip.pypa.io/en/stable/)
utility:

```bash
# via PyPI
pip install wis2box-csv-observations

# directly from GitHub
pip install https://github.com/wmo-cop/wis2box-csv-observations/archive/main.zip
```

### Requirements
- Python 3
- [virtualenv](https://virtualenv.pypa.io/)

### Dependencies
Dependencies are listed in [requirements.txt](requirements.txt). Dependencies
are automatically installed during wis2box-csv-observations installation.

### Installing wis2box-csv-observations

```bash
# setup virtualenv
python3 -m venv --system-site-packages wis2box-csv-observations
cd wis2box-csv-observations
source bin/activate

# clone codebase and install
git clone https://github.com/wmo-cop/wis2box-csv-observations.git
cd wis2box-csv-observations
python setup.py build
python setup.py install
```

## Running

- install into wis2box container/environment
- update `WIS2BOX_DATADIR_DATA_MAPPINGS` (see sample `data-mappings.yml`)


```bash
# create dataset topic hierarchy directories
wis2box data setup --topic-hierarchy observations-surface-land.mw.FWCL.landFixed

# display dataset topic hierarchy and directories
wis2box data info --topic-hierarchy observations-surface-land.mw.FWCL.landFixed

# process incoming data file (manually/no PubSub)
wis2box data process /path/to/file.csv

# process incoming data directory (manually/no PubSub)
wis2box data process /path/to/dir

# copy discovery-metadata.yml into $WIS2BOX_DATADIR/metadata/discovery
cp discovery-metadata.yml $WIS2BOX_DATADIR/metadata/discovery

# publish dataset discovery metadata to local catalogue
wis2box metadata discovery publish observations-surface-land.mw.FWCL.landFixed

# unpublish discovery metadata to local catalogue
wis2box metadata discovery unpublish observations-surface-land.mw.FWCL.landFixed
```

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

All bugs, enhancements and issues are managed on [GitHub](https://github.com/wmo-cop/wis2box-csv-observations/issues).

## Contact

* [Tom Kralidis](https://github.com/tomkralidis)
