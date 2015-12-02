## Laravel wkhtmltopdf installer

HTML to PDF converter. This package provides the binaries for linux x86/amd64 and intel-based Mac OS.

It is intended to be used in conjunction with packages like knplabs/knp-snappy for pure php, or barryvdh/laravel-snappy for Laravel.

## Requirements

* Ruby

## Installation

Add the following to composer.json:
```
"ferpetrelli/laravel_wkhtmltopdf": "dev-master"
```

And for now until it's completely tested and functional, use the repository.

```
"repositories": [
        {
            "type":"vcs",
            "url":"https://github.com/ferpetrelli/laravel_wkhtmltopdf"
        }
    ]
```

## Usage

A new ruby script 'wkhtmltopdf' will be set at 'vendor/bin', to be called by the installed packages.

**For Laravel. As an example, using the laravel-snappy package**

Just publish the configuration (read it's readme), and add:

```php
return array(

    'pdf' => array(
        'enabled' => true,
        'binary' => base_path('vendor/bin/wkhtmltopdf'),
        'timeout' => false,
        'options' => array(),
    )

);

```

## Contact

*All your contributions are welcome!!! Just make a pull request*

To get some help or give suggestions please contact the author.

## License

MIT License. Copyright 2015. Fernando Petrelli.



