## Cheatsheet

### Basics:

1. __Adding files__

  - You can add files individually like:
    ```bash
    $ git add <file_name>
    ```
  - You can add files in bulk like:
    ```bash
    $ git add --all
    ```

2. __Creating commits__: Commits are (semi)-immutable snapshots in time that should represent the state of the codecase at the point. A commit does not have to be functional; you should commit frequently so you can backtrack if you get into trouble.

  ```bash
  $ git commit -m 'My descriptive commit message'
  ```

  Or use your favorite text editor (Vim by default):

  ```bash
  $ git commit
  ```

3. __Pushing__

  ```bash
  $ git push origin <branch_name>
  ```

4. __Branching__

  When you branch, your branch will be created FROM the commit/branch you're currently on, not HEAD.

  ```bash
  $ git checkout -b <new-branch-name>
  ```

5. __Merging__

  You can merge on the command line if you want to merge two feature branches together, or update your branch with changes to master. From the branch you want to merge INTO, simply run:

  ```bash
  $ git merge --no-ff <other-branch>
  ```

  Sometimes you'll encounter conflicts when merging. Simply resolve them, then run:

  ```bash
  $ git merge --continue
  ```

  If at any point you get stuck in a bad merge with a lot of conflicts, you can abort the merge:

  ```bash
  $ git merge --abort
  ```

6. __Rebasing__

  Rebasing is like merging, but you "replay" your commits onto a branch as if they happened from a different HEAD. From your feature branch:

  ```bash
  $ git rebase <other-branch>
  ```

  It's easy to get into conflicts with rebasing. See [this guide](https://nathanleclaire.com/blog/2014/09/14/dont-be-scared-of-git-rebase/) for helpful pointers
