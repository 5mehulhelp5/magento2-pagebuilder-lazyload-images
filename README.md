# Page Builder Lazyload Images for Magento 2 (SISL fork)

Adds the native browser `loading="lazy"` attribute to images inserted through Magento 2
Page Builder — deferring off-screen images so they don't block the initial render. A small,
zero-config win for **LCP** and overall Core Web Vitals. Can be toggled per image.

Maintained fork of `develodesign/magento-module-pagebuilder-lazyload-images`, verified on
**Magento 2.4.9 / PHP 8.4**.

## What changed vs upstream

- Added `require` to composer.json (`php` 8.1–8.5, `magento/framework >=103.0.4 <104`).
  The original declared no requirements, so Composer would install it on any incompatible
  version silently.

## Install

```bash
composer config repositories.lazyimg vcs https://github.com/SISL-source/magento2-pagebuilder-lazyload-images
composer require develodesign/magento-module-pagebuilder-lazyload-images:dev-main
bin/magento setup:upgrade
```

Then edit any Page Builder image and toggle lazy loading in the image settings.

## License

GPL-3.0 (upstream). Maintained by [SISL](https://sisl.pl) — one of a set of revived, free,
open-source Magento modules kept working on the latest releases.
