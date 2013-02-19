# Installing on Linux, Unix, etc.

Under *nix, the easiest way to install git-flow is using Rick Osborne's
excellent git-flow installer, which can be run using the following command:

For the develop version:

	$ wget --no-check-certificate -q  https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh && bash gitflow-installer.sh install develop; rm gitflow-installer.sh

For the stable release:

	$ wget --no-check-certificate -q  https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh && bash gitflow-installer.sh install stable; rm gitflow-installer.sh
