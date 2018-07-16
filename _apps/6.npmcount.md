---
title: npm-downloads-count-cli
description: A simple command line tool to check number of downloads of your npm package.

logo:
- https://user-images.githubusercontent.com/24803604/40577428-0acee99c-6123-11e8-92cc-8e8efcbcfae8.jpg
previews:
  - https://user-images.githubusercontent.com/24803604/39419384-48704030-4c7d-11e8-8071-08c508a0da7a.gif
authors:
- knrt10

repository: npm-downloads-count-cli
githubUrl: https://github.com/knrt10/npm-downloads-count-cli/
---


# Install using npm

`npm i --global npm-downloads-count`

# Usage

`npmcount -h` to see commands you can use

**output**

```
Usage: npmcount [options] [command]

  Options:


    -h, --help                  output usage information

  Commands:

    package|p [options] <file>  Search file(s) and list them
```

To see counts commands

`npmcount p -h`

**output**

```
Usage: package|p [options] <file>

  List number of downloads of your package

  Options:


    -d, --lastDay      get last day counts
    -w, --lastWeek     get last week counts
    -m, --lastMonth    get last month counts
    -D, --date <date>  get counts for specific date, <date> format = YYYY-MM-DD
    -h, --help         output usage information
```

**Last day downloads**
- `npmcount p <packageName> -d`

**Last week downloads**
- `npmcount p <packageName> -w`

**Last month downloads**
- `npmcount p <packageName> -m`

**Particular date downloads**
- `npmcount p <packageName> -D <date>`
