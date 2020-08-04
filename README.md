Project Info
============

Minimum example repo to reproduce the bug in https://github.com/UnitedIncome/serverless-python-requirements/issues/437.


Requirements
------------
* Yarn - https://yarnpkg.com/
* Poetry - https://python-poetry.org/


Setup
-----

```
$ yarn install
$ poetry install
```


Steps to reproduce bug
----------------------

```
$ yarn sls package
$ du -h  .serverless/serverless-python-requirements-issue-437.zip
```

It will return
```
8.0M	.serverless/serverless-python-requirements-issue-437.zip
```

Unzipping that above ZIP file for inspection shows all files (`__pycache__` and `dist-info` directories as well as `.pyc` and `.pyo` files).
