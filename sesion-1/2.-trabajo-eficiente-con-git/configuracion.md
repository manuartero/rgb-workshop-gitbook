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

