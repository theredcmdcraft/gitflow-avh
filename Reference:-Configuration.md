# Reference: Configuration

### Setting a different remote repo
A remote repo different from _origin_ can be specified in the config file:

`$ git config gitflow.origin myorigin`

### Set git specific environment variables.
With git you can set environment variables to change the default behavior of 
git. You can set these environment variables just for git-flow.

These environment variables can be set in the file `.gitflow_export` in your 
home directory. 
Example of a `.gitflow_export` file:

    export GIT_MERGE_AUTOEDIT=no

### Environment variables to set flags
The environment variables are named as follows:
`GITFLOW_FLAG_<COMMAND>_<SUBCOMMAND>_<FLAG>`
All variables should be in caps.

If the variable is a boolean the following values are valid, the case does not 
matter:
* Y
* YES
* T
* TRUE
* N
* NO
* F
* FALSE

If the variable represents a string surround the value with double quotes.

This is an overview per command of environment variables you can set. The list 
is in the form `variable - flag - valid value`  
For reading improvement the prefix `GITFLOW_FLAG_` is not show here but should 
be used using the variables. 
#### git-flow feature
FEATURE_START_FETCH - fetch - boolean

FEATURE_FINISH_FETCH - fetch - boolean  
FEATURE_FINISH_REBASE - rebase - boolean  
FEATURE_FINISH_PRESERVE_MERGES - preserve_merges - boolean  
FEATURE_FINISH_KEEP - keep - boolean  
FEATURE_FINISH_KEEPREMOTE - keepremote - boolean  
FEATURE_FINISH_KEEPLOCAL - keeplocal - boolean  
FEATURE_FINISH_FORCE_DELETE - force_delete - boolean  
FEATURE_FINISH_SQUASH - squash - boolean  
FEATURE_FINISH_SQUASH_INFO - squash_info - boolean  
FEATURE_FINISH_NO_FF - no_ff - boolean  

FEATURE_REBASE_INTERACTIVE - interactive - boolean  
FEATURE_REBASE_PRESERVE_MERGES - preserve_merges - boolean  

FEATURE_DELETE_FORCE - force - boolean  
FEATURE_DELETE_REMOTE - remote - boolean  

#### git-flow hotfix
HOTFIX_START_FETCH - fetch - boolean  

HOTFIX_FINISH_FETCH - fetch - boolean  
HOTFIX_FINISH_SIGN - sign - boolean  
HOTFIX_FINISH_PUSH - push - boolean  
HOTFIX_FINISH_KEEP - keep - boolean  
HOTFIX_FINISH_KEEPREMOTE - keepremote - boolean  
HOTFIX_FINISH_KEEPLOCAL - keeplocal - boolean  
HOTFIX_FINISH_FORCE_DELETE - force_delete - boolean  
HOTFIX_FINISH_NOTAG - notag - boolean  
HOTFIX_FINISH_NOBACKMERGE - nobackmerge - boolean  
HOTFIX_FINISH_SIGNINGKEY - signingkey - string  
HOTFIX_FINISH_MESSAGE - message - string  
HOTFIX_FINISH_MESSAGEFILE - messagefile - string  

HOTFIX_DELETE_FORCE - force - boolean  

#### git-flow init
INIT_DEFAULTS - defaults - boolean  

#### git-flow release
RELEASE_START_FETCH - fetch - boolean  

RELEASE_FINISH_FETCH - fetch - boolean  
RELEASE_FINISH_SIGN - sign - boolean  
RELEASE_FINISH_PUSH - push - boolean  
RELEASE_FINISH_KEEP - keep - boolean  
RELEASE_FINISH_KEEPREMOTE - keepremote - boolean  
RELEASE_FINISH_KEEPLOCAL - keeplocal - boolean  
RELEASE_FINISH_FORCE_DELETE - force_delete - boolean  
RELEASE_FINISH_NOTAG - notag - boolean  
RELEASE_FINISH_NOBACKMERGE - nobackmerge - boolean  
RELEASE_FINISH_SQUASH - squash - boolean  
RELEASE_FINISH_SQUASH_INFO - squash_info - boolean  
RELEASE_FINISH_SIGNINGKEY - signingkey - string  
RELEASE_FINISH_MESSAGE - message - string  
RELEASE_FINISH_MESSAGEFILE - messagefile - string  

RELEASE_BRANCH_FETCH - fetch - boolean  
RELEASE_BRANCH_SIGN - sign - boolean  
RELEASE_BRANCH_PUSH - push - boolean  
RELEASE_BRANCH_NOTAG - notag - boolean  
RELEASE_BRANCH_SQUASH - squash - boolean  
RELEASE_BRANCH_SQUASH_INFO - squash_info - boolean  
RELEASE_BRANCH_SIGNINGKEY - signingkey - string  
RELEASE_BRANCH_MESSAGE - message - string  
RELEASE_BRANCH_MESSAGEFILE - messagefile - string  

RELEASE_DELETE_FETCH - fetch - boolean  
RELEASE_DELETE_REMOTE - remote - boolean  

#### git-flow support
SUPPORT_START_FETCH - fetch - boolean  

#### Example
You can set these variables either for your entire login session by adding them 
to the apriorate files (i.e. `.bashrc`) or add them to the file 
`~/.gitflow_export`  

    export GITFLOW_FLAG_RELEASE_FINISH_FETCH=yes