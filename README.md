# yoyo-packaging-bot

## yoyo-pkg-bot

A automatically packaging bot, a client of yoyo-mirror-bot.

Rolling github repository tags and build ubuntu and debian packages in schroot environment.

No need any additional configuration of schroot, the bot will configure it automatically.

### Configuration

``config/config`` is the default configure file, and you can edit ``config/config_usr`` to overwite it.

``config/repos`` is the github repositories bot will scan, each line describes a github repository. The format of the lines are ``<github-user> <github-repo> <branch>``.

### Output packages

Packages will be output under ``/tmp/yoyo-pkg-bot/backup/debian_debs`` and ``/tmp/yoyo-pkg-bot/backup/ubuntu_debs``, and scp to remote server.

### Dependencies

+ jq
+ git (configure api key and ssh key in ``config/config``)
+ debootstrap (configure suite and mirror in ``config/config``)
+ schroot (will be configured automatically)
+ scp (configure scp remote host in ``config/config``)
+ gotify (bot will send notifications to a gotify server configured in ``config/config``)

## yoyo-mirror-bot

A bot to add new packages into mirror and sync mirrors automatically, a server of yoyo-pkg-bot.

``config/mirror_config`` is the default configure file, and you can edit ``config/mirror_config_usr`` to overwite it.

Use nginx proxy ``yoyo-mirror-bot`` to make a https server.

## yoyo-chroot-builder

A script to run [pbuilder](https://pbuilder-team.pages.debian.net/pbuilder/) scripts.

But not have been used in fact.

## yoyo-repo-syncer

Automatically sync repo to and from different cloud storage providers with [Rclone](https://github.com/rclone/rclone).

