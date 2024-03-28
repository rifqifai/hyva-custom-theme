## Installation:


1. Install Swift Hyva https://github.com/icubebysirclo/swift-hyva

2. Add composer using this command in the root Magento project
```
composer config repositories.hyva-custom-theme git git@github.com:rifqifai/hyva-custom-theme.git
```
```
composer require rifqifai/hyva-custom-theme:dev-master
```

3. Full Deploy
```
rm -rf var/cache var/composer_home var/di var/generation var/page_cache var/session var/tmp var/view_preprocessed pub/static/* generated/* pub/static/frontend/* pub/static/_cache/merged pub/static/_requirejs pub/static/adminhtml && php bin/magento setup:upgrade && php bin/magento setup:di:compile && php bin/magento hyva:config:generate && php bin/magento setup:static-content:deploy en_US id_ID --jobs=5 -f && php bin/magento cache:clean && chmod -R 777 var/ pub/ generated/
```

4. Change Theme from Backoffice
