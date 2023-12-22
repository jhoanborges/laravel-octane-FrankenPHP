# Laravel Octane and FrankenPHP

In the world of web development, speed of execution and optimal performance are essential. Laravel Octane is the revolutionary solution for optimizing the execution speed of Laravel PHP applications. This article will explore how Laravel Octane, leveraging the powerful application server like FrankenPHP, can accelerate the performance of your application by starting it once and keeping it in memory to respond to requests at supersonic speeds.

## Installation

```bash
composer install
```


```bash
php artisan octane:start
```
If you want to control the number of workers you can use the workers option:
```bash
php artisan octane:start --workers=2
```
##Test
```bash
# Concurrency 1 for 5 seconds...
./vendor/bin/pest stress http://127.0.0.1:8000

Swoole Medium Request Duration ........... 4.94 ms
RoadRunner Medium Request Duration ....... 2.61 ms
FrankenPHP Medium Request Duration ....... 0.88 ms

# Concurrency 8 for 5 seconds...
./vendor/bin/pest stress http://127.0.0.1:8000 --concurrency=8

Swoole Medium Request Duration ........... 5.39 ms
RoadRunner Medium Request Duration ....... 4.00 ms
FrankenPHP Medium Request Duration ....... 1.59 ms
```
## Credits

[https://dev.to/robertobutti/laravel-octane-and-frankenphp-240o](https://dev.to/robertobutti/laravel-octane-and-frankenphp-240o)
[[https://dev.to/robertobutti/laravel-octane-and-frankenphp-240o](https://blog.laravel.com/octane-frankenphp)]([https://dev.to/robertobutti/laravel-octane-and-frankenphp-240o](https://blog.laravel.com/octane-frankenphp)https://blog.laravel.com/octane-frankenphp)
