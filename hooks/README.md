## les Hooks

Ce sont des scripts personnalisés lancés quand certaines actions importantes ont lieu (ex : le commit)

Normalement les Hook sont soit cotés client soit cotés serveur et non partageable ainsi que non versionnable 

Il existe une methode pour les rendre versionnable et partageable

La creation d'un dossier "hooks" est un lien symbolique entre le hook versionnable et le hook ce trouvant dans le .git/hooks

### Exemple :

```bash
git init
mkdir hooks
mv .git/hooks/pre-commit.sample hooks/pre-commit
touch .git/hooks/pre-commit
ln -s -f ../../hooks/pre-commit .git/hooks/pre-commit
```

### Info :
Dans le cas de notre exemple , si on veut passer outre le hook mis en place, il suffit de taper ceci :

```bash
git commit --no-verify
```

### Sources : 
* https://www.youtube.com/watch?v=7sBXEQ1dN4A
* https://stackoverflow.com/questions/4592838/symbolic-link-to-a-hook-in-git/4594681#4594681
