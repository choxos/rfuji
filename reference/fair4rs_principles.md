# The FAIR Principles for Research Software (FAIR4RS).

The canonical FAIR4RS (sub)principles that rfair's software metrics (the
FRSM metric set, `metric_version = "0.7_software"`) operationalize.
Principle statements are reproduced from the FAIR4RS Principles version
1.0.

## Usage

``` r
fair4rs_principles(category = NULL)
```

## Arguments

- category:

  Optional filter: one or more of `"F"`, `"A"`, `"I"`, `"R"`.

## Value

A data frame with `id`, `category`, `statement` (the principle text),
and `explanation`. The four foundational F/A/I/R statements and the
source citation are attached as the `"foundational"` and `"source"`
attributes.

## References

Chue Hong, N. P., Katz, D. S., Barker, M., Lamprecht, A.-L., Martinez,
C., Psomopoulos, F. E., Harrow, J., Castro, L. J., Gruenpeter, M.,
Martinez, P. A., Honeyman, T., et al. (2022). FAIR Principles for
Research Software (FAIR4RS Principles) (1.0). Research Data Alliance.
[doi:10.15497/RDA00068](https://doi.org/10.15497/RDA00068)

## See also

[`fair_principles()`](https://choxos.github.io/rfair/reference/fair_principles.md)
for the data FAIR principles.

## Examples

``` r
fair4rs_principles()
#>      id category
#> 1    F1        F
#> 2  F1.1        F
#> 3  F1.2        F
#> 4    F2        F
#> 5    F3        F
#> 6    F4        F
#> 7    A1        A
#> 8  A1.1        A
#> 9  A1.2        A
#> 10   A2        A
#> 11   I1        I
#> 12   I2        I
#> 13   R1        R
#> 14 R1.1        R
#> 15 R1.2        R
#> 16   R2        R
#> 17   R3        R
#>                                                                                             statement
#> 1                                   Software is assigned a globally unique and persistent identifier.
#> 2    Components of the software representing levels of granularity are assigned distinct identifiers.
#> 3                               Different versions of the software are assigned distinct identifiers.
#> 4                                                           Software is described with rich metadata.
#> 5               Metadata clearly and explicitly include the identifier of the software they describe.
#> 6                                                        Metadata are FAIR, searchable and indexable.
#> 7             Software is retrievable by its identifier using a standardized communications protocol.
#> 8                                          The protocol is open, free, and universally implementable.
#> 9             The protocol allows for an authentication and authorization procedure, where necessary.
#> 10                            Metadata are accessible, even when the software is no longer available.
#> 11 Software reads, writes and exchanges data in a way that meets domain-relevant community standards.
#> 12                                           Software includes qualified references to other objects.
#> 13                        Software is described with a plurality of accurate and relevant attributes.
#> 14                                                  Software is given a clear and accessible license.
#> 15                                                   Software is associated with detailed provenance.
#> 16                                          Software includes qualified references to other software.
#> 17                                                Software meets domain-relevant community standards.
#>                                                                                                                                                                                                                                       explanation
#> 1                                                            The software is given an identifier that is globally unique (refers to only one object, even across systems) and persistent (long-lasting, and resolvable to the identified source).
#> 2                                                        Distinct components at different granularity levels (e.g. a library and a function within it) are given their own identifiers, with the relationships between them captured in metadata.
#> 3                                                                                               Each version of the software, or of a component, is assigned a distinct identifier, with the relationships between versions captured in metadata.
#> 4                                                               The software is described with rich metadata that is itself FAIR (F4), follows community standards, and uses controlled vocabularies, to support indexing, search, and discovery.
#> 5                                                                              The software's globally unique and persistent identifier is stated explicitly in its associated metadata, making the metadata-to-software association unambiguous.
#> 6                                                                               Metadata about the software are FAIR, readable by humans and machines, and can be published in or harvested by a registry, catalog, repository, or search engine.
#> 7                                                                                     Obtaining the software by its identifier uses a standardized communications protocol (such as HTTPS) and does not require specialized or proprietary tools.
#> 8                                                                    The communications protocol (including the identifier resolver) is open, with no restrictions on implementing it, and free, with no fees or licensing costs to implement it.
#> 9                                                                                    The protocol supports an authentication and authorization procedure where access conditions (for example licensing, payment, or privilege level) require it.
#> 10                                                                             Metadata describing the software remain accessible even after the software itself is no longer available, since metadata are cheaper to preserve and retain value.
#> 11 Software reads, writes, and exchanges data using data and metadata types, controlled vocabularies, and formats defined by domain-relevant community standards; where it interacts via APIs these should be documented and open where possible.
#> 12                                                 Software includes qualified references to the other (non-software) objects it interacts with, such as data, samples, or instruments, specified via identifiers and/or controlled vocabularies.
#> 13                                                            Software is described with a plurality of accurate and relevant attributes, including but going beyond license (R1.1) and provenance (R1.2), to enable the broadest possible reuse.
#> 14                         Software has a clear, accessible license, ideally machine-readable (for example via an SPDX identifier), that is recognized, minimizes license proliferation, and is compatible with the licenses of its dependencies.
#> 15                                                                          Software is associated with detailed provenance describing why and how it came to be, and who contributed what, when, and where, establishing authenticity and trust.
#> 16                                                        Software includes qualified references to the other software it is built upon (requirements, imports, libraries) needed to compile and run it, resolvable via the authoritative source.
#> 17                                         Software, including its documentation and license, meets domain-relevant community standards and coding practices (for example the package conventions of a programming language, such as CRAN for R).
fair4rs_principles("R")
#>     id category
#> 1   R1        R
#> 2 R1.1        R
#> 3 R1.2        R
#> 4   R2        R
#> 5   R3        R
#>                                                                     statement
#> 1 Software is described with a plurality of accurate and relevant attributes.
#> 2                           Software is given a clear and accessible license.
#> 3                            Software is associated with detailed provenance.
#> 4                   Software includes qualified references to other software.
#> 5                         Software meets domain-relevant community standards.
#>                                                                                                                                                                                                              explanation
#> 1                                    Software is described with a plurality of accurate and relevant attributes, including but going beyond license (R1.1) and provenance (R1.2), to enable the broadest possible reuse.
#> 2 Software has a clear, accessible license, ideally machine-readable (for example via an SPDX identifier), that is recognized, minimizes license proliferation, and is compatible with the licenses of its dependencies.
#> 3                                                  Software is associated with detailed provenance describing why and how it came to be, and who contributed what, when, and where, establishing authenticity and trust.
#> 4                                Software includes qualified references to the other software it is built upon (requirements, imports, libraries) needed to compile and run it, resolvable via the authoritative source.
#> 5                 Software, including its documentation and license, meets domain-relevant community standards and coding practices (for example the package conventions of a programming language, such as CRAN for R).
```
