# Git Aliases
Git aliases simplifying common or odd tasks. 

## How to add an alias
- Edit your .gitconfig file
  - C:\Users\\%USERNAME%\\.gitconfig
  - Under the [alias] section
- git alias command
  - git config --global alias."alias name" "command1; command2; command3"
  - Ex.
    - git config --global alias.atomic '!f() { git add . && git commit -am "$1" && git push; }; f'

## Aliases

### Atomic commits
add untracked files, commit, and push.

<dl>
  <dt>Usage</dt>
  <dd>git atomic "Title" "Message"</dd>

  <dt>Install Command</dt>
  <dd>
    
    git config --global alias.atomic '!f() { git add . && git commit -am "$1" && git push; }; f'
  </dd>
</dl>


___

### Refresh local
Clears all local changes and pulls the latest version of the current branch.

<dl>
  <dt>Usage</dt>
  <dd>git fresh</dd>

  <dt>Install Command</dt>
  <dd>
    
    git config --global alias.fresh '!f() { current_branch=$(git rev-parse --abbrev-ref HEAD); git reset --hard; git fetch origin; git checkout $current_branch; git pull origin $current_branch; }; f'
  </dd>
</dl>
