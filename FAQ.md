* **Why a separate edition of git-flow?**

  As we were in need of the implementation of hooks and filters in git-flow, we
  wrote a patch for the original git-flow. After 5 months the patch still wasn't
  implemented and we decided to focus our work on creating the AVH Edition.
  Because of the rewrite we did it seems very likely that the patches for new
  features and bugfixes we create for the AVH Edition are not compatible with
  the original git-flow.

* **Can I still do manual branches and merges when I use git-flow?**

  Of course you can. `git-flow` does not forbid you to keep using vanilla Git
  commands!

  So if you want to merge `master` into `develop` for whatever reason you want
  to, you can safely do so without breaking `git-flow` compatibility. Do you
  want to manually merge a feature branch X into another feature branch Y? Not
  a problem. As long as you do it consciously and realize what this means for
  finishing those branches later on.

* **Why does git-describe not work for me?**

  It works with the AVH version of gitflow. Instead of merging the release
  branch back into the `develop` branch, the tag, if given, is merged back into
  the `develop` branch.

  <del>When finishing release and hotfix branches, that branch's HEAD is first
  merged into `master` and then into `develop`. It is not the resulting new
  merge commit from `master` that is merged back into `develop`. This means
  that a linear path from the new `develop` branch to the new `master` commit
  is not created. Even worse, a linear path is created from the new `develop`
  branch to the *previous* `master` commit. Although unintended, this is
  simply an effect of using the current branching rules.</del>

  <del>When using `git-describe` in these cases, you can get very confusing and
  misleading results, since `git-describe` scans the current commits linear
  history for the most recent tag it finds, which will always be the *previous*
  tag.</del>

* **Can I use it with Windows?**

  Yes, see [[Installing on Windows|Installing on Windows]]

* **What is the intended use of the `support` subcommand?**

  Long term support of old releases is a use case that not covered in the [original 
  description of Git Flow](https://nvie.com/posts/a-successful-git-branching-model/). You might for instance have customers running old releases 
  that still require bugfixes and maintenance, even though newer versions have long 
  since replaced them. The [`git flow support`](https://github.com/petervanderdoes/gitflow-avh/wiki/Reference:-git-flow-support)
  command creates branches that are _not supposed to be merged back into master_. 
  More info: [SO](https://stackoverflow.com/a/16866118/200987)
