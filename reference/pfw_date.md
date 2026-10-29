# Filter Project FeederWatch Data by Month and/or Year

This function filters Project FeederWatch data by year and/or month,
allowing range-based filtering and wrapping months around new years.

## Usage

``` r
pfw_date(data, year = NULL, month = NULL)
```

## Arguments

- data:

  A Project FeederWatch dataset.

- year:

  Optional. Integer or vector of years (e.g. 2010 or 2010:2015).

- month:

  Optional. Integer or vector of months (1–12). Supports wrapping (e.g.
  c(11:2) = Nov–Feb).

## Value

A filtered dataset with date filter attributes.

## Examples

``` r
if (FALSE) { # interactive()
# Download/load example dataset
data <- pfw_example

# Filter by a single year
data_2021 <- pfw_date(data, year = 2021)

# Filter by multiple years
data_2123 <- pfw_date(data, year = 2021:2023)

# Filter by a single month
data_feb <- pfw_date(data, month = 2)

# Filter by a span of months
data_winter <- pfw_date(data, month = 11:2)

# Filter by both year and month
data_filtered <- pfw_date(data, year = 2021:2023, month = 11:2)
}
```
