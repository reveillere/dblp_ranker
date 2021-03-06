# DBLP and rankings 

It grabs DBLP and tries to find rankings (Core Ranks and Scimago)

## Install

    npm i

## Run

It needs at least two arguments: the target URL (DBLP page) and the output file (CSV)

    node dblpExtractor.js DBLP_URL -o CSV file

For example

    node dblpExtractor.js https://dblp.uni-trier.de/pers/b/Blanc_0001:Xavier.html -o xavier.csv

## Options
```
  -h, --help         Print this usage guide.
  -c, --cache        Use a local cache for the ranking.
  -o, --out file     The output file to generate.
  -p, --patch file   DBLP and Scimago rewriting rules for ranking queries.
                     Default value is *patch.json*
  --url url          URL of the target DBLP page.
```

## Patches

Some DBLP entries do not match *Core* or *Scimago* queries.
The `--patch` option allows to specify user-specific rewriting rules between a DBLP entry and its corresponding Core/Scimago query.
