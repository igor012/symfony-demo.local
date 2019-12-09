symfony-demo.local
===

# Vagrant stack

## Requirements
Install composer locally
```
sudo apt install composer
```

Clone Symfony Demo Application
```
git clone git@github.com:igor012/symfony-demo.local.git
```

Clone Symfony Demo Application into *symfony-demo.local/code*
```
cd symfony-demo.local/code/
git clone git@github.com:symfony/demo.git project
cd project
composer install
```
Adapt /etc/hosts
```
sudo echo "10.0.15.10 symfony-demo.local" >> /etc/hosts
```

## Deploy the stack
```
vagrant up
```
When deployed you can access the URL http://symfony-demo.local/ or http://localhost:8080/

# Tests
Run unit tests and quality tests
```
cd tests
make help
