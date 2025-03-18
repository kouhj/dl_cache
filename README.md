Cache of source files required for my OpenWRT SDK build 
============================================================================

> Overview

This project is just a cache of source files that will be downloaded by the SDK of [my Openwrt builder](https://github.com/kouhj/openwrt_builder).
It provides the fast storage for the source archives that will be downloaded to the CONFIG_DOWNLOAD_FOLDER folder to speed up the build process as some source files may take a long time from the package maintainer's original site.

## Main branch
The main branch only provides the README.


## Architecture-specific branches
Source archives are saved to the architecture-specific branches seprarately. These files are maintained by the dl_cache workflow action of the kouhj/openwrt_builder repo.

## Add a new architecutre
Run the following to manually create a branch for the NEW_ARCH architecture with an empty folder. Adding files is then performed by the dl_cache workflow action of the kouhj/openwrt_builder repo.
```
git checkout TEMPLATE_FOR_NEW_ARCH
git checkout -b <NEW_ARCH>
git push --all origin
```
