# ZSH Command Line Interface Configuration #

This repo contains a bunch of helpers to improve my productivity in the Mac world.  Feel free to use and abuse this for your own needs.  You may prefer to use bash (via bash-it) and indeed some of the functions are written specifically in bash but you'll have to work out how to make any changes yourself as that is out of scope of this project. 

# iTerm2 #

Install and use iTerm, it has some functionality that allows for things like powerline fonts which are used by both oh-my-zsh and vim in this configuration (via certain plugins)

# .vimrc #

This configuration makes Vi a little more to my tastes.  Colour highlighted with some error detection, auto-completion and git integration.

By default I use darcula (blueshirts/darcula) but feel free to use your preferred colour scheme.  You may have noticed that I mix and match with solarized. 

[/blueshirts/darcula](https://github.com/blueshirts/darcula)

VI tagging is handled via eTags that can be installed via brew:

```brew install etags```

# Aliases #

|Alias|Command|
|---|---|---|
|-|'cd -'|
|...|../..|
|....|../../..|
|.....|../../../..|
|......|../../../../..|
|1|'cd -'|
|2|'cd -2'|
|3|'cd -3'|
|4|'cd -4'|
|5|'cd -5'|
|6|'cd -6'|
|7|'cd -7'|
|8|'cd -8'|
|9|'cd -9'|
|_|sudo|
|afind|'ack -il'|
|d|'dirs -v | head -10'|
|g|git|
|ga|'git add'|
|gaa|'git add --all'|
|gapa|'git add --patch'|
|gau|'git add --update'|
|gb|'git branch'|
|gba|'git branch -a'|
|gbd|'git branch -d'|
|gbda|'git branch --no-color --merged \| command grep -vE "^(\*|\s*(master|develop|dev)\s*$)" \| command xargs -n 1 git branch -d'|
|gbl|'git blame -b -w'|
|gbnm|'git branch --no-merged'|
|gbr|'git branch --remote'|
|gbs|'git bisect'|
|gbsb|'git bisect bad'|
|gbsg|'git bisect good'|
|gbsr|'git bisect reset'|
|gbss|'git bisect start'|
|gc|'git commit -v'|
|'gc!'|'git commit -v --amend'|
|gca|'git commit -v -a'|
|'gca!'|'git commit -v -a --amend'|
|gcam|'git commit -a -m'|
|'gcan!'|'git commit -v -a --no-edit --amend'|
|'gcans!'|'git commit -v -a -s --no-edit --amend'|
|gcb|'git checkout -b'|
|gcd|'git checkout develop'|
|gcf|'git config --list'|
|gcl|'git clone --recursive'|
|gclean|'git clean -fd'|
|gcm|'git checkout master'|
|gcmsg|'git commit -m'|
|'gcn!'|'git commit -v --no-edit --amend'|
|gco|'git checkout'|
|gcount|'git shortlog -sn'|
|gcp|'git cherry-pick'|
|gcpa|'git cherry-pick --abort'|
|gcpc|'git cherry-pick --continue'|
|gcs|'git commit -S'|
|gcsm|'git commit -s -m'|
|gd|'git diff'|
|gdca|'git diff --cached'|
|gdct|'git describe --tags `git rev-list --tags --max-count=1`'|
|gdt|'git diff-tree --no-commit-id --name-only -r'|
|gdw|'git diff --word-diff'|
|gf|'git fetch'|
|gfa|'git fetch --all --prune'|
|gfo|'git fetch origin'|
|gg|'git gui citool'|
|gga|'git gui citool --amend'|
|ggpull|'git pull origin $(git\_current\_branch)'|
|ggpur|ggu|
|ggpush|'git push origin $(git\_current\_branch)'|
|ggsup|'git branch --set-upstream-to=origin/$(git\_current\_branch)'|
|ghh|'git help'|
|gignore|'git update-index --assume-unchanged'|
|gignored|'git ls-files -v | grep "^[[:lower:]]"'|
|git-svn-dcommit-push|'git svn dcommit && git push github master:svntrunk'|
|gk|'\gitk --all --branches'|
|gke|'\gitk --all $(git log -g --pretty=%h)'|
|gl|'git pull'|
|glg|'git log --stat'|
|glgg|'git log --graph'|
|glgga|'git log --graph --decorate --all'|
|glgm|'git log --graph --max-count=10'|
|glgp|'git log --stat -p'|
|glo|'git log --oneline --decorate'|
|globurl|'noglob urlglobber '|
|glog|'git log --oneline --decorate --graph'|
|gloga|'git log --oneline --decorate --graph --all'|
|glol|'git log --graph --pretty='\'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --abbrev-commit'|
|glola|'git log --graph --pretty='\'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --abbrev-commit --all'|
|glp|\_git\_log\_prettily|
|glum|'git pull upstream master'|
|gm|'git merge'|
|gmom|'git merge origin/master'|
|gmt|'git mergetool --no-prompt'|
|gmtvim|'git mergetool --no-prompt --tool=vimdiff'|
|gmum|'git merge upstream/master'|
|gp|'git push'|
|gpd|'git push --dry-run'|
|gpoat|'git push origin --all && git push origin --tags'|
|gpristine|'git reset --hard && git clean -dfx'|
|gpsup|'git push --set-upstream origin $(git\_current\_branch)'|
|gpu|'git push upstream'|
|gpv|'git push -v'|
|gr|'git remote'|
|gra|'git remote add'|
|grb|'git rebase'|
|grba|'git rebase --abort'|
|grbc|'git rebase --continue'|
|grbi|'git rebase -i'|
|grbm|'git rebase master'|
|grbs|'git rebase --skip'|
|grep|'grep  --color=auto --exclude-dir={.bzr,CVS,.git,.hg,.svn}'|
|grh|'git reset HEAD'|
|grhh|'git reset HEAD --hard'|
|grmv|'git remote rename'|
|grrm|'git remote remove'|
|grset|'git remote set-url'|
|grt|'cd $(git rev-parse --show-toplevel || echo ".")'|
|gru|'git reset --'|
|grup|'git remote update'|
|grv|'git remote -v'|
|gsb|'git status -sb'|
|gsd|'git svn dcommit'|
|gsi|'git submodule init'|
|gsps|'git show --pretty=short --show-signature'|
|gsr|'git svn rebase'|
|gss|'git status -s'|
|gst|'git status'|
|gsta|'git stash save'|
|gstaa|'git stash apply'|
|gstc|'git stash clear'|
|gstd|'git stash drop'|
|gstl|'git stash list'|
|gstp|'git stash pop'|
|gsts|'git stash show --text'|
|gsu|'git submodule update'|
|gts|'git tag -s'|
|gtv|'git tag | sort -V'|
|gunignore|'git update-index --no-assume-unchanged'|
|gunwip|'git log -n 1 | grep -q -c "\\-\\-wip\\-\\-" && git reset HEAD~1'|
|gup|'git pull --rebase'|
|gupv|'git pull --rebase -v'|
|gwch|'git whatchanged -p --abbrev-commit --pretty=medium'|
|gwip|'git add -A; git rm $(git ls-files --deleted) 2> /dev/null; git commit --no-verify -m "--wip-- [skip ci]"'|
|history|'fc -l 1'|
|iswet|'curl -4 wttr.in/London'|
|l|'ls -lah'|
|la|'ls -lAh'|
|ll|'ls -lh'|
|ls|'ls -G'|
|lsa|'ls -lah'|
|md|'mkdir -p'|
|please|sudo|
|po|popd|
|pu|pushd|
|rd|rmdir|
|reload|'clear; source ~/.zshrc'|
|run-help|man|
|vupdate|'vim -c VundleUpdate -c quitall'|
|which-command|whence|

# Functions #

|Function|Purpose|
|---|---|
|mdless | less with MarkDown formatting|
|mdcat | cat with MarkDown formatting|
