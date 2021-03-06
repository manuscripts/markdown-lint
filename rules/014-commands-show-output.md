---
title: MD014 - Dollar signs used before commands without showing output
tags:  [code]
alias: commands-show-output
---

This rule is triggered when there are code blocks showing shell commands to be
typed, and the shell commands are preceded by dollar signs ($):

    $ ls
    $ cat foo
    $ less bar

The dollar signs are unnecessary in the above situation, and should not be
included:

    ls
    cat foo
    less bar

However, an exception is made when there is a need to distinguish between
typed commands and command output, as in the following example:

    $ ls
    foo bar
    $ cat foo
    Hello world
    $ cat bar
    baz

Rationale: it is easier to copy and paste and less noisy if the dollar signs
are omitted when they are not needed. See
<https://cirosantilli.com/markdown-style-guide#dollar-signs-in-shell-code>
for more information.

