# bt-trx Manual

This manual is [mkdocs](https://www.mkdocs.org/) based.

## Install mkdocs, mtdocs material and rtd-dropdown theme

`python -m pip install mkdocs`

`python -m pip install mkdocs-material`

`python -m pip install mkdocs-rtd-dropdown`

**Important: Each file name needs to be the same as the first heading in each file.**

## View documentation locally

`mkdocs serve`

This command starts a local webserver at [localhost:8000](http://localhost:8000).

## Build static documentation files (HTML)

`mkdocs build`

This command builds the documentation in ./site/

## Deploy to Github Pages

`mkdocs gh-deploy`

Will build the static files and push to the gh-pages branch on Github, so they
will be served automatically at [manual.bt-trx.com](https://manual.bt-trx.com)
