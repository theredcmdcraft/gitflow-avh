# Reference -  git flow release

### git flow release - List existing release branches

#### Description
List existing release branches

#### Synopsis
git flow release [list] [-h] [-v]

#### Options
-h,--[no]help  
show this help

-v,--[no]verbose  
verbose (more) output

---

### git flow release start - Start a new release branch

#### Description
Start a new release branch

#### Synopsis
git flow release start [-h] [-F] \<version>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing finish

---

### git flow release finish - Finish a release branch

#### Description
Finish a release branch

#### Synopsis
git flow release finish [-h] [-F] [-s] [-u] [-m | -f] [-p] [-k] [-n] [-b] [-S] \<version>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing finish

-s,--[no]sign  
sign the release tag cryptographically

-u,--signingkey  
use the given GPG-key for the digital signature (implies -s)

-m,--message  
use the given tag message

-f,--messagefile  
use the contents of the given file as a tag message

-p,--[no]push  
push the production and develop branch to origin after performing the finish.

--[no]pushproduction
push the production branch to origin after performing the finish.

--[no]pushdevelop
push the develop branch to origin after performing the finish.

-k,--[no]keep  
keep branch after performing finish

--[no]keepremote  
keep the remote branch

--[no]keeplocal  
keep the local branch

-n,--[no]notag  
don't tag this release

-T,--tagname  
Use given tag name

-b,--[no]nobackmerge  
don't back-merge master, or tag if applicable, in develop

-S,--[no]squash  
squash release during merge

--ff-master  
Fast forward master branch if possible

---

### git flow release branch - Finish any given branch

#### Description
Release a branch _[\<name>]_, if a name is not given it defaults to the
develop branch, and use the given version  _\<version>_

#### Synopsis
git flow release branch [-h] [-F] [-s] [-u] [-m] [-f] [-p] [-n] [-S] \<version> [\<name>]

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

-F,--[no]fetch  
fetch from origin before performing finish

-s,--[no]sign  
sign the release tag cryptographically

-u,--signingkey  
use the given GPG-key for the digital signature (implies -s)

-m,--message  
use the given tag message

-f,--messagefile  
use the contents of the given file as a tag message

-p,--[no]push  
push to origin after performing finish

-n,--[no]notag  
don't tag this release

-S,--[no]squash  
squash release during merge

---

### git flow release publish - Publish a release branch

#### Description
Publish the release branch _\<name>_ on $ORIGIN

#### Synopsis
git flow release publish [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands
Show git commands while executing them

---

### git flow release track - Track a release branch

#### Description
Start tracking release _\<name>_ that is shared on $ORIGIN

#### Synopsis
git flow release track [-h] \<name>

#### Options
-h,--[no]help  
show this help

--showcommands  
Show git commands while executing them

---

### git flow release delete - Delete a release branch

#### Description
Deletes a given release branch

#### Synopsis
git flow release delete [-h] [-f] [-r] _\<name>_

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

### git flow release rebase - Perform a rebase

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
 