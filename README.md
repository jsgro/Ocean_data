# Directory Hierarchy

This is a toy dataset to explore directory hierarchy and organization, or finding files.

This is useful with the (bash) commands: `tree`, `ls -lR`, `find`.

***Data files are empty*** (created with `touch`) and their filename extenstion reflect the text from NOAA page [sevenseas.html](https://oceanservice.noaa.gov/facts/sevenseas.html) which is included in the SevenSeas directory as `sevenseas.txt`.

Directory `/data` contains the material in native and compressed archives.

There are 40 directories in total, organized the following main directories named by narrative of the text (*e.g.* "In Greek literature", "In Medieval European literature".)

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
