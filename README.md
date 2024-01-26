
# A Hexagonal Quickstart Template

This is python, fastapi, postgres and docker quickstart template for Hexagonal Architecture projects.

This is an ongoing work in progress and is based on [Shako Rzayev's](https://github.com/ShahriyarR) hexagonal architecture repositories combined with [Python Alicante's](https://github.com/pythonalicante) meetup selector repository for docker setup.

## Setup

Pull down the files to your empty initialized repo.

Unzip the files and delete the repo.zip file.

Copy the files to the root of your repo.

Delete the downloaded repo.zip file and the unzipped subfolder.

```
curl -sL https://github.com/davidjnevin/template-python-fastapi-docker-postgres/archive/master.zip -o repo.zip
unzip repo.zip
cp -r template-python-fastapi-docker-postgres-main/ .
rm -rf template-python-fastapi-docker-postgres-main
```

### Update the App Name to a project name of your choice

Update the repo url in `pyproject.toml`.

Change 'appname' and description in `src/appname/__init__.py`

Change 'appname' folder to the project name.

Change 'appname' to the project name in:
1.	`MakeFile` (migrations, migrate and run commands)
1.	`pyproject.toml`

Copy `example.env` to `.env` and update the values.

## Usage:

Install pre-commit

```bash
pre-commit install
```

Create and edit the .env file

```bash
cp example.env .env
```

### Review the make comands avaialble

```bash
make help
```

For local development

```bash
make setup && make install-dev
```

Start Docker container - neccessary for testing

```
make build
```

Note: I am using a requirements.txt and requirements-dev.txt until I understand how to use `Flit` in a docker build. This may change soon, but for the moment neccessitates copying from pyproject to the requirement files.

## Contents:

It contains files and folders that I have found useful:

docs/

src/

  appname/

    adapters/

      db/

      migrations/

      repositories/

      services/

      unit_of_works/

      use_cases/

    configurator/

    domain/

tests/

.coveragerc

.dockerignore

.flake8

.gitignore

.pre-commit-config.yaml

docker-compose.yaml

example.env

LICENSE

Makefile

pyproject.toml

pytype.cfg

README.md
