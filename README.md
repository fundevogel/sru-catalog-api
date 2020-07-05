# Catalog Fetcher

[![Latest Version](https://img.shields.io/github/release/libreja/sru-catalog-api.svg?style=flat-square)](https://github.com/libreja/sru-catalog-api/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/libreja/sru-catalog-api/master.svg?style=flat-square)](https://travis-ci.org/libreja/sru-catalog-api)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/libreja/sru-catalog-api.svg?style=flat-square)](https://scrutinizer-ci.com/g/libreja/sru-catalog-api/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/libreja/sru-catalog-api.svg?style=flat-square)](https://scrutinizer-ci.com/g/libreja/sru-catalog-api)
[![Total Downloads](https://img.shields.io/packagist/dt/league/skeleton.svg?style=flat-square)](https://packagist.org/packages/league/skeleton)

This repository fetches serveral (mostly German) catalogs and converts the entries to an array

Please use with caution, happy to invite new contributors.

## Install

Via Composer

``` bash
$ composer require libreja/sru-catalog-api
```

## Usage

Currently you may choose from 5 services
* ```gvk``` Gemeinsamer Verbundkatalog
* ```bvb``` Bibliotheksverbund Bayern
* ```swb``` Südwestdeutscher Bibliotheksverbund Baden-Württemberg, Saarland, Sachsen
* ```loc``` Library of Congress
* ```dnb``` Deutsche Nationalbibliothek

``` php
use Libreja\SruCatalog;
$sruCatalog = new SruCatalog\CatalogMain();
$sruCatalog->service = "dnb";
var_dump($sruCatalog->parse([
  "title" => 'Meier',
]));
```
## Services

(can be generated by ```php tests/supportByService.php```)

| key | German-trans | gvk | bvb | dnb | swb | loc |
|-|-|-|-|-|-|-|
| all | Alles | x |  | x |  | x |
| title | Titel | x | x | x | x | x |
| author | Autor | x | x | x | x | x |
| subject | Stichwort | x | x | x | x | x |
| idn | Identifikationnr des Katalogs (ppn) | x | x | x | x | x |
| isxn | ISXN | x | x | x | x | x |
| isbn | ISBN | x | x |  |  | x |
| issn | ISSN | x |  |  |  | x |
| publisher | Verleger/Firma | x |  | x |  |  |
| publisherPlace | Verleger Ort | x |  | x |  |  |
| year | Jahr | x |  | x | x |  |
| language | Sprache | x |  | x |  |  |
| corporation | Körperschaft | x |  | x |  | x |m

## Testing

``` bash
$ vendor/bin/phpunit tests/TestAllServices.php
```

## Contributing

Please contact us

## Credits

- Libreja (https://www.libreja.de/)
- Martin Schibel (https://github.com/mshd)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
