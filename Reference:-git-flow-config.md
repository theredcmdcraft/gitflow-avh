# Reference: git flow config

### git flow config - List the git-flow configuration

#### Description
 List the git-flow configuration

#### Synopsis
git flow config [-h]

#### Options
-h,--[no]help
show this help

--showcommands
Show git commands while executing them

---

### git flow config set - Update the git-flow configuration

#### Description
Update the git-flow configuration.

#### Synopsis
git flow config set [options] \<config-option\> \<config-value\> 

#### Options
-h,--[no]help
show this help

--showcommands
Show git commands while executing them

*Use config file location*  
--local  
use repository config file - Default  

--global  
use global config file  

--system  
use system config file  

--file ...  
use given config file  


*Config Options*  
The following are the options you can set  
master			 - string  - Branch name for production releases  
develop			 - string  - Branch name for "next release" development  
feature			 - string  - Feature branch prefix  
hotfix			 - string  - Hotfix branch prefix  
release			 - string  - Release branch prefix  
support			 - string  - Support branch prefix  
versiontagprefix - string  - Version tag prefix  
allowmultihotfix - boolean - Allow multiple hotfix branches

---

### git flow config base - Update the git-flow base settings.

#### Description
Update the git-flow base configuration used when finishing a branch.

#### Synopsis
git flow config base [options] \<branch\> [\<base\>] 

#### Options
-h,--[no]help
show this help

--get  
Get the base for the given branch (default behavior).

--set   
Set the given base for the given branch.
