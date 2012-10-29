# Coding guidelines

In general we follow the same coding guidelines as git, but that doesn't mean
we follow them to the letter. So some of the guidelines might look familiar,
and that's because they are.

## General
As a rule of thumb just imitate the existing code. New code added to
git-flow AVH Edition is expected to match the overall style of existing code.
Modifications to existing code is expected to match the style the surrounding
code already uses (even if it doesn't match the overall style of existing code).

## More shell specific
* We use tabs for indentation.

* We eliminate whitespace at the end of a line.

* Case arms are indented at the same depth as case and esac lines.

* Variables used inside a function only should be declared local at the 
  beginning of the function.

* Local variables should be in lower case only.

* Local variables should not be assigned a value during declaration.

* Redirection operators should be written with space before, but no space
  after them.
  In other words, write 'echo test >"$file"' instead of 'echo test> $file'
  or 'echo test > $file'.  Note that even though it is not required by POSIX
  to double-quote the redirection target in a variable (as shown above), our
  code does so because some versions of bash issue a warning without the quotes.

* We prefer $( ... ) for command substitution; unlike ``, it properly nests.

* If you want to find out if a command is available on the user's $PATH, you
  should use 'type <command>', instead of 'which <command>'.
  The output of 'which' is not machine parseable and its exit code is not
  reliable across platforms.

* We use POSIX compliant parameter substitutions and avoid bashisms;
   namely:

   * We use ${parameter-word} and its [-=?+] siblings, and their colon'ed
     "unset or null" form.

   * We use ${parameter#word} and its [#%] siblings, and their doubled
     "longest matching" form.

   * No "Substring Expansion" ${parameter:offset:length}.

   * No shell arrays.

   * No pattern replacement ${parameter/pattern/string}.

* We use Arithmetic Expansion $(( ... )).

* Inside Arithmetic Expansion, spell shell variables with $ in front of them,
  as some shells do not grok $((x)) while accepting $(($x)) just
  fine (e.g. dash older than 0.5.4).

* We do not use Process Substitution <(list) or >(list).

* We prefer "[ ... ]" over "test".

* We do not write the noiseword "function" in front of shell
   functions.

## Git commits

1. Try to keep the first line short, preferably no more than 50 characters.
2. The second line should be blank.
3. Any additional lines should not exceed 80 columns.
4. The author field should properly be filled out with your full name and
   email address. If you need to know how to do this, please read this
   [paragraph](http://git-scm.com/book/en/Getting-Started-First-Time-Git-Setup#Your-Identity) in the book Pro Git, which is available for free on-line.

## Version numbering scheme
We follow the scheme as described by [Semantic Versioning 2.0.0-rc.1](http://semver.org/).
A normal version number MUST take the form X.Y.Z where X, Y, and Z are
non-negative integers. X is the major version, Y is the minor version,
and Z is the patch version.

For pre-release versions we append -dev.W where W is a non-negative integer.

For release candidates we append -rc.W where W is a non-negative integer.
