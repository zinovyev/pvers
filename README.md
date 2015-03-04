pvers
==========

*PHP version manager written in BASH. Easy to install and easy to use. Compile different versions of PHP and switch between them in a moment.*

## Installation
```sh
$ git clone https://github.com/zinovyev/pvers.git
$ sudo mv pvers/pvers /usr/bin/pvers
$ rm -rf pvers
```

## Usage

*pvers [ option ... ] [php-version]*


Where options are:


    -h or --help        Print helo message.

    -v or --version     Print pvers version.

    -l or --list        List locally installed PHP versions.

    -d or --delete      Remove locally installed PHP version (as root only).

    -i or --install     Install (only) PHP of given version (as root only).

    -s or --select      Select (only) PHP of given version (as root only).

    -vv or --verbose    Verbose output (show all warnings and errors).

*To install or select (if already installed) PHP of version 5.6.6 type:*
```sh
$ pvers 5.6.6
```