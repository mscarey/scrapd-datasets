# Data sets

Traffic fatality datasets for Austin, TX.

## Data availability

The traffic fatality reports pusblished by APD are hosted on their website for 2 years. Past this point they are
archived and are not publicly accessible anymore.

## Raw data sets

The data sets named `fatalities-{year}-raw.json` are generated directly from `ScrAPD` without any manual intervention.

The only exception is when merging data that is not available publicly anymore (see details in the section above) and
cannot be retrieved by `ScrAPD`.

## Enhanced data sets

The data sets named `fatalities-{year}-enhanced.json` are datasets that have been enhanced, manually or automatically,
in order to improve the quality of the data. Data from other sources may also have been included in these data sets.

## "all" data sets

The data sets whose year is `all` are a combination of all the dataset of the same category.

There are generated using the following `jq` command:

```bash
jq -s add fatalities-201{7..9}-raw.json > fatalities-all-raw.json
```
