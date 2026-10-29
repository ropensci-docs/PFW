# Update the Project FeederWatch Species Translation Table

This function downloads the latest species translation table from the
Project FeederWatch website and saves it to a local directory. If a
previous version exists in the local directory, the user will be asked
for confirmation before overwriting it. This ensures taxonomy can
readily be kept up to date annually, since it will only be manually
updated on the PFW website otherwise.

## Usage

``` r
update_taxonomy(user_dir = tools::R_user_dir("PFW", "data"))
```

## Arguments

- user_dir:

  Optional. A custom directory to write the translation table to. Using
  the default local directory is highly recommended.

## Value

A message confirming whether the update was successful.

## Examples

``` r
if (FALSE) { # interactive()
# Prompt a species translation table taxonomy update
update_taxonomy()
}
```
