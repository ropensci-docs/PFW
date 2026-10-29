# Filter Project FeederWatch Data by Region

This function filters Project FeederWatch data to include only specified
states, provinces, or countries.

## Usage

``` r
pfw_region(data, regions)
```

## Arguments

- data:

  A Project FeederWatch dataset.

- regions:

  A character vector of regions (e.g., "Washington", "United States").

## Value

A filtered dataset containing only the selected regions.

## Examples

``` r
if (FALSE) { # interactive()
# Download/load example dataset
data <- pfw_example

# Filter for data only from Washington using the state name
data_WA <- pfw_region(data, "Washington")

# Filter for data only from Washington using the state code
data_WA <- pfw_region(data, "US-WA")

# Filter for data from Washington, Oregon,
# and California using the state name
data_westcoastbestcoast <- pfw_region(data, c("Washington", "Oregon", "California"))
}
```
