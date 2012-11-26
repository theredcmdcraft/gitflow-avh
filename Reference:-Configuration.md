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
