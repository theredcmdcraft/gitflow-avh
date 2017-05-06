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

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing local operation

---

### git flow feature finish - Finish a existing feature

#### Description
Finish feature _\<name>_

#### Synopsis
git flow feature finish [-h] [-F] [-r] [-p] [-k] [-D] [-S] [--no-ff] \<name|nameprefix>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing finish

-r,--[no]rebase  
rebase instead of merge

-p,--[no]preserve-merges  
preserve merges while rebasing

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

--no-ff  
never fast-forward during the merge

---

### git flow feature publish - Publish feature branch

#### Description
Publish feature branch _\<name>_ on $ORIGIN

#### Synopsis
git flow feature publish [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow feature track - Track a feature branch

#### Description
Start tracking feature _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow feature track [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow feature diff - Show all changes of the feature branch

#### Description
Show all changes in _\<name>_ that are not in _\<develop>_

#### Synopsis
git flow feature diff [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow feature rebase - Perform a rebase

#### Description
Rebase _\<name>_ on _\<base_branch>_

#### Synopsis
git flow feature rebase [-h] [-i] [-p] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-i,--[no]interactive  
do an interactive rebase

-p, --[no]preserve-merges  
preserve merges

---

### git flow feature checkout - Checkout the feature branch

#### Description
Switch to feature branch _\<name>_

#### Synopsis
git flow feature checkout [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow feature pull - Pull feature branch

#### Description
Pull feature _\<name>_ from _\<remote>_

#### Synopsis
git flow feature pull [-h] \<remote> [\<name>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow feature delete - Delete a feature branch

#### Description
Deletes a given feature branch

#### Synopsis
git flow feature delete [-h] [-f] [-r] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-f,--[no]force  
force deletion

-r,--[no]remote  
delete remote branch

---

### git flow feature rename - Rename a feature branch

#### Description
Rename branch _\<name>_ to _\<new_name>_

#### Synopsis
git flow feature rename [-h] \<new_name> [\<name>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them
