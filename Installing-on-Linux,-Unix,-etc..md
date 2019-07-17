# Installing on Linux, Unix, etc.

## Ubuntu

* **Ubuntu 18.04**: git-flow AVH edition is packaged with Ubuntu. You can install the last version of  git-flow AVH Edition using:
    ```
    $ sudo apt-get install git-flow
    ```

* **Previous versions of Ubuntu**: the official repositories for old versions of Ubuntu include *3+ year old versions* of the git-flow AVH edition. These repositories had been not updated ([#336](https://github.com/petervanderdoes/gitflow-avh/issues/336)). If you install the software using `apt-get install` you will obtain obsolete versions. Instead of that, please use the manual instructions below.

**NOTE:** There is a PPA with a more recent version of git-flow (the version 1.9.1) that you can use to install it on Ubuntu Precise (12.04), Trusty (14.04), Wily (15.10), Xenial (16.04). You may check the corresponding [Launchpad page](https://launchpad.net/~pdoes/+archive/ubuntu/gitflow-avh). However, instead of using that PPA and installing the software using `apt-get install`, you may use the manual installation to get the latest version.

---
## Manual Installation
Under *nix, the easiest way to install git-flow is using Rick Osborne's
excellent git-flow installer, which can be run using the following command:

For the develop version:

	$ wget -q  https://raw.githubusercontent.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh && sudo bash gitflow-installer.sh install develop; rm gitflow-installer.sh

Option for `cURL` downloading:

	$ curl --silent --location  https://raw.githubusercontent.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh --output ./gitflow-installer.sh

For the stable release:

	$ wget -q  https://raw.githubusercontent.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh && sudo bash gitflow-installer.sh install stable; rm gitflow-installer.sh
