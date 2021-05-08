# IaafPoints

PHP library to calculate IAAF scoring points of athletics and IAAF scoring
points for combined events. And some other evaluations of athletics results.

This package is used for the stats system of [Latvian Athletics Association](https://athletics.lv).

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Changelog](#changelog)
- [License](#license)

## Installation

Use composer:

```sh
composer require glaivepro/iaafpoints
```

## Usage

This package provides mutliple calculators that all provide the same interface.

```php
// Calculator and use-case specific options.
$options = [
	'gender' => 'm',
	'venueType' => 'outdoor',
	'discipline' => '200m',
];

// Create a calculator instance
$calculator = new \GlaivePro\IaafPoints\IaafCalculator($options);

// Evaluate a result getting some points or a class assigned to result.
$points = $calculator->evaluate(21.61);
// 980

// Update options
$calculator->setOptions(['gender' => 'f']);
$points = $calculator->evaluate(21.61);
// 1279
```

See [docs](docs) for more details.

## Changelog

It's [here](CHANGELOG.md).

## License

This package is licensed under the [MIT license](LICENSE.md).
