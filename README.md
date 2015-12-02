## Laravel wkhtmltopdf installer

HTML to PDF converter. This package provides the 'wkhtmltopdf' binaries for linux x86/amd64 and intel-based Mac OS.

It is intended to be used in conjunction with packages like **knplabs/knp-snappy** for pure php, or **barryvdh/laravel-snappy** for Laravel.
The objective is to provide the binaries, without installing any package in the system. Because of that, this package could take a while to download and install.

The intention is to save time when you don't have access to the deployement scripts, nor system administrative tools.

## Requirements

* Ruby

## Installation

Add the following to composer.json:
```
"ferpetrelli/laravel_wkhtmltopdf": "dev-master"
```

For now, until it's completely tested and functional, use the repository version.

```
"repositories": [
        {
            "type":"vcs",
            "url":"https://github.com/ferpetrelli/laravel_wkhtmltopdf"
        }
    ]
```

## Usage

A new ruby script 'wkhtmltopdf-script' will be put at 'vendor/bin'.
This script automatically detects which architecture you're using and runs the correct binary.

**As an example, let's use the package laravel-snappy**

Just publish the package configuration file (read laravel-snappy readme), and add the binary path like the following:

```php
return array(

    'pdf' => array(
        'enabled' => true,
        'binary' => base_path('vendor/bin/wkhtmltopdf-script'),
        'timeout' => false,
        'options' => array(),
    )

);

```

Then when you use the package it will automatically runs the correct wkhtmltopdf version for your system.

## Contributions

The ruby script is almost a copy/paste of the one contained in the ruby gem: 'wkhtmltoimg_binary'

## Contact

*All your contributions are welcome!!! Just make a pull request*

To get some help or give suggestions please contact the author.

## License

MIT License. Copyright 2015. Fernando Petrelli.



