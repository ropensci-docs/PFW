# Filter Project FeederWatch Data by Species

This function filters Project FeederWatch data to include only selected
species, with common names or scientific names via the species
translation table.

## Usage

``` r
pfw_species(data, species, suppress_ambiguous = FALSE)
```

## Arguments

- data:

  The Project FeederWatch dataset.

- species:

  A character vector of species names (common, scientific, or six-letter
  species code).

- suppress_ambiguous:

  (Optional, default = FALSE) TRUE/FALSE on including missing subspecies
  in the warning. This is just a silencer for the pfw_filter function.

## Value

A filtered dataset containing only the selected species.

## Examples

``` r
if (FALSE) { # interactive()
# Download/load example dataset
data <- pfw_example

# Filter for only Greater Roadrunner using the common name
data_GRRO <- pfw_species(data, "Greater Roadrunner")

# Filter for Lesser Goldfinch and American Goldfinch using scientific names
data_goldfinches <- pfw_species(data, c("Spinus psaltria", "Spinus tristis"))

# Filter for Dark-eyed Junco, Song Sparrow, and Spotted Towhee using species codes
data_masonsyard <- pfw_species(data, c("daejun", "sonspa", "spotow"))

# Filter with a pre-existing species list
species_list <- c("daejun", "sonspa", "spotow")
data_masonsyard <- pfw_species(data, species_list)
}
```
