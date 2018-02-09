# Docker PHP, MySQL, Nginx and Xdebug

## This docker contains
- Nginx
- MySQL 5.7
- php-7.1 fpm with Xdebug enabled
- Composer
- Git
- Curl

### Libs enabled with PHP
- tokenizer
- iconv
- mbstring
- xdebug
- libxml

### Ports configuration

| Server     | Port |
|------------|------|
| Nginx      | 80   |
| MySQL      | 4306 |

---

## Using

You need docker-compose installed to run. Execute the commands below:

```sh
$ docker-compose build nginx mysql php
$ docker-compose up -d nginx mysql
```

Finally open http://localhost/ and see everything working! 👍

## Folder tree

The folder organization of your project should look like this:

```sh
.
├── application
│   └── public
│       └── index.php
└── my-docker-php
```

## Xdebug

To use Xdebug edit `php-fpm71/php.ini` with your own local IP address in line 8:

```sh
xdebug.remote_host=YOUR_OWN_LOCAL_IP_ADDRESS
```
