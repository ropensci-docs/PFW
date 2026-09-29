# View Filter Attributes on Manipulated Project FeederWatch Data

This function allows users to view all filters they've applied to a
filtered Project FeederWatch dataset by printing its recorded filter
attributes in a readable format.

## Usage

``` r
pfw_attr(data)
```

## Arguments

- data:

  A filtered Project FeederWatch dataset.

## Value

A named list of applied filters.

## Examples

``` r
if (FALSE) { # interactive()
# Download/load example dataset
data <- pfw_example

# Filter for Dark-eyed Junco
filtered_data <- pfw_species(data, "Dark-eyed Junco")

# View filters applied to your active data
pfw_attr(filtered_data)
}
```
