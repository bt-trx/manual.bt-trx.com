# bt-trx Manual

This manual is [mkdocs](https://www.mkdocs.org/) based.

## Install mkdocs, mkdocs-material and pdf-export-plugin

```bash
python -m pip install -r requirements.txt
```

### Warning

Currently, this documentation only works with mkdocs 1.0.4 and mkdocs-material
4.6.3. Therefore, you might want to work in a Python virtualenv.

```bash
virtualenv --python==/usr/bin/python3 venv/
source venv/bin/activate
python -m pip install -r requirements.txt
python -m pip show mkdocs mkdocs-material
python -m mkdocs serve
```

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

## Generate PDF

Currently, the _mkdocs-pdf-export-plugin_ can't handle anchors, therefore it is
necessary to temporarily alter links containing anchors i.e. from
"(../PTT-Taste#soft-ptt)" to "(../PTT-Taste.md#soft-ptt)" to be able to generate
a PDF file.

```bash
export ENABLE_PDF_EXPORT=1
mkdocs build
```
