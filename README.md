# Directory Hierarchy

This is a toy dataset to explore directory hierarchy and organization, or finding files.

This is useful with the (bash) commands: `tree`, `ls -lR`, `find`.

***Data files are empty*** (created with `touch`) and their filename extenstion reflect the text from NOAA page [sevenseas.html](https://oceanservice.noaa.gov/facts/sevenseas.html) which is included in the SevenSeas directory as `sevenseas.txt`. (2022/08/01 [archive](http://web.archive.org/web/20220108105026/https://oceanservice.noaa.gov/facts/sevenseas.html).)

## Data

Archives to download:

| Archive link   | Archive format | Unarchive command |
|-----------------|------------|-----------------------|
| [**SevenSeas.tar.gz**](./data/SevenSeas.tar.gz)|  gzip tar | `tar xzvf SevenSeas.tar.gz` |   
| [**SevenSeas.zip**](./data/SevenSeas.tar.gz) | Zip  | `unzip SevenSeas.zip` |

*Note*: most computer may offer a GUI version instead, then just "double click". (gzip and Zip are 2 different formats.)

## Hierarchy

Unarchived directory hierarchy **`SevenSeas`** contains  40 directories in total, organized the following main directories named by narrative of the [sevenseas.html](https://oceanservice.noaa.gov/facts/sevenseas.html) text (*e.g.* "In Greek literature", "In Medieval European literature".)

```
.
└── SevenSeas
    ├── Greek
    ├── Mariners
    ├── Medieval_Europe
    ├── Modern
    └── Oceans
        └── Geographic
```

Each main directory will contain sub-directories with the file name of the ocean or sea from the text, itself containing filenames. For example:

```
SevenSeas
├── Greek
│   ├── Adriatic
│   │   ├── Adriatic_1.grk
│   │   ├── Adriatic_2.grk
│   │   └── Adriatic_3.grk
```

The filename extension is "***made up***" and does not mean anything.   
**FILES ARE EMPTY** and do not contain data.

## Useage

Find all directories containing the word "Atlantic" as case insentive search:

```
$ find .  -type d -iname "*atlantic*"

./SevenSeas/Medieval_Europe/Atlantic
./SevenSeas/Oceans/Geographic/Atlantic
./SevenSeas/Mariners/the_Atlantic
./SevenSeas/Modern/North_Atlantic
./SevenSeas/Modern/South_Atlantic
```
