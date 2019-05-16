# Student handbooks

## About

This repo contains Rmarkdown files which produce student handbooks the taught PG
programmes (excluding conversion).

## Editing

You can make small text changes live on this site, by following links to the
relevant Rmd file, and then using the edit button.

For larger edits, or to add new files or restructure, you will need to clone the
repository to your local drive.

When adding new Rmd files, make sure to reference them in the `_bookdown.yml`
file.

## Rebuilding the HTML

If editing in RStudio you can preview you edits using the "Build book" function,
and the html files will appear in `docs/`.

You can browse them there using the filesystem, but some things work better if
served via http so if you have python3 installed use:

```
cd <REPOSITORY ROOT DIRECTORY>
python -m http.server
```

And then browse recently rebuilt files at, <http://127.0.0.1:8000/docs/>

## Publishing

Files are published automatically using [gihub-pages](https://pages.github.com)
and Travis CI.

Each time you commit a change to github, Travis builds a new html version and
publishes them to the live website.

## TODO

-   Use this url to read-in deadlines data and make tables
    https://wam.psy.plymouth.ac.uk/admin/reporting/programme/6/deadlines/?format=csv
