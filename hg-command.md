## hg-commands

1. Make changes in the repository.

2. `hg diff` to see diff of entire tree or `hg diff pathToDir` to see directory related diff.

3. Commit the changes with - `hg commit -m "Bug XXXX - My commit message. r?ReviewerNickName"`.

4- You can check out what you are pushing by this command- `hg out -r . review`.

5. Push it with - `hg push -r . review` or `hg push review`. `hg push review` will push all local changesets that are not in the review repository, while `-r .` will just push those in the current branch.
