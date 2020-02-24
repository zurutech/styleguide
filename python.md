# Zuru Tech Python Style Guide

[![Code Style - Zuru](https://img.shields.io/badge/codestyle-zuru-red)](https://github.com/zurutech/styleguide)

This is the Python Style Guide we use enforce inside our Python projects.

**NOTE:** For all missing entries our baseline is the [Google Python Style Guide].

[Zuru Tech cookiecutter-pypackage] provides a ease to use [cookiecutter] template to
quickstart new Python projects in accordance with our guidelines.

- [Python Version](#python-version)
- [Project Structure](#project-structure)
- [Python Formatting](#python-formatting)
- [Testing](#testing)
- [Type annotations](#type-annotations)
- [Linting](#linting)
- [Documentation](#documentation)

## Python Version

Whenever possible we try to stick with the latest and greatest stable Python version
(currently 3.8).

## Project Structure

- Source code goes inside a `src` folder under the project top level directory.
- Sphinx source code goes inside a `docs/source` folder under the project top level directory.
- Tests source code goes inside in a `tests` folder under the project top level directory.
- Use [gitignore.io] to keep `.gitignore` consistent across projects.

## Python Formatting

- Formatting should **ALWAYS** be done with [black]
- Line Length is 90 characters and via [flake8-bugbear] we tolerate up to 100.
- Import should be formatted via [isort]

## Testing

- Our preferred testing framework is [pytest]
- We automate tests and other checks via [tox]
- When working with [Travis CI] we use [tox-travis] to automatically generate tests jobs
  for various Python version
- Test coverage is a good indicator. Use it wisely.
- Doctests are an awesome tool. Use them and adopt a DDD (Documentation Driven Development)
  approach to your development workflow. Default always to a TDD one when DDD is not feasible.

## Type annotations

- Type annotations are 99% of time an improvement even when no stubs are present for some
  libraries. Always write them down unless you have **REALLY** good reason not to.
- [mypy] is our go-to type checker

## Linting

- Preferred linter is [pylint]
- Minimum linter should be [flake8] coupled with [flake8-bugbear]

## Documentation

- Docstrings follows [Google Style Docstrings]
- [pydocstyle] and [doc8] are used to lint the documentation
- [Sphinx] is used as the documentation generator
- Docstring and files used by Sphinx must be written in [ReStructuredText]
- Always provide detailed API reference (this can be done quickly with Sphinx see
  [AshPy Docs] for an example)
- Provide a dependency graph of your objects

[AshPy Docs]: https://ashpy.zurutech.io/en/latest/write_the_docs.html
[black]: https://github.com/psf/black
[cookiecutter]: https://github.com/audreyr/cookiecutter
[doc8]: https://github.com/PyCQA/doc8
[flake8-bugbear]: https://github.com/PyCQA/flake8-bugbear
[flake8]: https://github.com/PyCQA/flake8
[gitignore.io]: https://www.gitignore.io/
[Google Python Style Guide]: https://google.github.io/styleguide/pyguide.html
[Google Style Docstrings]: https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html
[isort]: https://github.com/timothycrosley/isort
[mypy]: https://github.com/python/mypy
[pydocstyle]: https://github.com/PyCQA/pydocstyle
[pylint]: https://github.com/PyCQA/pylint
[pytest]: https://github.com/pytest-dev/pytest
[ReStructuredText]: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
[Sphinx]: https://sphinx-doc.org/
[tox-travis]: https://tox-travis.readthedocs.io/en/stable/
[tox]: https://testrun.org/tox/
[Travis CI]: https://travis-ci.org/
[Zuru Tech cookiecutter-pypackage]: https://github.com/zurutech/cookiecutter-pypackage
