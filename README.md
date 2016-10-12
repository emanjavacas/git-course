
# Git materials
--- 
## Books ##

- [Official Git Book (Pro Git)](https://git-scm.com/book/en/v2), reference book.
- [Pragmatic Guide to Git](https://pragprog.com/book/pg_git/pragmatic-guide-to-git), easy-going introduction, not too difficult.
- [Mastering Git](https://www.packtpub.com/application-development/mastering-git), more advanced.

## Online Tutorials ##

- [Try Git](https://try.github.io/levels/1/challenges/1), simple and nice intro to the basics of the git command line.
- [Learn Git Branching](http://learngitbranching.js.org/), similar to Try Git but with a focus on "branching" and more advanced ops.

## Graphical Interfaces ##

- [gitk, git-gui](https://git-scm.com/book/en/v2/Git-in-Other-Environments-Graphical-Interfaces), prepackaged with `git`
- [GitHub Desktop](https://desktop.github.com/), MacOS, Windows, (no Linux support). Barebones git.
- [GitKraken](https://www.gitkraken.com/), MacOS, Windows, Linux. More complete in terms of features.
- Embedded in your text editor (via plugins, etc.):
  - [Sublime Text: GitSavvy](https://github.com/divmain/GitSavvy), text based interface to git. Quite complete.
  - [Sublime Text: Git](https://github.com/kemayo/sublime-text-git), access to git through an embedded command line. Very thin wrapper.
  - [Magit for Emacs](https://magit.vc/), extremely handy - if you use Emacs :-).
  
  
## Cheatsheets ##

- [GitHub Training Cheatsheet](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)

# Git Concepts #

---

## Conceptual level ##

### Repository ###

- All VCS-tracked files in your project plus the full history of changes (commits) and branches.
- Any folder with a valid `/.git` subfolder in charge of tracking changes to not `.gitignore`d files in the folder.
- A repository can also be stored remotedly (handy in cases of projects with multiple collaborators).


> Other repository-related concepts are:

> - **Clone**: Your personal, local copy of a project (including a pointer to the remote repository - `origin`)
> - **Origin**: A standard alias (a name) that references the remote repository from which yours is a clone.
> - **Fork** (GitHub-only): Your remote copy (stored in GitHub) of a project. A local copy of a fork will include a reference to the remote copy (`origin`), as well as a reference to the source project (`upstream`)
> - **Upstream**: A standard alias (a name) that references the remote repository from which yours is a fork.

> This diagram, taken from [StackOverflow](http://stackoverflow.com/questions/9257533/what-is-the-difference-between-origin-and-upstream-on-github/9257901#9257901) might help you understanding the clone/fork story:

> ![Diagram](./img/origin_upstream.png)

### Working tree (or directory) ###

- Current local view of the project (folder). It can be changed by switching back to a previous state of the project (reset), a parallel state of the project (branch), or a future state (e.g. pulling from a remote repository).

### References ###

- A human-readable pointer to a particular commit. There are several types: Heads, Tags, Remotes.

> - **Head**
>   - A pointer to the current state of the working-tree.
>   - A dynamic symbolic reference (a reference of a reference, instead of a SHA-1 value) to the current branch.
> - **Tags**
>  - A name to a particular state in the repository's history.
>  - A static symbolic reference to a commit. It contains a tagger, a date, a message and a pointer.
>  - There are two types, "annotated tags" and "lightweight tags":
>    - Annotated
>    - Lightweight
> - **Remote**
>  - A repository copy stored in a remote server to which the local respository copy has access to (read or write, or both).
>  - A reference (or a bookmark) to a commit on a remote repository. It is read-only in the sense that it doesn't get updated by local commits.

### Commit ###

- A snapshot of the entire working directory (plus metadata including references to a previous snapshot, unique identifier - hash -, author, date etc.).
- A reference to a commit object (a log of all changes from a previous/parent commit to the current). It is referenced by a SHA-1 value and it is always associated with a branch.

### Branch ###

- Any of the parallel states in the repository (a particular commit history).
- A dynamic symbolic reference (a reference to a reference) to a commit. It gets updated after every new commit operation.

## Command level ##

See Cheatsheets for the moment.

# Setup
---

## `.gitignore`
TODO (general intro)

### Excluding subfolders but including subsubfolders
TODO (remember syntax for this)

## Config ##


### Global ###
``` bash
git config --global user.name "My Name"
git config --global user.email "my@email.com"
git config --global core.editor /usr/bin/emacs
```

### Local ###

#### Editing `./git/config`
TODO

#### Passwordless pushing and pulling
TODO

# GitHub tips #

---

## GitHub pages ##

- You can have a personal homepage served by GitHub. See instructions [here](https://pages.github.com/):
  - Make sure that your project complies with the structure of a [static homepage](https://en.wikipedia.org/wiki/Static_web_page).
  - Set your repository name to `username.github.io`
  
## Get downloadable zip or tar files for your project ##

### From GitHub ###

- Create a tag for the commit you want a downloadable 

### From the command line ###

