# Download Raw Project FeederWatch Data by Year

This function downloads raw data for selected years from the Project
FeederWatch website. It unzips the downloaded data and saves the .csv
files into a local folder (default: "data-raw/"), removing the zip files
afterward. It will download all files required to cover the
user-selected years.

## Usage

``` r
pfw_download(years, folder = NULL)
```

## Arguments

- years:

  Integer or vector of years (e.g., 2001, 2001:2023, c(1997, 2001,
  2023)). Data is available from 1998 to present.

- folder:

  The folder where Project FeederWatch data is stored. Default is
  "data-raw/" in a local directory.

## Value

Invisibly returns the downloaded files.

## Examples

``` r
if (FALSE) { # interactive()
# Download data from 2001-2006 into the default folder
pfw_download(years = 2001:2006)
}
```
