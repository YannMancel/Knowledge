# Git

## Link
[https://git-scm.com/](https://git-scm.com/)

## Useful commands

### Configure tool

Command                                            | Description
:--------------------------------------------------|:-----------------------
`git config --global user.name "[nom]"`            | Définit le nom que vous voulez associer à toutes vos opérations de commit |
`git config --global user.email "[adresse email]"` | Définit l'email que vous voulez associer à toutes vos opérations de commit |
`git config --global color.ui auto`                | Active la colorisation de la sortie en ligne de commande |

### Create repository

Command                    | Description
:--------------------------|:-----------------------
`git init [nom-du-projet]` | Crée un dépôt local à partir du nom spécifié |
`git clone [url]`          | Télécharge un projet et tout son historique de versions |

### Perform changements

Command                                | Description
:--------------------------------------|:-----------------------
`git init [nom-du-projet]`             | Crée un dépôt local à partir du nom spécifié |
`git status`                           | Liste tous les nouveaux fichiers et les fichiers modifiés à commiter |
`git diff`                             | Montre les modifications de fichier qui ne sont pas encore indexées |
`git add [fichier]`                    | Ajoute un instantané du fichier, en préparation pour le suivi de version |
`git add -A`                           | Ajoute tous les fichiers, en préparation pour le suivi de version |
`git commit -m "[message descriptif]"` | Enregistre des instantanés de fichiers de façon permanente dans l'historique des versions |

### Group changements

Command                            | Description
:----------------------------------|:-----------------------
`git branch`                       | Liste toutes les branches locales dans le dépôt courant |
`git branch [nom-de-branche]`      | Crée une nouvelle branche |
`git checkout [nom-de-branche]`    | Bascule sur la branche spécifiée et met à jour le répertoire de travail |
`git checkout -b [nom-de-branche]` | Crée une nouvelle branche et bascule dessus et met à jour le répertoire de travail |
`git merge [nom-de-branche]`       | Combine dans la branche courante l'historique de la branche spécifiée |
`git branch -d [nom-de-branche]`   | Supprime la branche spécifiée |

### Changements on file' name

Command                                      | Description
:--------------------------------------------|:-----------------------
`git rm [fichier]`                           | Supprime le fichier du répertoire de travail et met à jour l'index |
`git rm --cached [fichier]`                  | Supprime le fichier du système de suivi de version mais le préserve localement |
`git mv [fichier-nom] [fichier-nouveau-nom]` | Renomme le fichier et prépare le changement pour un commit |

### Exclude files

Command                                             | Description
:---------------------------------------------------|:-----------------------
`*.log`<br>`build/`<br>`temp-*`                     | Un fichier texte nommé .gitignore permet d'éviter le suivi de version accidentel pour les fichiers et chemins correspondant aux patterns spécifiés |
`git ls-files --other --ignored --exclude-standard` | Liste tous les fichiers exclus du suivi de version dans ce projet |

### Check the version history

Command                                            | Description
:--------------------------------------------------|:-----------------------
`git log`                                          | Montre l'historique des versions pour la branche courante |
`git log --follow [fichier]`                       | Montre l'historique des versions, y compris les actions de renom- mage, pour le fichier spécifié |
`git diff [premiere-branche]...[deuxieme-branche]` | Montre les différences de contenu entre deux branches |
`git show [commit]`                                | Montre les modifications de métadonnées et de contenu inclues dans le commit spécifié |

### Perform again commit

Command                              | Description
:------------------------------------|:-----------------------
`git reset [commit]`                 | Annule tous les commits après `[commit]`, en conservant les modifications localement |
`git reset HEAD~[N dernier commits]` | Annule les `[N dernier commits]`, en conservant les modifications localement |
`git reset --hard [commit]`          | Supprime tout l'historique et les modifications effectuées après le commit spécifié |

### Save fragments

Command           | Description
:-----------------|:-----------------------
`git stash`       | Enregistre de manière temporaire tous les fichiers sous suivi de version qui ont été modifiés ("remiser son travail") |
`git stash pop`   | Applique une remise et la supprime immédiatement |
`git stash apply` | Applique une remise et sans la supprimer |
`git stash list`  | Liste toutes les remises |
`git stash drop`  | Supprime la remise la plus récente |

### Synchronize changements

Command                                  | Description
:----------------------------------------|:-----------------------
`git fetch [nom-de-depot]`               | Récupère tout l'historique du dépôt nommé |
`git merge [nom-de-depot]/[branche]`     | Fusionne la branche du dépôt dans la branche locale courante |
`git merge --abort`                      | Annule le fusion conflictuelle |
`git push [alias] [branche]`             | Envoie tous les commits de la branche locale vers GitHub |
`git push --force [alias] [branche]`     | Envoie tous les commits de la branche locale vers GitHub après un Rebase (modification de SHA-1) |
`git pull`                               | Récupère tout l'historique du dépôt nommé et incorpore les modifications |
`git remote add origin [url]`            | Crée une connexion avec un dépôt distant |
`git remote -vv`                         | Liste les connexions |
`git rebase [nom-de-branche]`            | Rebase la branche courante avec la branche spécifiée |
`git rebase -i HEAD~[N dernier commits]` | Rebase intéractif de la branche courante sur les `[N dernier commits]` |
`git rebase --continue`                  | Valide le Rebase |
`git reflog`                             | Accède au 50 derniers actions |
