# Configuración

```bash
git config --global -l
```

```properties
[user]
	name = Manu Artero Anguita
	email = manutero.developer@gmail.com

[push]
	default = simple

[alias]
  ...

[core]
	excludesfile = /Users/cx01885/.gitignore_global

[init]
	defaultBranch = main

[commit]
	template = /Users/cx01885/.stCommitMsg
```

#### .gitignore

1. **Local**: solo para el proyecto
   * [Herramienta para crear .gitignore](https://www.toptal.com/developers/gitignore)
   * [Colección en GitHub (por tipo de proyecto)](https://github.com/github/gitignore)
2. **Global**: fallback para todos tus proyectos

```properties
# MacOS
.DS_Store

# IDE
*~
.vscode

# deps
node_modules
.eggs/
*.pem
.mypy_cache/

# General
log/
*.log

```

### Alias que pueden ser útiles



```
[alias]
	ls = status -s
	head = !git rev-parse HEAD | pbcopy && pbpaste
	h = !git rev-parse HEAD | pbcopy && pbpaste
	l = cherry -v --abbrev=7 origin/master HEAD
	wip = commit -a --amend --no-edit
	check = checkout
	unstage = reset HEAD --
	stats = diff --stat HEAD~1 HEAD
	up = !git fetch && git rebase $(git rev-parse --abbrev-ref origin/HEAD)
	squash = "!function __git_squash() { branch=$1:-master; git rebase -i $(git merge-base branch HEAD); }; __git_squash"
	conflicts = !git diff --name-only --diff-filter=U
	alias=config --get-regexp alias
	super-pull = !git fetch && git reset --hard origin/$(git symbolic-ref --short HEAD)
  ctr-c-ctr-v= rebase
  
```

{% hint style="info" %}
Para hacer el mensaje de un commit, elige una de estas cinco (no te defraudará)



* fix: listing whatever properly
* feat: displaying whatever when whenever
* refactor: move from whatever to whateverito
* chore: house keeping. Mi casa como los chorros del oro
* docs
* \[test]
* \[style]
* \[perf]


{% endhint %}

{% embed url="https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716" %}
