Docker From php:5.6.8-fpm 

Included libraries: 

 * iconv
 * mcrypt
 * mbstring
 * gd

# Docker compose usage

Add to your docker-compose.yml file following:

```
phpfpm: 
  command: php-fpm --allow-to-run-as-root
  image: torniker/phpfpm
  volumes:
    - fpm.conf:/usr/local/etc/php-fpm.conf
    - php.ini:/usr/local/etc/php/php.ini
    - /your/path/to/prject:/var/www/html
  privileged: true
```

you can find samples for fpm.conf and php.ini on following urls:

php.ini - [https://gist.github.com/torniker/27472db39a623fe95a2c](https://gist.github.com/torniker/27472db39a623fe95a2c)
fpm.conf - [https://gist.github.com/torniker/e5192a3e42b4d72092ca](https://gist.github.com/torniker/e5192a3e42b4d72092ca)

