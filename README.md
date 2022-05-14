# svg4web

svg4web is an SVG optimizer/cleaner that reduces the size of scalable vector graphics by optimizing structure and removing unnecessary data written in Python.

It can be used to create streamlined vector graphics suitable for web deployment, publishing/sharing or further processing.

The goal of svg4web is to output a file that renderes identically at a fraction of the size by removing a lot of redundant information created by most SVG editors. Optimization options are typically lossless but can be tweaked for more agressive cleaning.

svg4web is open-source and licensed under [Apache License 2.0](https://github.com/codedread/svg4web/blob/master/LICENSE).

svg4web was originally developed by Jeff "codedread" Schiller and Louis Simard in in 2010.
The project moved to GitLab in 2013 an is now maintained by Tobias "oberstet" Oberstein and Patrick "Ede_123" Storz.

## Installation

svg4web requires [Python](https://www.python.org) 2.7 or 3.4+. Further, for installation, [pip](https://pip.pypa.io) should be used.

To use the svg4web:
- download
- unzip
- run

```console
todo
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
