imdock-cnp56
====================================================

## What's this:

Centos(Nginx + PHP5.6)

  * you can easy install PHP Framework (ex: Laravel)

  * you can use xdebug mode by PHPStorm(2016.2 or latest)

  * this project use management by docker-compose
  
  * you can use this for Laravel-5 PHP Framework

    
## How to install:

    ~ $ git clone https://github.com/imagine10255/imdock-cnp56.git {your-project-name}
    ~ $ cd {your-project-name}
    
    # change your custom settting
    ~/{your-project-name} $ vim ./docker-compose-yml
    ~/{your-project-name} $ docker-compose up
    
    # open browser, testing your host-ip, see the phpinfo is success! ctrl+c close this
    # now, you can move the your project to website dir
    
    ~/{your-project-name} $ cp ./sites-enable/default.vhost.sample ./sites-enable/default.vhost
    
    # setting your custom nginx config
    ~/{your-project-name} $ vim ./default.vhost
    ~/{your-project-name} $ docker-compose up -d
            
            
## How to and other docker-compose use the same network :

    #if you not have group network, you can create this, and other docker-compose use this network setting
    ~ $ docker network create --driver bridge imdockgroup
    
    
## How to change setting:

  * You just look at this directory you will understand (config/*)
    
  * When the settings are complete, restart the container
    
## PHP Extend:
- [x] PHP5.6
  - [x] mbstring
  - [x] mcrypt
  - [x] php-dom, php-domxml, php-wddx, php-xsl
  - [x] php-mysqli, php_database
  - [ ] mongodb
  - [ ] redis
  - [ ] pgsql
  - [x] php-mssql
  - [x] php56w-pdo_sqlite, php56w-sqlite3
  - [ ] apcu
  - [x] gd
  - [ ] imap  
  - [x] imagick
  - [x] zend-opcache
  - [x] memcache
  - [x] xdebug
