# Réponses — chasse au trésor

<!-- Format imposé, une réponse par ligne :
Q01: <réponse>
commande: <commande(s) utilisée(s)>
-->

Q01: il y a 32 commits accessibles depuis le tag depart
commande: git rev-list --count depart

Q02: C'est Sarah Benali qui a écrit la ligne return de la fonction formaterLigne dans src/format.js
commande: git blame depart -- src/format.js

Q03: Voici le SHA du premier commit fautif : 4459c91715f9b1c97cf4776ad2e5afbdb3aa7051
commande: node scripts/controle-alertes.js
          echo $?
          git bisect start
          git bisect bad depart
          git bisect good v0.2.0
          git bisect run node scripts/controle-alertes.js

Q04: API_KEY=sk_live_01de6ba0c9f4d846
commande: git log --all -p -i -G"api[_-]?key|secret|token" --format="COMMIT %h %s"

Q05: 11544ab
commande: git log --all --diff-filter=D --name-only --format="COMMIT %h %s"

Q06: 17 commits sont accessibles depuis la v1.0.0 mais pas depuis v0.2.0 
commande: git rev-list --count v0.2.0..v1.0.0

Q07: c'est le commit "essai-perf" qui est un tag leger
commande: git for-each-ref refs/tags --format="%(refname:short) %(objecttype)"


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
