# Merge Site Metadata into Project FeederWatch Data

This function joins habitat and site metadata into Project FeederWatch
observation data using the site description file.If the site metadata
file is not found, it will be downloaded automatically to the designated
path or "data-raw" if no path is selected.

## Usage

``` r
pfw_sitedata(data, path)
```

## Arguments

- data:

  A Project FeederWatch dataset.

- path:

  File path to the site description .csv from
  https://feederwatch.org/explore/raw-dataset-requests/. If not
  specified, defaults to "data-raw/sitedata.csv".

## Value

The original dataset with site metadata merged in.

## Examples

``` r
if (FALSE) { # interactive()
# Download/loads the example dataset
data <- pfw_example

# Merge site metadata into example observation data
data_sites <- pfw_sitedata(data, "data-raw/site_data.csv")
}
```
