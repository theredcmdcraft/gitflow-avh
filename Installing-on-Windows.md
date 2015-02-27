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

Install the application and download the [getopt archive](http://bit.ly/T5ZMHE) which I created.
Extract the files and copy them in `C:\Program Files(x86)\Git\bin`

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
during installation).
You can either install a stable version or the developer version, simply run 
this command from a Cygwin shell in your `$HOME` and replace `<state>` with either stable or develop

	$ wget -q -O - --no-check-certificate https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh install <state> | bash

If you get the error "flags: FATAL unable to determine getopt version" error after 

	$ git flow init

you need to install the `util-linux` package using the Cygwin setup.

## GitHub for Windows

GitHub for Windows uses a portable installation of MSysGit for its shell. You'll need to follow the above instructions for MSysGit, except for two differences, both of which rely on the install location for GHfW's MSysGit install location. To find that location:

Navigate to the GitHub directory under the OS's `"Local Application Data"` directory. On Windows 7, it is located at: `"C:\Users\USER_NAME\AppData\Local\GitHub"`.
Look for a directory named something similar to `"PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7"`. Note: the GUID at the end may change.

Once you have the location, use it to perform the following (refer to the above MSysGet instructions above for more details):  
Download the [getopt archive](http://bit.ly/T5ZMHE) which I created. Extract the files and copy them to the `bin` directory directly under the location found above. In Windows 7, you would copy the files to: `"C:\Users\USER_NAME\AppData\Local\GitHub\PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7\bin"`.

Open the GitHub for Windows Git Shell and check that you are in the GitHub root directory e.g. `C:\GitHub>`
Clone the GitFlow folder with 

	C:\GitHub> git clone --recursive git://github.com/nvie/gitflow.git

This will clone the GitFlow code into a new `gitflow` folder in your GitHub directory. You can select a different location if you prefer or you can remove the GitFlow clone later.

Change to the GitFlow directory:

	C:\GitHub> cd gitflow

Run the `msysgit-install` script with the location as a parameter. For example:

	C:\GitHub\gitflow [develop]> contrib\msysgit-install.cmd "C:\Users\USER_NAME\AppData\Local\GitHub\PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7"

Note: Replace `PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7` with the name of your directory; you do not need the \bin at the end.

Check that GitFlow is installed by calling the help:

	C:\GitHub> git flow help 