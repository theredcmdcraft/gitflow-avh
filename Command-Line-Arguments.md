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
show this help (default: false)

---

### git flow feature diff - Show all changes of the feature branch

#### Description
Show all changes in _\<name>_ that are not in _\<develop>_

#### Synopsis
git flow feature diff [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help (default: false)

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

---

### git flow feature delete - Delete a feature branch

#### Description
Deletes a given feature branch

#### Synopsis
git flow feature delete [-h] [-f] [-r] _\<name>_

#### Options
-h,--[no]help  
show this help (default: false)

-f,--[no]force  
force deletion (default: false)

-r,--[no]remote  
delete remote branch (default: false)

---

## Release

### git flow release - List existing release branches

#### Description
List existing release branches

#### Synopsis
git flow release [list] [-h] [-v]

#### Options
-h,--[no]help  
show this help (default: false)

-v,--[no]verbose  
verbose (more) output (default: false)

---

### git flow release start - Start a new release branch

#### Description
Start a new release branch

#### Synopsis
git flow release start [-h] [-F] \<version>

#### Options
-h,--[no]help  
show this help (default: false)

-F,--[no]fetch  
fetch from origin before performing finish (default: false)

---

### git flow release finish - Finish a release branch

#### Description
Finish a release branch

#### Synopsis
git flow release finish [-h] [-F] [-s] [-u] [-m | -f] [-p] [-k] [-n] [-b] [-S] \<version>

#### Options
-h,--[no]help  
show this help (default: false)

-F,--[no]fetch  
fetch from origin before performing finish (default: false)

-s,--[no]sign  
sign the release tag cryptographically (default: false)

-u,--signingkey  
use the given GPG-key for the digital signature (implies -s) (default: '')

-m,--message  
use the given tag message (default: '')

-f,--messagefile  
use the contents of the given file as a tag message (default: '')

-p,--[no]push  
push to origin after performing finish (default: false)

-k,--[no]keep  
keep branch after performing finish (default: false)

-n,--[no]notag  
don't tag this release (default: false)

-b,--[no]nobackmerge  
don't back-merge master, or tag if applicable, in develop  (default: false)

-S,--[no]squash  
squash release during merge (default: false)

---

### git flow release publish - Publish a release branch

#### Description 
Publish the release branch _\<name>_ on $ORIGIN

#### Synopsis
git flow release publish [-h] \<name>

#### Options
-h,--[no]help  
show this help (default: false)

---

### git flow release track - Track a release branch

#### Description
Start tracking release _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow release track [-h] \<name>

#### Options
-h,--[no]help  
show this help (default: false)

---

### git flow release delete - Delete a release branch

#### Description
Deletes a given release branch

#### Synopsis
git flow release delete [-h] [-f] [-r] _\<name>_

#### Options
-h,--[no]help  
show this help (default: false)

-f,--[no]force  
force deletion (default: false)

-r,--[no]remote  
delete remote branch (default: false)

---

## Hotfix

### git flow hotfix - Lists all hotfix branches

#### Description
Lists all local hotfix branches

#### Synopsis
git flow hotfix [list] [-h] [-v]

#### Options
-h,--[no]help  
show this help (default: false)

-v,--[no]verbose  
verbose (more) output (default: false)

---

### git flow hotfix start - Start a hotfix branch

#### Description
Start new hotfix branch named _\<version>_, optionally base it on _\<base>_ instead of the _\<master>_ branch

#### Synopsis
git flow hotfix start [-h] [-F] \<version> [\<base>]

#### Options
-h,--[no]help  
show this help (default: false)

-F,--[no]fetch  
fetch from origin before performing finish (default: false)

---

### git flow hotfix finish - Finish a hotfix branch

#### Description
Finish hotfix branch _\<version>_

#### Synopsis 
git flow hotfix finish [-h] [-F] [-s] [-u] [-m | -f ] [-p] [-k] [-n] [-b] _\<version>_

#### Options
-h,--[no]help  
show this help (default: false)

-F,--[no]fetch  
fetch from origin before performing finish (default: false)

-s,--[no]sign  
sign the release tag cryptographically (default: false)

-u,--signingkey  
use the given GPG-key for the digital signature (implies -s) (default: '')

-m,--message  
use the given tag message (default: '')

-f,--messagefile  
use the contents of the given file as tag message (default: '')

-p,--[no]push  
push to origin after performing finish (default: false)

-k,--[no]keep  
keep branch after performing finish (default: false)

-n,--[no]notag  
don't tag this release (default: false)

-b,--[no]nobackmerge
  don't back-merge master, or tag if applicable, in develop  (default: false)

---
  
### git flow hotfix publish - Publish the hotfix branch

#### Description
Start sharing hotfix _\<name>_ on $ORIGIN

#### Synopsis
git flow hotfix publish [-h] \<name>

#### Options
-h,--[no]help  
show this help (default: false)

---

### git flow hotfix delete - Delete a hotfix branch

#### Description
Deletes a given hotfix branch

#### Synopsis
git flow hotfix delete [-h] [-f] [-r] _\<name>_

#### Options
-h,--[no]help  
show this help (default: false)

-f,--[no]force  
force deletion (default: false)

-r,--[no]remote  
delete remote branch (default: false)

---

## Support

### git flow support - List all support branches

#### Description
List all local support branches

#### Synopsis
git flow support [list] [-h] [-v]

#### Options
-h,--[no]help  
show this help (default: false)

-v,--[no]verbose  
verbose (more) output (default: false)

---

### git flow support start - Start a support branch

#### Description
Start a new support branch name _\<version_ based on _\<base>_

#### Synopsis
git flow support start [-h] [-F] \<version> \<base>

#### Options
-h,--[no]help  
show this help (default: false)

-F,--[no]fetch  
fetch from origin before performing finish (default: false)

---

## Version

### git flow version

#### Description
Display the git flow version.

#### Synopsis
git flow version

#### Options
_None_

---

## Configuration

### Setting a different remote repo
A remote repo different from _origin_ can be specified in the config file:

`$ git config gitflow.origin myorigin`
