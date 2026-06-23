# Canonical definition of the FAIR principle a metric maps to.

For data metrics (`FsF-*`) this returns the FAIR Guiding Principle
definition; for software metrics (`FRSM-*`) it returns the corresponding
FAIR4RS Principle statement (see
[`fair4rs_principles()`](https://choxos.github.io/rfair/reference/fair4rs_principles.md)).

## Usage

``` r
principle_definition(metric_identifier)
```

## Arguments

- metric_identifier:

  A metric identifier (e.g. "FsF-F1-01MD" or "FRSM-17-R1.2").

## Value

The principle's definition string, or `NA`.

## Examples

``` r
principle_definition("FsF-R1.1-01M")
#> [1] "(meta)data are released with a clear and accessible data usage license"
principle_definition("FRSM-17-R1.2")
#> [1] "Software is associated with detailed provenance."
```
