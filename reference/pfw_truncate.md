# Filter Project FeederWatch Data to "Standard" Seasonal Window

Project FeederWatch's Data Users Guide
(https://birdscanada.github.io/BirdsCanada_PFW/Start2.html) Suggests
that data should be truncated by date to avoid biases from years where
the Project FeederWatch survey season was extended. This function
filters data to include only observations within the typical FeederWatch
season: after November 8 and before April 3.

## Usage

``` r
pfw_truncate(data)
```

## Arguments

- data:

  A Project FeederWatch dataset with Year, Month, and Day columns.

## Value

A filtered dataset limited to Nov 8 – Apr 3 across years.

## Examples

``` r
# Download/load example dataset
data <- pfw_example

# Truncate an active PFW dataset to November 8 - April 3
truncated_data <- pfw_truncate(data)
#> Data filtered to standard PFW season window.
```
