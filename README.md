# symfony-demo.local


**Nota Bene:**
> This stack was tested on Debian 10, Vagrant 2.2.5 and VirtualBox 6.0.14

> It should work on most GNU/Linux distributions and MacOS

## Vagrant stack

### Requirements
Install composer locally
```console
sudo apt install composer
```

Clone Symfony Demo Application
```console
git clone git@github.com:igor012/symfony-demo.local.git
#OR with https https://github.com/igor012/symfony-demo.local.git
```

Clone Symfony Demo Application into *symfony-demo.local/code*
```console
cd symfony-demo.local/code/
git clone git@github.com:symfony/demo.git project
#OR with https https://github.com/symfony/demo.git
cd project
composer install
```
Adapt /etc/hosts
```console
sudo echo "10.0.15.10 symfony-demo.local" >> /etc/hosts
```

### Deploy the stack
```console
vagrant up
```
When deployed you can access the URL http://symfony-demo.local/ or http://localhost:8080/

## Tests
Run Symfony demo's unit tests and quality tests
```console
cd tests/
make help
 tests : Run tests whith /usr/bin/phpunit

 cs: Execute code quality with PhpCS

 all: Run all at once

```