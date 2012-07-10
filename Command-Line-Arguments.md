(version 1.0.65-avh)

### git flow init - Initialize the repository for git flow usage.

#### Description
Setup a git repository for git flow usage. Can also be used to start a git repository.

#### Synopsis
git flow init [-h] [-d] [-f]

#### Options
-h,--[no]help
show this help (default: false)                
-d,--[no]defaults
use default branch naming conventions (default: false)    
-f,--[no]force
force setting of gitflow branches, even if already configured (default: false)

## git flow feature

### git flow feature [list] [-v] - Lists existing feature branches

#### Description
Lists all the existing feature branches in the local repository.

#### Synopsis
git flow feature [list] [-h] [-v]

#### Options
-h,--[no]help
show this help (default: false)                     
-v,--[no]verbose
verbose (more) output (default: false)

---

### git flow feature start - Start a new feature branch

#### Description
Start new feature _\<name>_, optionally basing it on _\<base>_ instead of _\<develop>_

#### Synopsis
git flow feature start [-h] [-F] \<name> [\<base>]

#### Options
-h,--[no]help
show this help (default: false)    
-F,--[no]fetch
fetch from origin before performing local operation (default: false)    

---

### git flow feature finish - Finish a existing feature

#### Description
Finish feature _\<name>_

#### Synopsis
git flow feature finish [-h] [-F] [-r] [-k] [-D] [-S] \<name|nameprefix>

#### Options
-h,--[no]help
show this help (default: false)    
-F,--[no]fetch
fetch from origin before performing finish (default: false)    
-r,--[no]rebase
rebase instead of merge (default: false)    
-k,--[no]keep
keep branch after performing finish (default: false)    
-D,--[no]force_delete
force delete feature branch after finish (default: false)    
-S,--[no]squash
squash feature during merge (default: false)    

---

### git flow feature publish - Publish feature branch

#### Description
Publish feature branch _\<name>_ on $ORIGIN

#### Synopsis
git flow feature publish [-h] \<name>

#### Options
-h,--[no]help
show this help (default: false)    

---

### git flow feature track - Track a feature branch

#### Description
Start tracking feature _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow feature track [-h] \<name>

#### Options
-h,--[no]help

---

### git flow feature diff - Show all changes of the feature branch

#### Description
Show all changes in _\<name>_ that are not in _\<develop>_

#### Synopsis
git flow feature diff [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help

---

### git flow feature rebase - Perform a rebase

#### Description
Rebase _\<name>_ on _\<develop>_

#### Synopsis
git flow feature rebase [-h] [-i] [\<name|nameprefix>]

#### Options
-h,--[no]help
show this help (default: false)    
-i,--[no]interactive
do an interactive rebase (default: false)    

---

### git flow feature checkout - Checkout the feature branch

#### Description
Switch to feature branch _\<name>_

#### Synopsis
git flow feature checkout [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help
show this help (default: false)    

---

### git flow feature pull - Pull feature branch

#### Description
Pull feature _\<name>_ from _\<remote>_

#### Synopsis
git flow feature pull [-h] \<remote> [\<name>]

#### Options
-h,--[no]help
show this help (default: false)    

## Release

### git flow release [list] [-v]
**-v** verbose (more) output

Lists existing releases

### git flow release start [-F] \<version>
**-F** fetch from $ORIGIN before performing local operation

Start new release named _\<version>_

### git flow release finish [-FsumpknbS] \<version>
**-F** fetch from $ORIGIN before performing finish

**-s** sign the release tag cryptographically

**-u** use the given GPG-key for the digital signature (implies -s)

**-m** use the given tag message
**-f**

**-p** push to $ORIGIN after performing finish

**-k** keep branch after performing finish

**-n** don't tag this release

**-b** Don't back-merge the master branch or associated tag into the develop branch. Use the Release branch instead 

**-S** squash commits into one large one

Finish release _\<version>_

### git flow release publish \<name>
Start sharing release _\<name>_ on $ORIGIN

### git flow release track \<name>
Start tracking release _\<name>_ that is shared on $ORIGIN

## Hotfix
### git flow hotfix [list] [-v]
**-v** verbose (more) output

Lists existing hotfixes
### git flow hotfix start [-F] \<version> [\<base>]
**-F** fetch from $ORIGIN before performing local operation

Start new hotfix named _\<version>_, optionally base it on _\<base>_ instead of _\<master>_
### git flow hotfix finish [-Fsumpknb] \<version>
**-F** fetch from $ORIGIN before performing finish

**-s** sign the release tag cryptographically

**-u** use the given GPG-key for the digital signature (implies -s)

**-m** use the given tag message

**-p** push to $ORIGIN after performing finish

**-k** keep branch after performing finish

**-n** don't tag this release

**-b** Don't back-merge the master branch or associated tag into the develop branch. Use the Hotfix branch instead

Finish hotfix _\<version>_


### git flow hotfix publish \<name>
Start sharing hotfix _\<name>_ on $ORIGIN

## Support
### git flow support [list] [-v]
**-v** verbose (more) output

Lists existing support branches
### git flow support start [-F] \<version> \<base>
**-F** fetch from $ORIGIN before performing local operation

Start new support branch named _\<version>_ based on _\<base>_

## Version
### git flow version

Displays the git flow version.

## Configuration

### Setting a different remote repo
A remote repo different from _origin_ can be specified in the config file:

`$ git config gitflow.origin myorigin`
