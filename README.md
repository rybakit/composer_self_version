# composer_self_version

```bash
git clone https://github.com/rybakit/composer_self_version.git
cd composer_self_version/app

export COMPOSER_ROOT_VERSION=dev-$(git rev-parse --abbrev-ref HEAD)
echo COMPOSER_ROOT_VERSION=$COMPOSER_ROOT_VERSION
composer -vvv update --no-suggest --prefer-dist --no-scripts

git checkout feature_branch

export COMPOSER_ROOT_VERSION=dev-$(git rev-parse --abbrev-ref HEAD)
echo COMPOSER_ROOT_VERSION=$COMPOSER_ROOT_VERSION
composer -vvv update --no-suggest --prefer-dist --no-scripts
```


Details: [https://github.com/composer/composer/issues/6625](https://github.com/composer/composer/issues/6625)
