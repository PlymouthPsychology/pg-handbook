# Student handbooks

## TODO

-   Use https://wam.psy.plymouth.ac.uk/admin/reporting/programme/6/deadlines/?format=csv

## About

Rmd files to produce student handbooks for UG and PG programmes (at present, only the MSc PRM).

Shared content is included across multiple programmes from the `common/` directory.

These `Rmd` files and other assets are not shared publically.

HOWEVER, the contents of `docs/` is visible here: <http://docs.psy.plymouth.ac.uk/>

## Editing a handbook

Each programme handbook has a separate subdirectory, and an RStduio project file and `_bookdown.yml` and `_config.yml` specfic to that programme.

To work on a handbook:

Open `<PROGRAMME>/handbook-project.Rproj` in RStudio

Edit files in that directory, adding assets which might be resued across programmes to `../static/`. Rmarkdown content which will be re-used across programmes should be saved in `../common/`.

## Rebuilding the HTML

As above, you can rebuilt in RStudio. If you prefer, you can instead

```
cd <PROGRAMME SUBDIRECTORY>
R --vanilla < _render
```

## Previewing changes locally

HTML files are built into `staging/` for review. You can browse them there using the filesystem, but some things work better if served via http so if you have python3 installed use:

```
cd <REPOSITORY ROOT DIRECTORY>
python -m http.server
```

And then browse recently rebuilt files at, <http://127.0.0.1:8000/staging/>

> NOTE that we serve from the root of the repo directory to ensure that the `static/` files are served too (which are one directory above the PRM files, because shared).

## Publishing

Files are published using [gihub-pages](https://pages.github.com) which just takes everying in the `docs` directory of a repository and serves it over http on the github.io domain.

To publish revisions of the docs run the following commands (e.g. here for the `PRM` subdirectory)

```
cp -r staging/ docs/
git add docs/
git commit docs/ -m "published latest changes to docs"
git push
```
