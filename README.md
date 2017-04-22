imdock-cnp56
====================================================

## What's this:

Centos(Nginx + PHP5.6)

  * you can easy install PHP Framework (ex: Laravel)

  * you can use xdebug mode by PHPStorm(2016.2 or latest)

  * this project use management by docker-compose
  
  * you can use this for Laravel-5 PHP Framework

    
## How to install:

    ~ $ mkdir {project-name}
    ~ $ cd {project-name}
    ~/{project-name} $ git clone https://github.com/imagine10255/imdock-cnp56.git
    ~/{project-name} $ cd imdock-cnp56
    
    # change your custom settting (container_name: {project-name})
    ~/{project-name}/imdock-cnp56 $ vim ./docker-compose-yml      
    ~/{project-name}/imdock-cnp56 $ docker-compose up
    
    # open browser, testing your host-ip, see the phpinfo is success! ctrl+c close this
    # now, you can move the your project to website dir
    
    ~/{project-name}/imdock-cnp56 $ cp ./sites-enable/default.vhost.sample ./sites-enable/default.vhost
    
    # setting your custom nginx config (volumes: ./website:/var/www → ../{project-dir}:/var/www)
    ~/{project-name}/imdock-cnp56 $ vim ./docker-compose-yml
    ~/{project-name}/imdock-cnp56 $ vim ./default.vhost
    ~/{project-name}/imdock-cnp56 $ docker-compose up -d


```txt
{project-name}
├── imdock-cnp56
│   ├── conf/
│   ├── sites-enable/(nginx website setting)
│   ├── sites-module/
│   └── website(sample phpinfo)
└── {project-dir}
    └── ...
```
            
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
