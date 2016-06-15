# Installing on Linux, Unix, etc.

## Ubuntu
git-flow AVH edition is packaged with Ubuntu. To install git-flow AVH Edition type `sudo apt-get install git-flow`.  

A PPA exists with the latest git-flow version for Ubuntu, backported from Ubuntu Xenial.
* Precise (12.04)
* Trusty (14.04)
* Wily (15.10)
* Xenial (16.04)

See the Launchpad page at [https://launchpad.net/~pdoes/+archive/ubuntu/gitflow-avh](https://launchpad.net/~pdoes/+archive/ubuntu/gitflow-avh)

## Manual
Under *nix, the easiest way to install git-flow is using Rick Osborne's
excellent git-flow installer, which can be run using the following command:

For the develop version:

	$ wget --no-check-certificate -q  https://raw.github.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh && sudo bash gitflow-installer.sh install develop; rm gitflow-installer.sh

For the stable release:

	$ wget --no-check-certificate -q  https://raw.github.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh && sudo bash gitflow-installer.sh install stable; rm gitflow-installer.sh
