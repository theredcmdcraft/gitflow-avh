# Installing on Windows

For Windows users, [Git for Windows](#git-for-windows) is the recommended method.

## Git for Windows
Follow the instructions on the [Git for Windows homepage](https://git-for-windows.github.io) to install Git for Windows.  As of Git for Windows 2.6.4, GitFlow (AVH edition) is included, so you're all done.

# Other Methods

The below instructions are unsupported. The installation files need to be updated.

## Visual Studio
[Jakob Ehn](https://github.com/jakobehn/) created an extension for Visual Studio. Currently Visual Studio 2013 and 2015 are supported.  
The extension is available on the Microsoft Visual Studio Gallery website, the 2013 extension you can find [here](https://visualstudiogallery.msdn.microsoft.com/27f6d087-9b6f-46b0-b236-d72907b54683) and the 2015 extension is located [here](https://visualstudiogallery.msdn.microsoft.com/f5ae0a1d-005f-4a09-a19c-3f46ff30400a)  
For more information about the extension read up on [Jakob's website](http://blog.ehn.nu/2015/02/introducing-gitflow-for-visual-studio/) and you can find the source on [Github](https://github.com/jakobehn/GitFlow.VS)  

## Cygwin
For Windows users who wish to use the automated install, it is suggested that you install [Cygwin](http://www.cygwin.com/)
first to install tools like `git`, `util-linux` and `wget` (with those three being packages that can be selected
during installation).
You can either install a stable version or the developer version, simply run 
this command from a Cygwin shell in your `$HOME` and replace <state> with either stable or develop

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

	C:\GitHub> git clone --recursive git://github.com/petervanderdoes/gitflow.git

This will clone the GitFlow code into a new `gitflow` folder in your GitHub directory. You can select a different location if you prefer or you can remove the GitFlow clone later.

Change to the GitFlow directory:

	C:\GitHub> cd gitflow

Run the `msysgit-install` script with the location as a parameter. For example:

	C:\GitHub\gitflow [develop]> contrib\msysgit-install.cmd "C:\Users\USER_NAME\AppData\Local\GitHub\PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7"

Note: Replace `PortableGit_8810fd5c2c79c73adcc73fd0825f3b32fdb816e7` with the name of your directory; you do not need the \bin at the end.

Check that GitFlow is installed by calling the help:

	C:\GitHub> git flow help 