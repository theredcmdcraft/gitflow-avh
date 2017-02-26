# Installing on Mac OS X

## Homebrew

Easy as Homebrew itself is:

### Stable release
    brew install git-flow-avh

### Development release
    brew install git-flow-avh --HEAD

### Post installation setup
As per version 1.7.0 there is no need for any post installation setup.
If you upgraded from an earlier version you can remove `export FLAGS_GETOPT_CMD="$(brew --prefix gnu-getopt)/bin/getopt"` 
from the file `~/.gitflow_export`.

For git-flow prior to 1.7.0

Create a `~/.gitflow_export` with the content `export FLAGS_GETOPT_CMD="$(brew --prefix gnu-getopt)/bin/getopt"`.

## wget

Even using wget its a one line effort.

### Stable release
    wget --no-check-certificate -q -O - https://github.com/petervanderdoes/gitflow-avh/raw/develop/contrib/gitflow-installer.sh install stable| sudo bash

### Development release
    wget --no-check-certificate -q -O - https://github.com/petervanderdoes/gitflow-avh/raw/develop/contrib/gitflow-installer.sh install develop| sudo bash

## curl

wget: command not found?  curl is only one as well!

### Stable release
    curl -sL https://github.com/petervanderdoes/gitflow-avh/raw/develop/contrib/gitflow-installer.sh | sudo bash -s install stable

### Development release
    curl -sL https://github.com/petervanderdoes/gitflow-avh/raw/develop/contrib/gitflow-installer.sh | sudo bash -s install develop
    
## Post installation setup
Install GNU getopt via Homebrew:    

    brew install gnu-getopt.

Create a `~/.gitflow_export` with the content `export FLAGS_GETOPT_CMD="$(brew --prefix gnu-getopt)/bin/getopt"`.

For git-flow versions prior to 1.4.0-dev.28  
Create a `~/.gitflow_export` with the content `alias getopt="$(brew --prefix gnu-getopt)/bin/getopt"`.

If you have installed GNU getopt through other means than Homebrew, substitute `$(brew --prefix gnu-getopt)/bin/getopt` with the location of the GNU getopt file.