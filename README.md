# yoyo-packaging-bot

## yoyo-pkg-bot

A automatically packaging bot.

Rolling github repository tags and build ubuntu and debian packages in schroot environment.

No need any additional configuration of schroot, the bot will configure it automatically.

### Configuration

``config/config`` is the default configure file, and you can edit ``config/config_usr`` to overwite it.

``config/repos`` is the github repositories bot will scan, each line describes a github repository. The format of the lines are ``<github-user> <github-repo> <branch>``.

### Output packages

Packages will be output under ``/tmp/yoyo-pkg-bot/backup/debian_debs`` and ``/tmp/yoyo-pkg-bot/backup/ubuntu_debs``

## Dependencies

+ jq
+ git
+ debootstrap
+ schroot

## yoyo-chroot-builder

A script to run [pbuilder](https://pbuilder-team.pages.debian.net/pbuilder/).

But not have been used in fact.

## yoyo-repo-syncer

Automatically sync repo to and from different cloud storage providers with [Rclone](https://github.com/rclone/rclone).

