### Tests and linter status:
[![my-check](https://github.com/maxheong54/php-project-48/actions/workflows/my-check.yml/badge.svg)](https://github.com/maxheong54/php-project-48/actions/workflows/my-check.yml)

### Prerequisites

* Linux, Macos, WSL
* PHP >=8.4
* Xdebug
* Make
* Git
  
### Install
```bash
git clone https://github.com/maxheong54/php-gendiff.git
cd php-gendiff
make install
```

### Project Description

This project is a command-line program designed to determine the differences between two data structures.

Features:
- Supports various input file formats: YAML and JSON.
- Generates reports in multiple formats: plain text, stylish, json.

### Example Usage:
```bash
# format plain
gendiff --format plain path/to/file.yml another/path/file.json

Property 'common.follow' was added with value: false
Property 'group1.baz' was updated. From 'bas' to 'bars'
Property 'group2' was removed

# format stylish
gendiff filepath1.json filepath2.json

{
  + follow: false
    setting1: Value 1
  - setting2: 200
  - setting3: true
  + setting3: {
        key: value
    }
  + setting4: blah blah
  + setting5: {
        key5: value5
    }
}

```

Demonstration of gendiff work: [Watch demo](https://asciinema.org/a/R0OfENOrV3kmPiYtJaPaDTcZc)
