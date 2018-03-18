[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

# Docker running PHP-FPM, Nginx, MySQL, Redis and Xdebug enabled

## This docker contains
- Nginx
- MySQL 5.7
- php-7.1 fpm with Xdebug enabled
- Composer
- Git
- Curl
- Redis

### Libs enabled with PHP
- tokenizer
- iconv
- mbstring
- xdebug
- libxml
- pcntl

### Ports configuration

| Server     | Port |
|------------|------|
| Nginx      | 80   |
| MySQL      | 4306 |
| Redis      | 6379 |

---

## Using

You need docker-compose installed to run. Execute the commands below:

```sh
$ docker-compose build nginx mysql php redis
$ docker-compose up -d nginx mysql redis
```

Finally open http://localhost/ and see everything working! 👍

## Folder tree

The folder organization of your project should look like this:
*You can change this if you want* 

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
