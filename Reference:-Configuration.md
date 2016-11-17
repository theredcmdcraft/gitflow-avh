# Reference: Configuration

### Setting a different remote repo
A remote repo different from .origin. can be specified in the config file:

`$ git config gitflow.origin myorigin`

### Set git specific environment variables.
With git you can set environment variables to change the default behavior of 
git. You can set these environment variables just for git-flow.

These environment variables can be set in the file `.gitflow_export` in your 
home directory. 
Example of a `.gitflow_export` file:

    export GIT_MERGE_AUTOEDIT=no

### Configuration variables to set flags
The configuration variables are named as follows:
`gitflow.<command>.<subcommand>.<flags>`
All variables should be in lower caps.

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

This is an overview per command of configuration variables you can set. The list 
is in the form `variable - flag - valid value`  
For reading improvement the prefix `gitflow.` is not show here but should 
be used when you set the variable. 
#### git-flow feature
feature.start.fetch - fetch - boolean

feature.finish.fetch - fetch - boolean  
feature.finish.rebase - rebase - boolean  
feature.finish.preserve.merges - preserve.merges - boolean  
feature.finish.keep - keep - boolean  
feature.finish.keepremote - keepremote - boolean  
feature.finish.keeplocal - keeplocal - boolean  
feature.finish.force.delete - force.delete - boolean  
feature.finish.squash - squash - boolean  
feature.finish.squash-info - squash.info - boolean  
feature.finish.no-ff - no-ff - boolean  

feature.rebase.interactive - interactive - boolean  
feature.rebase.preserve.merges - preserve.merges - boolean  

feature.delete.force - force - boolean  
feature.delete.remote - remote - boolean  

#### git-flow hotfix
hotfix.start.fetch - fetch - boolean  

hotfix.finish.fetch - fetch - boolean  
hotfix.finish.sign - sign - boolean  
hotfix.finish.push - push - boolean  
hotfix.finish.keep - keep - boolean  
hotfix.finish.keepremote - keepremote - boolean  
hotfix.finish.keeplocal - keeplocal - boolean  
hotfix.finish.force.delete - force.delete - boolean  
hotfix.finish.notag - notag - boolean  
hotfix.finish.nobackmerge - nobackmerge - boolean  
hotfix.finish.signingkey - signingkey - string  
hotfix.finish.message - message - string  
hotfix.finish.messagefile - messagefile - string  

hotfix.rebase.interactive - interactive - boolean  
hotfix.rebase.preserve.merges - preserve.merges - boolean  

hotfix.delete.force - force - boolean  

#### git-flow init
init.defaults - defaults - boolean  

#### git-flow release
release.start.fetch - fetch - boolean  

release.finish.fetch - fetch - boolean  
release.finish.sign - sign - boolean  
release.finish.push - push - boolean  
release.finish.keep - keep - boolean  
release.finish.keepremote - keepremote - boolean  
release.finish.keeplocal - keeplocal - boolean  
release.finish.force.delete - force.delete - boolean  
release.finish.notag - notag - boolean  
release.finish.nobackmerge - nobackmerge - boolean  
release.finish.squash - squash - boolean  
release.finish.squash.info - squash.info - boolean  
release.finish.signingkey - signingkey - string  
release.finish.message - message - string  
release.finish.messagefile - messagefile - string  

release.branch.fetch - fetch - boolean  
release.branch.sign - sign - boolean  
release.branch.push - push - boolean  
release.branch.notag - notag - boolean  
release.branch.squash - squash - boolean  
release.branch.squash.info - squash.info - boolean  
release.branch.signingkey - signingkey - string  
release.branch.message - message - string  
release.branch.messagefile - messagefile - string  

release.rebase.interactive - interactive - boolean  
release.rebase.preserve.merges - preserve.merges - boolean
  
release.delete.fetch - fetch - boolean  
release.delete.remote - remote - boolean  

#### git-flow support
support.start.fetch - fetch - boolean  
support.rebase.interactive - interactive - boolean  
support.rebase.preserve.merges - preserve.merges - boolean  

#### Example
You can set these variables using the `git config` command

    git config gitflow.release.finish.fetch yes
    
gitflow follows the same pattern for reading the options as `git config`.
You can use the options `--system`, `--global`, `--local` to write to that 
location and gitflow will behave simular in reading the configuration as git. 