# Pathway Technologies Website

This repository holds the source for the pathway-technologies.com website

See the documentation folder for more details

The Pathway Technologies website is written using Jekyll and hosted on GitHub.

The website URL is https://pathway-technologies.github.io/ and https://pathway-technologies.com

## Quick Start

Open an interactive shell:

```bash
./devshell.sh
```

Start the development server with automatic rebuilds (run this command from within the `devshell`):

```bash
./serve.sh
```

The site will be available at: http://localhost:4000

Changes to source files are detected automatically and the site is rebuilt.

## Validate

Build and validate the site:

```
./check.sh
```

This performs a clean Jekyll build and reports any build errors.

## Production Build

Generate the final site:

```
./build.sh
```

The generated output is written to:

```bash
public/
```
