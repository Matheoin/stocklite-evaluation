# Réponses — chasse au trésor

<!-- Format imposé, une réponse par ligne :
Q01: <réponse>
commande: <commande(s) utilisée(s)>
-->

Q01: 
commande: 

Q02: 
commande: 

Q03: 
commande: 

Q04: 
commande: 

Q05: 
commande: 

Q06: 
commande: 

Q07: 
commande: 

Q08: remotes/origin/experiment/cache-redis
commande: git branch -a --no-merged main --no-contains v1.0.0

Q09: src/utils.js
commande: git log --follow --name-status --oneline -- src/outils.js

Q10: 15 Nathan Robin
commande: git shortlog depart -sn | head -n 1

Q11: 2026-03-24
commande: git show -s --format=%cs v1.0.0

Q12: feat(cli): bannière de démarrage
commande: git log --grep="Revert" --oneline

Q13: de5637a7c2ec4e7458525081fd1d1e9b237f0708
commande: git log --grep="fix/valeur-totale" --merges -1 --format="%H"

Q14: 16
commande: git diff --numstat v0.1.0 v1.0.0 -- src/stock.js | awk '{print $1}'

Q15: 6d6b9207651255c22dd0f084b0cf793faed17f31
commande: git log -S "TODO: gérer les quantités négatives" -1 --format="%H"
