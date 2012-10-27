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

--

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
master				- Branch name for production releases    
develop				- Branch name for "next release" development    
feature				- Feature branch prefix    
hotfix				- Hotfix branch prefix    
release				- Release branch prefix    
support				- Support branch prefix    
versiontagprefix	- Version tag prefix    