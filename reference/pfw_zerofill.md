# Zerofill Species not Detected in each Survey Instance for Analysis

This function adds zeros for checklists where selected species were
absent, setting HOW_MANY = 0 for presence/absence-based analyses. Note
that zerofilling entire, unfiltered datasets from Project FeederWatch
will take a long time!

## Usage

``` r
pfw_zerofill(data)
```

## Arguments

- data:

  A Project FeederWatch dataset, optionally filtered for species.

## Value

A dataset with zerofilled values included for each species.

## Examples

``` r
if (FALSE) { # \dontrun{
# This example cannot be run because it relies on a cached version of the
# data which is created upon using pfw_import(). Storing a version of this
# for the example dataset would be too large for CRAN!

# Zerofill a PFW  dataset
data_zf <- pfw_zerofill(data)
} # }
```
