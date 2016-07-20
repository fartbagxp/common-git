# Summary

A list of common tricks for using `git` that I've found useful in the past.

## Links

This is probably the best guide out there.

[Atlassian Git Guide](https://www.atlassian.com/git/tutorials/)

## Tricks

*   Scenario: You try to update from a particular branch to sync your code.
    However, your changes will be overwritten by the merge.

    `git pull origin master`

    To get around this, you should reset the repo and pull, and then apply your
    changes again.

    `git stash`

    `git reset --hard HEAD`

    `git pull origin master`

    `git stash pop`

*   Scenario: You want clean commit to be a single line only (the last commit).

    `git commit --amend --no-edit -a && git push --force`
