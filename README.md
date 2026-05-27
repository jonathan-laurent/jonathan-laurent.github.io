# Personal Website

## Setup

```sh
brew install sass/sass/sass  # on MacOS
poetry install
```

## To generate and visualize

```sh
poetry run python -m generator build
poetry run python -m http.server --directory generated
```

## Generate a black and white version of a picture

```sh
poetry run python -m generator bw thumbnails/inhibition.png
```

## Deploy to GitHub Pages

This repository now includes a GitHub Actions workflow that builds the site
from `main` and deploys the generated static files to GitHub Pages.

1. Push this repository to GitHub.
2. In the repository settings, open Pages and set the source to `GitHub Actions`.
3. Push to `main`, or run the `Deploy GitHub Pages` workflow manually.

The published site will use the contents of the generated `generated/`
directory.