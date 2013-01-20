# Installing on Windows

The below instructions are unsupported. The installation files need to be updated.

For Windows users, [msysGit]


## msysGit

msysGit allows multiple forms of installation, one which allows you to hack git and one that doesn't.

### Downloads that allow hacking
The downloads are called `Net installer if you want to hack on Git` and `Full installer (self-contained) if you want to hack on Git `
Follow the instructions on the [msysGit wiki](https://github.com/msysgit/msysgit/wiki/InstallMSysGit) to install git. Their preferred method is the Net Installer.

Download the [getopt binary archive](http://lrn.no-ip.info/other/mingw/mingw32/getopt/1.1.4-1/getopt-1.1.4-1-mingw32-bin.tar.lzma), extract the `getopt.exe`  and copy it in `C:\msysgit\bin` 

### Download that doesn't allow the hacking
The download is called `Full installer for official Git for Windows`.

Install the application and download the [getopt archive](http://bit.ly/T5ZMHE) which I created to make it a bit easier.
This archive contains all needed files. Extract the files and copy them in `C:\Program Files(x86)\Git\bin`

### Install git-flow
Clone the git-flow sources from GitHub:

	$ git clone git://github.com/petervanderdoes/gitflow.git
	$ cd gitflow

Run the `msysgit-install` script from a command-line prompt (you may have to
run it with "Full Administrator" rights if you installed msysgit with its
installer):

	C:\gitflow> contrib\msysgit-install.cmd

**Note**
This will not copy the example hook files, only the needed executables.

## Cygwin


For Windows users who wish to use the automated install, it is suggested that you install [Cygwin](http://www.cygwin.com/)
first to install tools like `git`, `util-linux` and `wget` (with those three being packages that can be selected
during installation). Then simply run this command from a Cygwin shell in your `$HOME`:

	$ wget -q -O - --no-check-certificate https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh | bash

If you get the error "flags: FATAL unable to determine getopt version" error after 

	$ git flow init

you need to install the `util-linux` package using the Cygwin setup.
