# Laravel Web Push Example
A basic example of using webpush notifications with laravel and Javascript. Push Notifications are a part of Service Workers and It requires HTTPS unless you are using localhost.

## Running this web application
- make sure you have xampp or wamp installed if you are on windows machine, mamp for mac , and lamp for linux.

- clone this repository to your local machine or just download the zip.

- install [Composer](https://getcomposer.org/download) first, then run this command in your command-line (you should be inside your project directory). 
```bash
  composer install
```

- rename .env.example to .env and configure your database.

- generate application key.

```bash
    php artisan key:generate
```

- create tables by migrations.

```bash
    php artisan migrate
```

- Generate VAPID Keys (this command will place the VAPID keys in your .env file).
```bash
    php artisan webpush:vapid
```

- Add the VAPID public key to application server key in enable-push.js file located in public/js directory, here's the link to that [line](https://github.com/SagarMaheshwary/webpush-example/blob/0a0be26c038ea6de1289035c19bc715513340356/public/js/enable-push.js#L64)

- Start Laravel dev server.
```bash
    php artisan serve
```
- Read the entire tutorial [Push Notifications with Laravel and Webpush](https://medium.com/@sagarmaheshwary31/push-notifications-with-laravel-and-webpush-446884265aaa) on Medium.

- [Webpush](https://github.com/laravel-notification-channels/webpush) package is used by this app.