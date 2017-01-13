# Laravel Package Start Toolkit


A simple toolkit to KickStart laravel package development.

## Quick Start

* Clone the github repo 

``` bash

git clone https:/github.com/shawnsandy/PkgStart myapp/packages/Vendor/PackageName

```


  
* CD into your new package dir and run `$ php prefill.php` in the command line. Follow the prompts to replace :author_name :author_username :author_website :author_email :vendor :package_name :package_description :psr4_namespace with their correct values package files, CHANGELOG.md, CONTRIBUTING.md, LICENSE.md, `/src/**.php` and composer.json files:  Delete the file prefill.php when done.

``` bash 

 php prefill.php
 
```

* Add the package to composer.json `psr-4` namespace

``` json

"psr-4": {
            "VendorName\\PackageName\\": "packages/VendorName/PackageName/src",
 },
            
```

* Go to config/app.php and add the package service provider

``` php

VendorName\PackageName\ServicesProvider::class,

```

  
Dump composer autoload

``` bash

composer dumpautoload

```


## Install via laravel-packager

Via Composer

``` bash 
    $ composer require jeroen-g/laravel-packager
```

Then add the service `jeroen-g/laravel-packager` provider in config/app.php:

``` bash
    JeroenG\Packager\PackagerServiceProvider::class,
```

Then run the following php artisan commands

```bash

php artisan packager:get https://github.com/shawnsandy/PkgStart MyVendor MyPackage

```

Got to config/app.php and find and replace (replace MyVendor/MyPackage with those you provided)

``` php

 Myvendor\MyPackage\MyPackageServiceProvider::class,
 
 ```
 with 
 
``` php

Myvendor\MyPackage\ServicesProvider::class,

```
  
* Follow the instructions on the following steps in the Quickstart section

    * Add the package to composer.json `psr-4` namespace

    * Go to config/app.php and add the package service provider
    
    * Dump composer autoload


__Build something awesome__

```

Go to `packages\MyVendor\MyPAckage` to and start coding your package, see [Laravel Packager](https://github.com/Jeroen-G/laravel-packager) for more info and options.


## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email shawnsandy04@gmail.com instead of using the issue tracker.

## Credits

- [shawn sandy](http://shawnsandy.com)


## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

