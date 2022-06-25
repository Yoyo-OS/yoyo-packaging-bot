# yoyo-packaging-bot
YoyoOS packaging bot

## Bot dependencies

+ ``debootstrap`` to make chroot environment for ``yoyo-chroot-builder``
+ TODO: ``socat`` to get new command from outside (localhost only)
+ TODO: ``socat`` to get http requests from browser (for bot health)

## Bot autobuild policies

+ TODO: Read registed repository list from database
+ TODO: Refresh data from database every 5 minutes
+ TODO: Polling GitHub API and find new tags (and manually send new tag to the bot)
+ TODO: Clone repository and build with ``yoyo-chroot-builder`` or ``ycb``
+ TODO: Add new packages into local ``aptly`` repository
+ TODO: Shot a new snapshot everyday at 3:00 and publish it (and manually create and publish new snapshot at any time, but DO NOT use default snapshot name)

## IN-PROGRESS: yoyo-chroot-builder (ycb)

A package builder to build package in chroot environment, referenced some code from [``pbuilder``](https://wiki.ubuntu.com/pbuilder), to build package directly from upstream package (without generating debian source package), it need a ``yoyo-build.sh`` at the root of directory to instruct the build process in chroot environment.

As it depends on ``debootstrap``, you should install it before using ycb.

