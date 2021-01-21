# pass export

A pass extension that exports given passwords in csv format

## Description

_pass-export_ extends the pass with a export command thats exports (all/given) passwords in csv (+bitwarden) format to stdout. Also look here for other cool extensions: [awesome-password-store](https://github.com/tijn/awesome-password-store)!

## Usage

```
pass export 1.1 - A pass extension that exports (all/given) passwords in csv format

Usage:
    pass export [a | all] [b | bitwarden] [<pass-name> | <pass-dir>] [-v | --version] [-h | --help]
    Provide a command to export passwords in csv format

    Options:
    a, all                   Export all passwords
    b, bitwarden     Export in bitwarden CSV format
    -v, --version    Show version information.
    -h, --help               Print this help message and exit.

    More information may be found in the pass-export(1) man page.
```

## Installation

**From git**

```sh
git clone https://github.com/dvogt23/pass-export/
cd pass-export
sudo make install
```

**OS X**

```sh
git clone https://github.com/dvogt23/pass-export/
cd pass-export
make install PREFIX=/usr/local
```

**Requirements**

- `pass 1.7.0` or greater.
- If you do not want to install this extension as system extension, you need to enable user extension with `PASSWORD_STORE_ENABLE_EXTENSIONS=true pass`. You can create an alias in `.bashrc`: `alias pass='PASSWORD_STORE_ENABLE_EXTENSIONS=true pass'`

## Examples

_Export all passwords_

```
zx2c4@laptop ~ $ pass export a
```

_Export all passwords_ in bitwarden format

```
zx2c4@laptop ~ $ pass export a b
```

_Export a password dir_

```
zx2c4@laptop ~ $ pass export social
```

_Export a password entry_

```
zx2c4@laptop ~ $ pass export social/twitter.com
```

## Contribution

Feedback, contributors, pull requests are welcome.

## License

```
    Copyright (C) 2017

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
