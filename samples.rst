samples
=======

Samples are chances to outperform your competitors. They are problems you've faced and solved once,
but that you didn't learn from. You're bound to fall on them again, much like all your adversaries,
and the only thing your experience will do is let you know you've fixed them once, so you're bound
to fix them again. But if you train on the solution you've found once, you'll outperform your
competitors.

You can feel how much you'll outperform your adversaries by how reluctact your body is from
answering the exercise. That reluctance is what your competitors will feel, and by overcoming it,
you overcome your competitors. Feel the reluctance giving to satisfaction by practicint the exercise
until you have an answer that perfectly answers it.

You can verify how untrained you are by how ambiguous your questions are at the beggining. And so
are your competitors. As sson as you begin getting a true answer to the question, you rephrase the
question because you have gained understanding about the question. Your competitors will be stuck
with the uninformed question, and it will take them ages to debug a situation because they lack
overall understanding of the problem.

Answering by writing in a txt file and comparing against the correct answer is not a good idea. You
must practice with the real feeling, that is, in an execution environment. The longer you take to answer
the exercise, the less you have practiced it. 

* the greatest resource is not time but focus
* don't reinvent the wheel, integrate
* champions practice until they can't it wrong, loosers practice until they get it right

samples
-------


- `E1` install vscode + zscaler + mac to bypass `unable to get local issuer certificate`
  - install extension `inhmtran168.mac-ca-vscode` and restart
  - TODO understand what the issue was
- `E2` project poetry config file? Show how to use the local config to create a venv locally instead the default location.
  - `poetry.toml` in project dir replaces global config in the specified keys
  - By default the venvs are created at `~/Library/Caches/pypoetry/virtualenvs`
  - Either edit `poetry.toml` or run `poetry config virtualenvs.in-project true --local`
- `E3` Where are the poetry environments located by default?
  - `~/.cache/pypoetry/virtualenvs`
- `E4` global poetry config file?
  - TODO
- `E5` How do you know you are using a python version installed by pyenv? How does that differ from a python versions intalled locally?
  - TODO, something about PATH? 
- `E6` how do you spawn a poetry shell with the pyenv selected version?
  - `poetry env use $(pyenv which python)` create and activate globally the virtual environment with the pyenv version
  - `poetry shell` activates that virtual environment
- `E7` which terminal session profile config file does poetry shell load?
  - `~/.bashrc`
- `E8` how to set globally which profile file ought new poetry environments to load?
  - TODO
- `E9` pyenv list available python versions locally installed
  - `pyenv versions`
- `E10` name 2 environment variables set by `pyenv shell` and their meaning.
  - `PYENV_ROOT`: where the pyenv python versions are installed
  - `PYENV_SHELL`: TODO
- `E11` select python interpreter at project dir?
  - open vscode in project dir, not in super folder
  - create poetry shell in the project dir (local poetry config file)
  - `cmd+shift+p` and `select python interpreter`
  - `select at workspace level`
  - the interpreter will appear suggested as `./.venv/...`
- `E12` why does `python@3.11` keep appearing in `/opt/homebrew/Cellar` after running `brew remove python`?
  - You're installing a brew package with brew `python@3.11` and installs it by
  default. Example: `virtualenv` is installed by `ranger`, and `virtualenv` installs `python@3.11`
- `E13` delete pyenv python version
  - `pyenv uninstall <version>`
- `E14` can't select python interpreter in workspace
  - open a project directory instead of opening a workspace with multiple orojects.
  - It will be then possible to identify the existing virtual env, the existing python system
  - versios, pyenv versions, atc.. Test with:
    - samples-sphinx $ poetry env use $(pyenv which python)
    - select venv as environment and try running a python file importing a dependency, see that it
      fails.
    - samples-sphinx $ poetry shell
    - (samples-sphinx-py4.11) samples-sphinx $ poetry install
    - select venv as environment and try running a python file importing a dependency, see that it
    succeeds.
- `E15` how many sorts of pyhton installations are there in a system?
  - system python
  - homebrew python
  - pyenv python
  - poetry python (for example points for a pyenv shim)
- `E16` tmux session `session-name` and window `window-name`: pane `?` tells `1` to prints its pwd
  - `tmux new-session -s session-name -n window-name`
  - `ctrl+b %`
  - `ctrl+b q`
  - `ctrl+b <left>|<right>`
  - `tmux send-keys -t 1 'pwd' Enter`
- `E17` tmux new named session and named window
  - `tmux new-session -d -s <session-name> -n <window-name>`
- `E18` What is the difference between a pane and a window in tmux?
  - panes are always on the same directory, windows can be in different directories
- `E19` Check commits of file?
  - `git log --follow <file>`
- `E20` Check commits of file with author?
  - `git log --follow --author=<author> <file>`
- `E21` Check commits of file with author and changes?
  - `git log --follow --author=<author> -p <file>`
- `E22` Check commits of file with author and changes, starting from the oldest?
  - `git log --follow --author=<author> -p --reverse <file>`
- `E23` vscode expand collapsed component on a macro
  - `cmd+K+J`
- `E24` get contributors of branch
  - `git shortlog -s -n <branch>`
- `E25` git get contribution for developer for all branches
  - `git shortlog -sne --no-merges --author=matdem --all --numstat`
- `E26` git delete local and remote branch
  - `git branch -d <branch>`
  - `git push origin --delete <branch>`
- `E27` docker remove all images
  - `docker rmi -f $(docker images -a -q)`
- `E28` docker stop all containers
  - `docker stop $(docker ps -a -q)`
- `E29` git reset local branch contents with remote branch contents
  - `git fetch origin`
  - `git reset --hard origin/<branch>`
- `E30` git delete local branch
  - `git branch -d <branch>`
- `E31` git see stash
  - `git stash list`
- `E32` git get stashed changes
  - `git stash show -p stash@{0}`
- `E33` git unstash
  - `git stash pop stash@{0}`
- `E34` postgres list all tables in database
  - `\dt`
- `E35` docker remove all containers
  - `docker rm -f $(docker ps -a -q)`
- `E36` docker list containers
  - `docker ps -a`
- `E37` mac install docker engine
  - TODO
- `E38` what is the difference between docker engine and docker desktop?
  - TODO
- `E39` tmux session `session-name` and window `window-name`: pane `?` tells `1` to print `?`s pwd
  - `tmux new-session -s session-name -n window-name`
  - `ctrl+b %`
  - `ctrl+b q`
  - `ctrl+b <left>|<right>`
  - `tmux send-keys -t 1 "echo $(pwd)" Enter`
- `E40` tmux session `session-name` and window `window-name`: pane `?` tells `1` to print env var of `?` with colours
  - `tmux new-session -s session-name -n window-name`
  - `ctrl+b %`
  - `ctrl+b q`
  - `ctrl+b <left>|<right>`
  - `here="\033[0;32m$(pwd)\033[0m"; tmux send-keys -t 1 "echo -e \"$here\"" Enter` or
  - `tmux send-keys -t 1 "echo -e \"\033[0;32m$(pwd)\033[0m]\"" Enter`
- `E41` mac tmux shortcut to close tmux session
  - `ctrl+b :kill-session`
- `E42` print pwd coloured green
  - `here="\033[0;32m$(pwd)\033[0m"; echo -e "$here"`
- `E43` how to you spawn a poetry shell in the poetry default dir for virtualenvs?
  - `poetry init`
  - `poetry config virtualenvs.in-project false`
  - `poetry shell`
- `E44` poetry remove env?
  - `poetry env remove <env-full-name>`
- `E45` mac tmux shorcut to detach?
  - `ctrl+b d`
- `E46` mac tmux shortcut to create new pane?
  - `ctrl+b %`
- `E47` mac tmux shortcut to show pane ids?
  - `ctrl+b q`
- `E48` mac tmux move to pane to the left?
  - `ctrl+b <left-arrow>`
- `E49` git log oneline with author name
  - `git log --oneline --format="%h %an: %s"`
- `E50` git stage only deleted files
  - `git ls-files --deleted -z | xargs -0 git rm`
- `E51` git revert single file to previous commit
  - `git checkout <commit> <file>`
- `E52` git revert to previous commit
  - `git reset --hard <commit>`
- `E53` What is IAM credentials passthrough?
  - legacy data governance model. 
- `E54` What should IAM credentials passthrough should be replaced with?
  - Unity Catalog which simplifies security and governance of your data by providing a central place to administer and audit data access across multiple workspaces in your account.
TODO
----

- what is the cdk proxy?
- how to see the history of a file (git)?
- git: what is git blame
- git: what is rebase
- git: what is the difference between fetch and pull
- git: what is the difference between merge and rebase
