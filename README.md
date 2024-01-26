# A Hexagonal Quickstart Template

This is python, fastapi, postgres and docker quickstart template for Hexagonal Architecture projects.

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

This is an ongoing work in progress and is based on [Shako Rzayev's](https://github.com/ShahriyarR) hexagonal architecture repositories combined with [Python Alicante's](https://github.com/pythonalicante) meetup selector repository for docker setup.

Usage:

Pull down the files to your repo.

```
curl -sL https://github.com/davidjnevin/template-python-fastapi-docker-postgres/archive/master.zip -o repo.zip

```
Unzip the files and delete the repo.zip file.

Update the repo url in `pyproject.toml`.
Change 'appname' folder to the project name.
Change 'appname' to project name in `MakeFile` (migrations, migrate and run commands), `pyproject.toml`

Copy `example.env` to `.env` and update the values.
