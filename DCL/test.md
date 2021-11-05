# laravel

## install the Laravel Installer as a `global Composer` dependency on linux:

```bash
$ composer global require laravel/installer
```

**membuat path default composer**
```bash
$ export PATH="~/.config/composer/vendor/bin:$PATH" 
```
**lanjut insall laravel global**
```bash
$ laravel new example-app
$ cd example-app
$ php artisan serve
```

## jika muncul keterang error
`Installation failed, reverting ./composer.json to its original content.`
```bash
$ sudo apt-get install php7.0-curl
```
```php
echo 'test';
```

## sumber
* [panduan git & github](https://github.com/datascienceid/panduan-github/edit/master/README.md)
