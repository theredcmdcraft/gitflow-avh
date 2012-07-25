# Installing git-flow manually

If you prefer a manual installation, please use the following instructions:

	$ git clone git://github.com/petervanderdoes/gitflow.git

Then, you can install `git-flow`, using:

	$ sudo make install

By default, git-flow will be installed in /usr/local. To change the prefix
where git-flow will be installed, simply specify it explicitly, using:

	$ sudo make prefix=/opt/local install

Or simply point your `PATH` environment variable to your git-flow checkout
directory.

*Installation note:*  
git-flow depends on the availability of the command line utility `getopt`,
which may not be available in your Unix/Linux environment.  Please use your
favorite package manager to install `getopt`.  For Cygwin, install the
`util-linux` package to get `getopt`.  If you use `apt-get` as your install
manager, the package name is `opt`.
