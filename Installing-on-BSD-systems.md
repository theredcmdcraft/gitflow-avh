# Installing on BSD systems

To install git-flow on BSD systems, like FreeBSD. OpenBSD or NetBSD, 
follow these instructions:

	$ git clone git://github.com/petervanderdoes/gitflow.git

Then, you can install git-flow, using:

	$ sudo gmake install

By default, git-flow will be installed in /usr/local/bin. To change the prefix
where git-flow will be installed, simply specify it explicitly, using:

	$ sudo make prefix=/opt/local install

This will install git-flow in /opt/local/bin

## Post installation setup
Install GNU getopt

    cd /usr/ports/misc/getopt/
    sudo make install
    
This will install GNU `getopt` in `/usr/local/bin`