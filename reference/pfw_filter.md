# Apply Multiple Filters to Project FeederWatch Data

This function filters Project FeederWatch data by species, region, and
data validity.

## Usage

``` r
pfw_filter(
  data,
  species = NULL,
  region = NULL,
  year = NULL,
  month = NULL,
  valid = TRUE,
  reviewed = NULL,
  rollup = TRUE
)
```

## Arguments

- data:

  A Project FeederWatch dataset.

- species:

  (Optional) A character vector of species names (common or scientific).

- region:

  (Optional) A character vector of region names (e.g., "Washington",
  "British Columbia").

- year:

  (Optional) Integer or vector of years (e.g., 2010 or 2010:2015).

- month:

  (Optional) Integer or vector of months (1–12). Supports wrapping
  (e.g., 11:2 = Nov–Feb).

- valid:

  (Optional, default = TRUE) Filter out invalid data. Removes rows where
  VALID == 0.

- reviewed:

  (Optional) If specified, filters by review status (TRUE for reviewed,
  FALSE for unreviewed).

- rollup:

  (Optional, default = TRUE) Automatically roll up subspecies to species
  level and remove spuhs, slashes, and hybrids.

## Value

A filtered dataset.

## Examples

``` r
if (FALSE) { # interactive()
# Download/load example dataset
data <- pfw_example

# Filter for Dark-eyed Junco, Song Sparrow, and Spotted Towhee in Washington in 2023
data_masonsyard <- pfw_filter(
  data,
  species = c("daejun", "sonspa", "spotow"),
  region = "US-WA",
  year = 2023
)

# Filter for all data from Washington, Oregon, or California from November
# through February for 2021 through 2023
data_westcoastwinter <- pfw_filter(
  data,
  region = c("Washington", "Oregon", "California"),
  year = 2021:2023,
  month = 11:2
)

# Filter for Greater Roadrunner in California, keeping only reviewed
# records and disabling taxonomic rollup
data_GRRO_CA <- pfw_filter(
  data,
  species = "Greater Roadrunner",
  region = "California",
  reviewed = TRUE,
  rollup = FALSE
)

# Filter for Fox Sparrow with rollup
rollFOSP <- pfw_filter(pfw_example, species = "Fox Sparrow", rollup = TRUE)
# Taxonomic rollup complete. 116 ambiguous records removed.
# 1 species successfully filtered.
# Filtering complete. 8070 records remaining.

# Filter for Fox Sparrow without rollup
norollFOSP <- pfw_filter(pfw_example, species = "Fox Sparrow", rollup = FALSE)
# 1 species successfully filtered.
# Filtering complete. 7745 records remaining.

# 116 records were identified to subspecies (e.g. "Fox Sparrow (Sooty)",
# listed as 'foxsp2' in SPECIES_CODE)
# These records are merged into the parent "Fox Sparrow" total with rollup,
# but excluded in favor of records only identified exactly as
# "Fox Sparrow" (no subspecies, only SPECIES_CODE = 'foxspa') if rollup = FALSE.
}
```
