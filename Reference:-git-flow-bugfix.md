# Reference: git flow bugfix

### git flow bugfix [list] [-v] - Lists existing bugfix branches

#### Description
Lists all the existing bugfix branches in the local repository.

#### Synopsis
git flow bugfix [list] [-h] [-v]

#### Options
-h,--[no]help
show this help

-v,--[no]verbose
verbose (more) output

---

### git flow bugfix start - Start a new bugfix branch

#### Description
Start new bugfix _\<name>_, optionally basing it on _\<base>_ instead of _\<develop>_

#### Synopsis
git flow bugfix start [-h] [-F] \<name> [\<base>]

#### Options
-h,--[no]help
show this help

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing local operation

---

### git flow bugfix finish - Finish a existing bugfix

#### Description
Finish bugfix _\<name>_

#### Synopsis
git flow bugfix finish [-h] [-F] [-r] [-p] [-k] [-D] [-S] [--no-ff] \<name|nameprefix>

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
force delete bugfix branch after finish

-S,--[no]squash  
squash bugfix during merge

--no-ff  
never fast-forward during the merge

---

### git flow bugfix publish - Publish bugfix branch

#### Description
Publish bugfix branch _\<name>_ on $ORIGIN

#### Synopsis
git flow bugfix publish [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow bugfix track - Track a bugfix branch

#### Description
Start tracking bugfix _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow bugfix track [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow bugfix diff - Show all changes of the bugfix branch

#### Description
Show all changes in _\<name>_ that are not in _\<develop>_

#### Synopsis
git flow bugfix diff [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow bugfix rebase - Perform a rebase

#### Description
Rebase _\<name>_ on _\<base_branch>_

#### Synopsis
git flow bugfix rebase [-h] [-i] [-p] [\<name|nameprefix>]

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

### git flow bugfix checkout - Checkout the bugfix branch

#### Description
Switch to bugfix branch _\<name>_

#### Synopsis
git flow bugfix checkout [-h] [\<name|nameprefix>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow bugfix pull - Pull bugfix branch

#### Description
Pull bugfix _\<name>_ from _\<remote>_

#### Synopsis
git flow bugfix pull [-h] \<remote> [\<name>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow bugfix delete - Delete a bugfix branch

#### Description
Deletes a given bugfix branch

#### Synopsis
git flow bugfix delete [-h] [-f] [-r] _\<name>_

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-f,--[no]force  
force deletion

-r,--[no]remote  
delete remote branch
