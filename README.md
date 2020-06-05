# Catalog Fetcher

[![Latest Version](https://img.shields.io/github/release/libreja/sru-catalog-fetcher-php.svg?style=flat-square)](https://github.com/libreja/sru-catalog-fetcher-php/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/libreja/sru-catalog-fetcher-php/master.svg?style=flat-square)](https://travis-ci.org/libreja/sru-catalog-fetcher-php)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/libreja/sru-catalog-fetcher-php.svg?style=flat-square)](https://scrutinizer-ci.com/g/libreja/sru-catalog-fetcher-php/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/libreja/sru-catalog-fetcher-php.svg?style=flat-square)](https://scrutinizer-ci.com/g/libreja/sru-catalog-fetcher-php)
[![Total Downloads](https://img.shields.io/packagist/dt/league/skeleton.svg?style=flat-square)](https://packagist.org/packages/league/skeleton)

**Note:** Replace `skeleton` with the correct package name in the above URLs, then delete this line.

This is where your description should go. Try and limit it to a paragraph or two, and maybe throw in a mention of what
PSRs you support to avoid any confusion with users and contributors.

## Install

Via Composer

``` bash
$ composer require league/skeleton
```

## Usage

``` php
use Libreja\SruCatalog;
$sruCatalog = new SruCatalog\CatalogMain();
$sruCatalog->service = "dnb";
var_dump($sruCatalog->parse([
  "title" => 'Meier',
]));
```

## Testing

``` bash
$ phpunit
```

## Contributing

Please see [CONTRIBUTING](https://github.com/thephpleague/:package_name/blob/master/CONTRIBUTING.md) for details.

## Credits

- Martin Schibel (https://github.com/mshd)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
