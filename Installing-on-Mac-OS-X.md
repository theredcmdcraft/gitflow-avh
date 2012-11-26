# Installing on Mac OS X

## Homebrew

Currently not supported as I don't have a MAC and can't create the brew formula.

## wget

Even using wget its a one line effort.

### Stable release
    wget --no-check-certificate -q -O - https://github.com/petervanderdoes/gitflow/raw/develop/contrib/gitflow-installer.sh install stable| sudo bash

### Development release
    wget --no-check-certificate -q -O - https://github.com/petervanderdoes/gitflow/raw/develop/contrib/gitflow-installer.sh install develop| sudo bash

## curl

wget: command not found?  curl is only two.  (Note that URL is where the above URL currently redirects.)

    curl https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh > gitflow-installer.sh
    chmod a+x gitflow-installer.sh

### Stable release
    sudo bash gitflow-installer.sh install stable

### Development release
    sudo bash gitflow-installer.sh install develop