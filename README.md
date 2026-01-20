## Branch Structure

**dev** Add encouraging message for players.
**documentation** Contains documentation-only changes added to describe the project’s branch structure and summarize the purpose of each branch.
**feature1** Adds the ability for the user to quit the game by entering a negative number, includes a play-again loop, and improves user feedback messages.
**feature2** Implements max attempts logic and game over condition.
**feature3** Adds a hint feature to assist the player during the game.
**hotfix** Fixes the randomInt function to properly include the maximum value in the range.
**main** Contains the initial version of the number guessing game.

## Learning Summary

**Differences:**
A merge combines branches while keeping their full history. I used merges when integrating stable branches, such as merging main back into dev after applying a hotfix. Merge commits make it clear when branches come together.

A rebase rewrites commit history by moving commits onto a new base. I rebased feature2 onto dev to keep the history cleaner and more linear. Although this required resolving conflicts, the resulting history was easier to follow than one with many merge commits.

Squashing combines multiple commits into a single commit. This was especially useful for feature3, which had several small development commits that were cleaned up into one clear, meaningful change before merging.

Cherry-picking applies a single commit from one branch to another. I used this for the hotfix so it could be applied directly to main without pulling in unfinished feature work, and then merged it back into dev to keep development in sync.

**Observations:**
feature1 shows gradual, incremental development.

feature2 highlights how rebasing changes and simplifies history.

feature3 demonstrates the benefit of squashing messy development commits.

**Use in real projects:**
I would use merge to preserve history, rebase to keep branches up to date, squash to clean up feature commits, and cherry-pick for urgent fixes that need to be applied independently of ongoing work.
