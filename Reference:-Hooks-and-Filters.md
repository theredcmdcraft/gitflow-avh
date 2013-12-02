# Reference: Hooks and Filters

## Introduction

Starting with version 0.4.2-avh1 filters are introduced and in the near future hooks will also be introduced.
Filters and Hooks are small scripts called during the git flow process.

## Installation

* Scripts need to be installed in the .git/hooks directory.
* Scripts need to be executable.

The use of filter and/or hooks is not mandated, when a script doesn't exists normal operations continue.

## Filters

### Version filters
These filters allow you to change the version.  
You can use this for example to automatically update the version, make sure the version adheres to the projects standards.

The filters are implemented in the following git flow commands

**git flow release start**

Script name: filter-flow-release-start-version


**git flow hotfix start**

Script name: filter-flow-hotfix-start-version

### Tag message filters
Filter the given tag message
 Works for the following commands:
 
 * hotfix finish
 * release finish
 * release branch
 
 Script names:
 * filter-flow-hotfix-finish-tag-message
 * filter-flow-release-finish-tag-message
 * filter-flow-release-branch-tag-message

## Hooks
### Hook scripts
Naming convention for the hook scripts follows the Git hooks conventions:
.git/hooks/{pre,post}-{subcmd}  
For example:  
* .git/hooks/pre-flow-feature-start
* .git/hooks/post-flow-release-finish

There are documented bare-bone scripts available in the doc/gitflow/hooks directory.
* {post,pre)-flow-feature-{finish,publish,pull,start,track,delete}
* {post,pre}-flow-hotfix-{finish,publish,start,delete}
* {post,pre}-flow-release-{finish,publish,start,track,delete}
