Installing on Windows
---------------------

For Windows users, [msysgit](http://code.google.com/p/msysgit/) is a good
starting place for installing git.

Cygwin
======

For Windows users who wish to use the automated install, it is suggested that you install [Cygwin](http://www.cygwin.com/)
first to install tools like `git`, `util-linux` and `wget` (with those three being packages that can be selected
during installation). Then simply run this command from a Cygwin shell in your `$HOME`:

	$ wget -q -O - --no-check-certificate https://github.com/nvie/gitflow/raw/develop/contrib/gitflow-installer.sh | bash

If you get the error "flags: FATAL unable to determine getopt version" error after 

	$ git flow init

you need to install the `util-linux` package using the Cygwin setup.


MSysGit
=======

Download and install `getopt.exe` from the [util-linux package](http://gnuwin32.sourceforge.net/packages/util-linux-ng.htm) into `C:\Program Files\Git\bin`. (Only `getopt.exe`, the others util-linux files are not used). Also install `libintl3.dll` from the Dependencies package, into the same directory. 

Clone the git-flow sources from GitHub:

	$ git clone --recursive git://github.com/nvie/gitflow.git
	$ cd gitflow

Run the `msysgit-install` script from a command-line prompt (you may have to
run it with "Full Administrator" rights if you installed msysgit with its
installer):

	C:\gitflow> contrib\msysgit-install.cmd
