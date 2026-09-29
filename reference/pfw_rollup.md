# Do Taxonomic Rollup on Project FeederWatch Data

This function removes spuhs, hybrids, and slashes and "demotes"
subspecies/subspecies intergrades to their parent species.

## Usage

``` r
pfw_rollup(data)
```

## Arguments

- data:

  A Project FeederWatch dataset.

## Value

A cleaned dataset with only species-level codes and a rollup attribute.

## Examples

``` r
# Download/load example dataset
data <- pfw_example

# Apply taxonomic rollup to an active PFW dataset
rolled_data <- pfw_rollup(data)
#> Taxonomic rollup complete. 116 ambiguous records removed.
```
