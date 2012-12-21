# Installing on BSD systems

To install git-flow on BSD systems, like FreeBSD. OpenBSD or NetBSD, 
follow these instructions:

	$ git clone git://github.com/petervanderdoes/gitflow.git

Then, you can install git-flow, using:

	$ sudo make install

By default, git-flow will be installed in /usr/local/bin. To change the prefix
where git-flow will be installed, simply specify it explicitly, using:

	$ sudo make prefix=/opt/local install

This will install git-flow in /opt/local/bin

## Post installation setup
git-flow depends on the availability of the command line utility `gexpr`, which may not be available in your BSD environment.  
Please use your favorite package manager to install `gexpr` found in `sysutils/coreutils`.
