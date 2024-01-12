all: html pdf

html: all-index-html user-manual-html user-modules-html
pdf: user-manual-pdf user-modules-pdf

all-index-html:
	python3 -msphinx -M html "all_index" "build"
	@echo "Build finished. The HTML pages are in build."
	@echo "User-index-html build finished; HTML is updated"

user-manual-html:
	rm -rf user_manual/_build/html/com
	pwd
	cd user_manual && make html
	@echo "User-manual-html build finished; HTML is updated"

user-manual-pdf:
	cd user_manual && make latexpdf
	@echo "User-manual-pdf build finished; PDF is updated"

user-modules-html:
	rm -rf user_modules/_build/html/com
	pwd
	cd user_modules && make html
	@echo "User-modules-html build finished; HTML is updated"

user-modules-pdf:
	cd user_modules && make latexpdf
	@echo "User modules build finished; PDF is updated"

icons-docs: clean-icons-docs
	cd build && sh get-server-sources.sh $(DRONE_BRANCH)
	cd build && composer install && composer update
	cd build && php generateIconsDoc.php

clean: clean-icons-docs
	rm -r _build user_manual/_build user_modules/_build

clean-icons-docs:
	rm -rf design/img/
