# Scour

[![PyPI](https://img.shields.io/pypi/v/svg4web.svg)](https://pypi.python.org/pypi/svg4web "Package listing on PyPI")
 
[![Build status](https://img.shields.io/travis/svg4web-project/svg4web.svg)](https://travis-ci.org/svg4web-project/svg4web "Build status (via TravisCI)")
[![Codecov](https://img.shields.io/codecov/c/github/svg4web-project/svg4web.svg)](https://codecov.io/gh/svg4web-project/svg4web "Code coverage (via Codecov)")

---

Scour is an SVG optimizer/cleaner that reduces the size of scalable vector graphics by optimizing structure and removing unnecessary data written in Python.

It can be used to create streamlined vector graphics suitable for web deployment, publishing/sharing or further processing.

The goal of Scour is to output a file that renderes identically at a fraction of the size by removing a lot of redundant information created by most SVG editors. Optimization options are typically lossless but can be tweaked for more agressive cleaning.

Scour is open-source and licensed under [Apache License 2.0](https://github.com/codedread/svg4web/blob/master/LICENSE).

Scour was originally developed by Jeff "codedread" Schiller and Louis Simard in in 2010.
The project moved to GitLab in 2013 an is now maintained by Tobias "oberstet" Oberstein and Patrick "Ede_123" Storz.

## Installation

Scour requires [Python](https://www.python.org) 2.7 or 3.4+. Further, for installation, [pip](https://pip.pypa.io) should be used.

To install the [latest release](https://pypi.python.org/pypi/svg4web) of Scour from PyPI:

```console
pip install svg4web
```

To install the [latest trunk](https://github.com/codedread/svg4web) version (which might be broken!) from GitHub:

```console
pip install https://github.com/codedread/svg4web/archive/master.zip
```

## Usage

Standard:

```console
svg4web -i input.svg -o output.svg
```

Better (for older versions of Internet Explorer):

```console
svg4web -i input.svg -o output.svg --enable-viewboxing
```

Maximum scrubbing:

```console
svg4web -i input.svg -o output.svg --enable-viewboxing --enable-id-stripping \
  --enable-comment-stripping --shorten-ids --indent=none
```

Maximum scrubbing and a compressed SVGZ file:

```console
svg4web -i input.svg -o output.svgz --enable-viewboxing --enable-id-stripping \
  --enable-comment-stripping --shorten-ids --indent=none
```
