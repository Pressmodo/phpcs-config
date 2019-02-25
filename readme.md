# Pressmodo PHPCS Configuration
Composer library to provide drop in installation and configuration of [WPCS](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards) and [PHPCompatibilityWP](https://github.com/PHPCompatibility/PHPCompatibilityWP), setting reasonable defaults for WordPress development with nearly zero configuration.

## Installation

Install the library via Composer:

```bash
$ composer require --dev pressmodo/phpcs-composer:dev-master
```

That's it!

## Usage

Lint your PHP files with the following command:

```bash
$ ./vendor/bin/phpcs .
```

If relying on Composer, edited the `composer.json` file by adding the following:

```json
"scripts": {
	"lint": [
		"phpcs ."
	],
}
```

Then lint via:

```bash
$ composer run lint
```

### IDE Integration

Some IDE integrations of PHPCS fail to register the `Pressmodo-Default` ruleset. In order to rectify this, place `.phpcs.xml.dist` at your project root:

```xml
<?xml version="1.0"?>
<ruleset name="Project Rules">
	<rule ref="pressmodo-Default" />
</ruleset>
```
