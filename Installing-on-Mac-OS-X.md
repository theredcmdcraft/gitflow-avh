# Installing on Mac OS X

## Homebrew

In the works

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
    
## Post installation setup
Install GNU getopt via Homebrew:    

    brew install gnu-getopt.

Create a `~/.gitflow_export` with the content `FLAGS_GETOPT_CMD="$(brew --prefix gnu-getopt)/bin/getopt"`.

For git-flow versions prior to 1.4.0-dev.28  
Create a `~/.gitflow_export` with the content `alias getopt="$(brew --prefix gnu-getopt)/bin/getopt"`.

If you have installed GNU getopt through other means than Homebrew, substitute `$(brew --prefix gnu-getopt)/bin/getopt` with the location of the GNU getopt file.