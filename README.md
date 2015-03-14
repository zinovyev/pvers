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


    -h or --help        Print help message.

    -v or --version     Print pvers version.

    -l or --list        List locally installed PHP versions.

    -d or --delete      Remove locally installed PHP version (as root only).

    -i or --install     Install (only) PHP of given version (as root only).

    -s or --select      Select (only) PHP of given version (as root only).

    -vv or --verbose    Verbose output (show all warnings and errors).

*To install or select (if already installed) PHP of version 5.6.6 just type:*
```sh
$ pvers 5.6.6
```
As you see, if neither '-i', nor '-s' flag are declared, a package will be first installed (if not already) and then selected (linked). So you can easy skip both of this flags.

## Example

1) Install the latest PHP version:
```sh
$ sudo pvers latest
Downloading...
Extracting...
Configuring...
Compiling...
Applying php.ini...
Applying php-fpm.conf...
Successfully installed!
Linking...
Current PHP version is 5.6.6
```

2) You can find out which version is currently used by typing:
```sh
$ php -v
PHP 5.6.6 (cli) (built: Feb 26 2015 10:51:33) 
Copyright (c) 1997-2015 The PHP Group
Zend Engine v2.6.0, Copyright (c) 1998-2015 Zend Technologies
```

3) Now select another version:
```sh
$ sudo pvers 5.3
You are trying to install an old version of PHP. Its support is highly experimental. Really want to continue? [Y/n] Y
Linking...
Current PHP version is 5.3.29
```

4) You can find out which version is currently used by typing:
```
$ php -v
PHP 5.3.29 (cli) (built: Mar  1 2015 13:34:21) 
Copyright (c) 1997-2014 The PHP Group
Zend Engine v2.3.0, Copyright (c) 1998-2014 Zend Technologies
```

5) List all versions installed locally:
```sh
$ pvers -l
5.3.29 [*]
5.4.38
5.5.22
5.6.0
5.6.1
5.6.2
5.6.6
```