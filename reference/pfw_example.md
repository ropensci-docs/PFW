# Example Project FeederWatch Dataset

A sample dataset for demonstration and testing purposes. This dataset
includes data from 2020 - May 2024 from Washington and Oregon.

## Usage

``` r
pfw_example
```

## Format

A data frame with 556,814 rows and 24 columns.

## Source

Created using
[`pfw_download()`](https://docs.ropensci.org/PFW/reference/pfw_download.md)
and
[`pfw_import()`](https://docs.ropensci.org/PFW/reference/pfw_import.md)
in data-raw/pfw_example.R

## Examples

``` r
# Load the example data into the environment
data(pfw_example)

# Assign the example dataset
testing_data <- pfw_example
```
