# Import Project FeederWatch Data

This function reads all .csv files downloaded from the Project
FeederWatch website, either from the default "data-raw/" folder created
by pfw_download() or from a user-specified folder. Optionally, it can
apply filters like region, species, year, etc. .csv files for import can
be downloaded via pfw_download() or from the [Project FeederWatch
website](https://feederwatch.org/explore/raw-dataset-requests/).

## Usage

``` r
pfw_import(folder = NULL, filter = FALSE, ...)
```

## Arguments

- folder:

  The folder where Project FeederWatch data is stored. Default is
  "data-raw/" in a local directory.

- filter:

  Logical. If TRUE, applies filters using pfw_filter(). Default is
  FALSE.

- ...:

  Additional arguments passed to pfw_filter() for filtering (e.g.,
  region, species, year).

## Value

A combined and optionally filtered dataset containing all Project
FeederWatch data.

## Examples

``` r
if (FALSE) { # \dontrun{
# This example cannot be run without user-downloaded data! This data can
# be downloaded manually or with pfw_download().

# Import all downloaded data from the default folder ("data-raw")
data <- pfw_import()

# Import and filter for Washington checklists from 2023
data_filtered <- pfw_import(filter = TRUE, region = "Washington", year = 2023)
} # }
```
