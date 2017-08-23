# composer_self_version

```bash
export COMPOSER_ROOT_VERSION=dev-$$(git rev-parse --abbrev-ref HEAD)
composer -vvv update --no-suggest --prefer-dist --no-scripts
```
