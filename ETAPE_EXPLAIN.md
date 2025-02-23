# Etape 4:

L’upstream est la branche distante associée à une branche locale dans Git. Elle permet à Git de savoir vers où envoyer (git push) et d’où récupérer (git pull) les mises à jour.

Quand vous créez une nouvelle branche locale (git checkout -b Etape3), cette branche n'a pas d'upstream par défaut, ce qui signifie que Git ne sait pas où la pousser sur le dépôt distant. C'est pourquoi, lors du premier git push, une erreur s'affiche :

```
PS C:\Users\Legion\Documents\GitHub\devopsTP1> git checkout -b Etape3
Switched to a new branch 'Etape3'
PS C:\Users\Legion\Documents\GitHub\devopsTP1> git add AUTHORS.md     
warning: in the working copy of 'AUTHORS.md', CRLF will be replaced by LF the next time Git touches it
PS C:\Users\Legion\Documents\GitHub\devopsTP1> git commit -m "Etape 3"
[Etape3 0771dcf] Etape 3
 1 file changed, 1 deletion(-)
PS C:\Users\Legion\Documents\GitHub\devopsTP1> git push            
fatal: The current branch Etape3 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin Etape3

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

```

Cette commande :
- Crée une branche `Etape3` sur le dépôt distant.
- Associe la branche locale `Etape3` à la branche distante `origin/Etape3`.
- Permet d'utiliser `git push` sans argument par la suite.