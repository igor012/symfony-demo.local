.PHONY: help
PU  = /usr/bin/phpunit
PUV =  $(PU) -v
PHPCS = /usr/bin/phpcs -p


help:
		@echo "\n tests : Run tests whith $(PU)\n"
		@echo " cs: Execute code quality with $(PCS)\n"
		@echo " all: Run all at once\n"

all: tests phpcs

tests:
		@cd ../code/project; $(PUV) tests/Controller
		@cd ../code/project; $(PUV) tests/Command/AddUserCommandTest.php
		@cd ../code/project; $(PUV) tests/Utils

phpcs:
		@$(PHPCS) ../code/project/src/ || true