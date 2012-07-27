# Reference: git flow feature

### git flow feature [list] [-v] - Lists existing feature branches

#### Description
Lists all the existing feature branches in the local repository.

#### Synopsis
git flow feature [list] [-h] [-v]

#### Options
-h,--[no]help
show this help

-v,--[no]verbose
verbose (more) output

---

### git flow feature start - Start a new feature branch

#### Description
Start new feature _\<name>_, optionally basing it on _\<base>_ instead of _\<develop>_

#### Synopsis
git flow feature start [-h] [-F] \<name> [\<base>]

#### Options
-h,--[no]help
show this help

-F,--[no]fetch
fetch from origin before performing local operation

---

### git flow feature finish - Finish a existing feature

#### Description
Finish feature _\<name>_

#### Synopsis
git flow feature finish [-h] [-F] [-r] [-k] [-D] [-S] \<name|nameprefix>

#### Options
-h,--[no]help
show this help

-F,--[no]fetch
fetch from origin before performing finish

-r,--[no]rebase
rebase instead of merge

-k,--[no]keep
keep branch after performing finish

--[no]keepremote
keep the remote branch

--[no]keeplocal
keep the local branch

-D,--[no]force_delete
force delete feature branch after finish

-S,--[no]squash
squash feature during merge

---

### git flow feature publish - Publish feature branch

#### Description
Publish feature branch _\<name>_ on $ORIGIN

#### Synopsis
git flow feature publish [-h] \<name>

#### Options
-h,--[no]help
show this help

---

### git flow feature track - Track a feature branch

#### Description
Start tracking feature _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow feature track [-h] \<name>

#### Options
-h,--[no]help
show this help

---

### git flow feature diff - Show all changes of the feature branch

#### Description
Show all changes in _\<name>_ that are not in _\<develop>_

#### Synopsis
git flow feature diff [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help
show this help

---

### git flow feature rebase - Perform a rebase

#### Description
Rebase _\<name>_ on _\<develop>_

#### Synopsis
git flow feature rebase [-h] [-i] [\<name|nameprefix>]

#### Options
-h,--[no]help
show this help

-i,--[no]interactive
do an interactive rebase

---

### git flow feature checkout - Checkout the feature branch

#### Description
Switch to feature branch _\<name>_

#### Synopsis
git flow feature checkout [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help
show this help

---

### git flow feature pull - Pull feature branch

#### Description
Pull feature _\<name>_ from _\<remote>_

#### Synopsis
git flow feature pull [-h] \<remote> [\<name>]

#### Options
-h,--[no]help
show this help

---

### git flow feature delete - Delete a feature branch

#### Description
Deletes a given feature branch

#### Synopsis
git flow feature delete [-h] [-f] [-r] _\<name>_

#### Options
-h,--[no]help
show this help

-f,--[no]force
force deletion

-r,--[no]remote
delete remote branch
